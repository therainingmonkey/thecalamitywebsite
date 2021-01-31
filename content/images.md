{{
	local output = ''
	for i=1,15 do
		local img = '![](images-small/' .. i .. '.jpg)'
		output = output .. '<a href="./images/' .. i .. '.jpg">' .. img .. '</a>\n\n'
	end
	return output
}}
