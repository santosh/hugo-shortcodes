# hugo-shortcodes

![GitHub repo size](https://img.shields.io/github/repo-size/santosh/hugo-shortcodes)
![GitHub contributors](https://img.shields.io/github/contributors/santosh/hugo-shortcodes)
![GitHub stars](https://img.shields.io/github/stars/santosh/hugo-shortcodes?style=social)
![GitHub forks](https://img.shields.io/github/forks/santosh/hugo-shortcodes?style=social)
![GitHub followers](https://img.shields.io/github/followers/santosh?style=social)

While writing posts in markdown, writing HTML embed codes directly don't work.
And [shortcodes](https://gohugo.io/content-management/shortcodes/) were created
to fill this gap only. Shortcodes also DRY up things. You can find more information about shortcodes at [Hugo Docs][1].

hugo-shortcodes theme components contains a list of unofficial [Hugo][2] shortcodes.
If you are using a shortcode your blog, that you think belongs here, please make a PR.

## Getting Started

hugo-shortcodes comes as a theme component which makes it modular and easy to integrate in your existing site.

## Install

- `cd` to your Hugo powered site.

```bash
cd ~/repos/yoursite.dev
```

- Add this repo as a theme i.e. inside theme directory of your site.

```bash
git submodule add https://github.com/santosh/hugo-shortcodes.git themes/hugo-shortcodes
```

- Modify `config.toml` to list *hugo-shortcodes* as theme.

```toml
theme = ["hermit", "hugo-shortcodes"]
```

**Note**: In theme declaration in the config file. Componenets listed to the right will override components listed to the left of it. This means if two themes components defined same things, the later will be in effect. Check out [theme component](https://gohugo.io/hugo-modules/theme-components/) docs.

### Update

The easiest way to update hugo-shortcodes to latest is to issue following command from your main repo:

```bash
git submodule update --remote --merge themes/hugo-shortcodes
```

This will pull the latest updates from this repo and you will left to `git add` from your main repo.

## Usage

Below are possible directions to use available codes.

### Giphy

- Visit <https://giphy.com/>
- Search for your term, and open gif page.
- Copy the gif ID and pass if to `giphy`. Like below:

```md
{{< giphy 12UlfHpF05ielO >}}
```

You get a responsive version of gif embedded to the post.

### Blockquote

Blockquote takes:

- a source as first argument
- a body enclosed between `{{< blockquote >}}` tags, Like so:

```md
{{< blockquote "webassembly.org" >}}
WebAssembly (abbreviated Wasm) is a binary instruction format for a stack-based virtual machine. Wasm is designed as a portable target for compilation of high-level languages like C/C++/Rust, enabling deployment on the web for client and server applications.
{{</ blockquote >}}
```

## Contributing

Do you have an idea for a shortcode? Can you enhance an exiting shortcode? Or do you already use a certain shortcode that you want to be listed here? Great! Head over to [contribution guidelines][4] to get started.

## Contributors

Thanks to the following people who have contributed to this project:

- Santosh Kumar ([github](https://github.com/santosh), [twitter](https://twitter.com/sntshk))

## License

This project uses [Apache 2.0][3]. Same as Hugo.

[1]: https://gohugo.io/content-management/shortcodes/#what-a-shortcode-is
[2]: https://github.com/gohugoio/hugo
[3]: ./LICENSE
[4]: .github/CONTRIBUTING.md
