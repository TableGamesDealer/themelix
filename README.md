themelix

Themelix is a lightweight utility for dynamically managing and applying themes to the Helix text editor. Designed to enhance your workflow, it integrates seamlessly with Helix and terminal-based tools like Zellij for a more immersive coding experience.

Features

Dynamically change Helix themes.
Automatically create a default configuration if missing.
Clear terminal scroll buffer for a cleaner workflow.
Can be used as a standalone CLI tool or a library in other Rust projects.
Installation

Prerequisites
Rust: Ensure you have the Rust toolchain installed. You can install it via rustup.
Helix Editor: Themelix manages themes in the  ~/Library/Application Support/helix/config.toml file.
Clone and Build
Clone the repository:
git clone https://github.com/<your-username>/themelix.git
cd themelix
Build the binary:
cargo build --release
Add the binary to your $PATH:
cp target/release/themelix ~/.local/bin/
Usage as a Library
Add themelix to your Cargo.toml as a dependency:

[dependencies]
themelix = { git = "https://github.com/<your-username>/themelix.git" }
Usage

CLI Mode
Run the tool from your terminal:

themelix --theme <theme_name> <file> [OPTIONS]
Arguments:

--theme <theme_name>: The Helix theme to apply.
<file>: The file to open in Helix after applying the theme.
Options:

--quiet, -q: Suppress output messages.
--clear-buffer, -c: Clear the terminal scroll buffer before opening Helix.

Example:

themelix --theme nord example.rs --clear-buffer
Library Mode
Use Themelix's functionality in your Rust projects:

Configuration

Themelix modifies the ~/Library/Application Support/helix/config.toml file to set the desired theme. If the file does not exist, it creates a default configuration with a placeholder theme.

Example config.toml:

theme = "nord"

Contributing

Contributions are welcome! To contribute:
idk man im to new at this


License

This project is licensed under the Apache 2.0 License.

Let me know if you'd like to make any adjustments or add more details!
