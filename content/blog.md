## Notes on The Struggle
<hr>

{{
	local output = ""
	
	for name, post in pairs(content.posts) do
	
	-- ### [<POST TITLE>](<URL>)\n<POST TEXT FOLLOWING POST TITLE UP TO 144 CHARS>
	
		output = output .. "## ["..post:match("#(.-)\n").."](".."./posts/"..name..".html)\n"..post:match("#.-\n(.*)"):sub(1, 144).."...\n\n"
		
	end
	
	return output
}}
