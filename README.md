# configuration starship

```toml
#format = """
#[╭─user───❯](bold blue) $username
#[┣─system─❯](bold yellow) $hostname
#[┣─project❯](bold red) $directory$rust$git_branch$git_status$package$golang$terraform$docker_context$python$docker_context$nodejs
#[╰─cmd────❯](bold green) 
#"""
[username]
style_user = "green bold"
style_root = "red bold"
format = "[Mr.Robots]($style) "
disabled = false
show_always = true

[hostname]
ssh_only = false
format = 'on [$hostname](bold yellow) '
trim_at = "."
disabled = true

# Replace the "❯" symbol in the prompt with "➜"
[character]                            # The name of the module we are configuring is "character"
success_symbol = "[➜](bold green)"     # The "success_symbol" segment is being set to "➜" with the color "bold green"
error_symbol = "[✗](bold red)"
#  
# configure directory
[directory]
read_only = " "
truncation_length = 5
truncate_to_repo = true # truncates directory to root folder if in github repo
style = "bold italic blue"

[cmd_duration]
min_time = 4
show_milliseconds = false
disabled = false
style = "bold italic purple"

[aws]
symbol = "  "

[conda]
symbol = " "

[dart]
symbol = " "

[docker_context]
symbol = " "
format = "via [$symbol$context]($style) "
style = "blue bold"
only_with_files = true
detect_files = ["docker-compose.yml", "docker-compose.yaml", "Dockerfile"]
detect_folders = []
disabled = false

[elixir]
symbol = " "

[elm]
symbol = " "

[git_branch]
symbol =  "🚀 "  # Menggunakan simbol daun untuk cabang Git
format = "on [$symbol$branch]($style) "
style = "bold purple"
disabled = false

[git_status]
conflicted = "✖"  # the character to represent conflicted state
ahead = "⬆"  # the character to represent ahead state
behind = "⬇"  # the character to represent behind state
diverged = "⭠"  # the character to represent diverged state
renamed = "➦"  # the character to represent renamed state
deleted = "✖"  # the character to represent deleted state
staged = "✔"  # the character to represent staged state
untracked = "✭"  # the character to represent untracked state
stashed = "🗑"  # the character to represent stashed stat
modified = "✚"  # the character to represent modified state




[golang]
symbol = " "


[java]
symbol = " "

[julia]
symbol = " "

[memory_usage]
symbol = "󰍛 "

[nim]
symbol = " "

[nix_shell]
symbol = " "

[package]
symbol = "󰏗 "

[perl]
symbol = " "

[php]
symbol = " "

[python]
symbol = " "
#pyenv_version_name = true
format = 'via [${symbol}python (${version} )(\($virtualenv\) )]($style)'
style = "bold yellow"
pyenv_prefix = "venv "
python_binary = ["./venv/bin/python", "python", "python3", "python2"]
detect_extensions = ["py"]
version_format = "v${raw}"

[ruby]
symbol = " "

[rust]
symbol = " "

[scala]
symbol = " "

[shlvl]
symbol = " "

[swift]
symbol = "ﯣ "

[nodejs]
format = "via [ Node.js $version](bold green) "
detect_files = ["package.json", ".node-version"]
detect_folders = ["node_modules"]


```
