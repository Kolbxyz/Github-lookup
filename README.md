# Github-lookup
A ROBLOX game that uses Github's API

game link: https://www.roblox.com/games/10283170475/Github-lookup

**How does it worK?**
The game uses Github's APIs with game:GetService("HttpService"):GetAsync("API_URL")

To get the user's public data I simply use this:

 	 local url = "https://api.github.com"
  	local data = httpService:GetAsync(string.format("%s/users/%s", url, Username))
	  return httpService:JSONDecode(data)

To get the user's repos I use this:

	local url = "https://api.github.com"
	local data = httpService:GetAsync(string.format("%s/users/%s/repos", url, Username))
	return httpService:JSONDecode(data)
  
And to get repo's content/ file content I use this:

	local url = "https://api.github.com"
	local data = httpService:GetAsync(string.format("%s/repos/%s/%s/contents%s", url, Username, Repo, "/"..path))
	return httpService:JSONDecode(data)
