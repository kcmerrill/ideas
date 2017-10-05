# bobba

I'd like to create a command line launcher for various things.

The idea would be a weighted fuzzy finder. Bash History, URL History, files, executables. Depending on weighted order, previous usages, etc ... would go to the right thing

`$ boba stop`

Based on a generic 0-1 scale, direct matches would be closer to 1(or some scale) would determine by looking through your command history, prebaked commands, files, folders bookmarks. In this case, we'd have a command, that would stop spotify from playing and would execute the command.

Each inventory that bobba would search through would be a type, so `bookmark`, `file`, `dir`, 'shell', 'cmd' etc .. and you'd be able to map based on rules. Oh, found a file? I like to open it in vim so shell out `vim file.txt`

Lets say, I'm in `/code/go/src/github.com/kcmerrill/bobba` and I need to make a change in a different repo, say `/code` and I did `boba mycoolprojectsomefile` boba would look through your inventory, in this case some smart folder structure(say all the way up to /something and also maybe a few adjacent folders over a few levels deep) for a folders/files. Depending on weights, and your previous launching history, would go to the appropriate place.

Another scenario, `boba wwwkcmerrill/alfred` might open a browser based on my history to http://www.github.com/kcmerrill/alfred. Of course, the more the fuzzy matcher could match on, the more accurate the results.
