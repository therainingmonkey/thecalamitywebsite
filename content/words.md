<hr>

{{
	local output = ""
	
	for name, post in pairs(content.posts) do
	
	-- ### [<POST TITLE>](<URL>)\n<POST TEXT FOLLOWING POST TITLE UP TO 144 CHARS>
		
		local title = post:match("#(.-)\n") or ''
		output = output .. "## ["..title.."](./posts/"..name..".html)\n"..post:match("#.-\n(.*)"):sub(1, 144).."...\n\n"
		
	end
	
	return output
}}
