# Github-lookup
A ROBLOX game that uses Github's API, it allows players to see public repos and check public informations about a github profile.

game link: https://www.roblox.com/games/10283170475/Github-lookup

**How does it work?**
Example of HTTP GET request on ROBLOX Studio: ``game:GetService("HttpService"):GetAsync("API_URL")``
Github's api url is : ``https://api.github.com``

To get the user's public data:

 	local url = "https://api.github.com"
  	local data = httpService:GetAsync(string.format("%s/users/%s", url, Username))
	return httpService:JSONDecode(data)

To get the user's repos:

	local url = "https://api.github.com"
	local data = httpService:GetAsync(string.format("%s/users/%s/repos", url, Username))
	return httpService:JSONDecode(data)
  
And to get repo's content/ file content:

	local url = "https://api.github.com"
	local data = httpService:GetAsync(string.format("%s/repos/%s/%s/contents%s", url, Username, Repo, "/"..path))
	return httpService:JSONDecode(data)
