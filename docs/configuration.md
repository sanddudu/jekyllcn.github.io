---
layout: docs
title: 配置
prev_section: structure
next_section: frontmatter
permalink: /docs/configuration/
contributor: sanddudu
---

得益于强大且灵活的配置选项，Jekyll 允许你使用任何你能想要的方式改造你的站点。这些
选项可以指定在你站点的根目录下的 `_config.yml` 文件里，或者在终端执行 `jekyll` 时
作为参数。

## 配置设定

### 全局配置

下面的表格列出了可用的 Jekyll 设置，分别由 <code class="option">选项</code> (被指
定在配置文件中) 和 <code class="flag">参数</code> (被指定在命令行中) 控制。

<div class="mobile-side-scroller">
<table>
  <thead>
    <tr>
      <th>设置</th>
      <th>
        <span class="option">选项</span> 和 <span class="flag">参数</span>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr class='setting'>
      <td>
        <p class='name'><strong>Site Source</strong></p>
        <p class='description'>更换 Jekyll 读取文件的目录。</p>
      </td>
      <td class="align-center">
        <p><code class="option">source: DIR</code></p>
        <p><code class="flag">-s, --source DIR</code></p>
      </td>
    </tr>
    <tr class='setting'>
      <td>
        <p class='name'><strong>Site Destination</strong></p>
        <p class='description'>更换 Jekyll 写入文件的目录。</p>
      </td>
      <td class="align-center">
        <p><code class="option">destination: DIR</code></p>
        <p><code class="flag">-d, --destination DIR</code></p>
      </td>
    </tr>
    <tr class='setting'>
      <td>
        <p class='name'><strong>Safe</strong></p>
        <p class='description'>关闭 <a href="../plugins/">自定义插件。</a>.</p>
      </td>
      <td class="align-center">
        <p><code class="option">safe: BOOL</code></p>
        <p><code class="flag">--safe</code></p>
      </td>
    </tr>
    <tr class='setting'>
      <td>
        <p class='name'><strong>Exclude</strong></p>
        <p class="description">在转换时被排除的目录和（或）文件。</p>
      </td>
      <td class='align-center'>
        <p><code class="option">exclude: [DIR, FILE, ...]</code></p>
      </td>
    </tr>
    <tr class='setting'>
      <td>
        <p class='name'><strong>Include</strong></p>
        <p class="description">
          被强制转换的目录和（或）文件。<code>.htaccess</code> 是一个很好的例子因为以
          "." 开头的文件是默认被排除的。
        </p>
      </td>
      <td class='align-center'>
        <p><code class="option">include: [DIR, FILE, ...]</code></p>
      </td>
    </tr>
    <tr class='setting'>
      <td>
        <p class='name'><strong>Time Zone</strong></p>
        <p class="description">
            设置站点生成的时区。这个设置将会更改 <code>TZ</code> 环境变量，Ruby使用
            这个变量处理创建时间和日期的操作。输入 <a href="http://en.wikipedia.org/wiki/Tz_database">IANA 时区数据库</a> 
            里的任意时区都是有效的，比如 <code>America/New_York</code> 。时区默认设置为
            本地时间，即你的操作系统系统的时间。
        </p>
      </td>
      <td class='align-center'>
        <p><code class="option">timezone: TIMEZONE</code></p>
      </td>
    </tr>
    <tr class='setting'>
      <td>
        <p class='name'><strong>Encoding</strong></p>
        <p class="description">
            设置文件编码的名称。（仅在Ruby 1.9或以后版本可用）
            默认值为 nil ，使用Ruby默认的 <code>ASCII-8BIT</code> 编码。
            可以通过执行 <code>ruby -e 'puts Encoding::list.join("\n")'</code> 来查看 Ruby 可用的
            编码列表。
        </p>
      </td>
      <td class='align-center'>
        <p><code class="option">encoding: ENCODING</code></p>
      </td>
    </tr>
  </tbody>
</table>
</div>

### 构建命令选项

<div class="mobile-side-scroller">
<table>
  <thead>
    <tr>
      <th>设置</th>
      <th><span class="option">选项</span> 和 <span class="flag">参数</span></th>
    </tr>
  </thead>
  <tbody>
    <tr class='setting'>
      <td>
        <p class='name'><strong>Regeneration</strong></p>
        <p class='description'>开启当文件被更改时自动重新生成站点的功能。</p>
      </td>
      <td class="align-center">
        <p><code class="flag">-w, --watch</code></p>
      </td>
    </tr>
    <tr class='setting'>
      <td>
        <p class='name'><strong>Configuration</strong></p>
        <p class="description">指定配置文件而不自动使用 <code>_config.yml</code> 。
        后面指定的文件中的设定将会覆盖之前指定的文件的设定。</p>
      </td>
      <td class='align-center'>
        <p><code class="flag">--config FILE1[,FILE2,...]</code></p>
      </td>
    </tr>
    <tr class='setting'>
      <td>
        <p class='name'><strong>Drafts</strong></p>
        <p class="description">处理且渲染草稿文章。</p>
      </td>
      <td class='align-center'>
        <p><code class="flag">--drafts</code></p>
      </td>
    </tr>
    <tr class='setting'>
      <td>
        <p class='name'><strong>Future</strong></p>
        <p class="description">使用一个未来的时间发布文章。</p>
      </td>
      <td class='align-center'>
        <p><code class="option">future: BOOL</code></p>
        <p><code class="flag">--future</code></p>
      </td>
    </tr>
    <tr class='setting'>
      <td>
        <p class='name'><strong>LSI</strong></p>
        <p class="description">生成相关文章的索引</p>
      </td>
      <td class='align-center'>
        <p><code class="option">lsi: BOOL</code></p>
        <p><code class="flag">--lsi</code></p>
      </td>
    </tr>
    <tr class='setting'>
      <td>
        <p class='name'><strong>Limit Posts</strong></p>
        <p class="description">解析和发布文章的数量限制</p>
      </td>
      <td class='align-center'>
        <p><code class="option">limit_posts: NUM</code></p>
        <p><code class="flag">--limit_posts NUM</code></p>
      </td>
    </tr>
  </tbody>
</table>
</div>

### 服务命令选项

除了下面的选项之外，`serve` 子命令可以接受任何执行于网站构建之前的 `build` 子命令的选项。

<div class="mobile-side-scroller">
<table>
  <thead>
    <tr>
      <th>设置</th>
      <th><span class="option">选项</span> 和 <span class="flag">参数</span></th>
    </tr>
  </thead>
  <tbody>
    <tr class='setting'>
      <td>
        <p class='name'><strong>Local Server Port</strong></p>
        <p class='description'>在指定端口监听</p>
      </td>
      <td class="align-center">
        <p><code class="option">port: PORT</code></p>
        <p><code class="flag">--port PORT</code></p>
      </td>
    </tr>
    <tr class='setting'>
      <td>
        <p class='name'><strong>Local Server Hostname</strong></p>
        <p class='description'>在指定主机名上监听</p>
      </td>
      <td class="align-center">
        <p><code class="option">host: HOSTNAME</code></p>
        <p><code class="flag">--host HOSTNAME</code></p>
      </td>
    </tr>
    <tr class='setting'>
      <td>
        <p class='name'><strong>Base URL</strong></p>
        <p class='description'>Serve the website from the given base URL</p>
      </td>
      <td class="align-center">
        <p><code class="option">baseurl: URL</code></p>
        <p><code class="flag">--baseurl URL</code></p>
      </td>
    </tr>
    <tr class='setting'>
      <td>
        <p class='name'><strong>Detach</strong></p>
        <p class='description'>使服务脱离终端在后台运行。</p>
      </td>
      <td class="align-center">
        <p><code class="option">detach: BOOL</code></p>
        <p><code class="flag">-B, --detach</code></p>
      </td>
    </tr>
  </tbody>
</table>
</div>

<div class="note warning">
  <h5>在配置文件中不要使用 Tab</h5>
  <p>
    这将导致解析错误，Jekyll 会使用默认设置。使用空格来代替 Tab。
  </p>
</div>

## 默认配置

Jekyll 将默认使用以下的配置运行。除非替代的设置指定在配置文件或命令行里。

<div class="note warning">
  <h5>有两个 kramdown 选项不被支持</h5>
  <p>
    由于 kramdown HTML 转换器中并不包含 <code>remove_block_html_tags</code> 和 <code>remove_span_html_tags</code> ，
    Jekyll 将不支持这两个选项。
  </p>
</div>

{% highlight yaml %}
source:      .
destination: ./_site
plugins:     ./_plugins
layouts:     ./_layouts
include:     ['.htaccess']
exclude:     []
keep_files:  ['.git','.svn']
timezone:    nil
encoding:    nil

future:      true
show_drafts: nil
limit_posts: 0
pygments:    true

relative_permalinks: true

permalink:     date
paginate_path: 'page:num'

markdown:      maruku
markdown_ext:  markdown,mkd,mkdn,md
textile_ext:   textile

excerpt_separator: "\n\n"

safe:        false
watch:       false    # deprecated
server:      false    # deprecated
host:        0.0.0.0
port:        4000
baseurl:     /
url:         http://localhost:4000
lsi:         false

maruku:
  use_tex:    false
  use_divs:   false
  png_engine: blahtex
  png_dir:    images/latex
  png_url:    /images/latex

rdiscount:
  extensions: []

redcarpet:
  extensions: []

kramdown:
  auto_ids: true
  footnote_nr: 1
  entity_output: as_char
  toc_levels: 1..6
  smart_quotes: lsquo,rsquo,ldquo,rdquo
  use_coderay: false

  coderay:
    coderay_wrap: div
    coderay_line_numbers: inline
    coderay_line_numbers_start: 1
    coderay_tab_width: 4
    coderay_bold_every: 10
    coderay_css: style

redcloth:
  hard_breaks: true
{% endhighlight %}


## Markdown 选项

被 Jekyll 支持的 Markdown 渲染器有他们可用的额外选项。

### Redcarpet

Redcarpet 可以通过给定一个 `extensions` 副设置进行配置, 它的值应该是一个字符串数组。每个字符串都应该被命名为 `Redcarpet::Markdown` 类的扩展；如果出现在数组中，相应的扩展将被设为 `true`。

Jekyll 处理两个特别的 Redcarpet 扩展:

- `no_fenced_code_blocks` --- Jekyll 默认将 `fenced_code_blocks` 扩展 （用来分割由三个波浪线和三个反向引号组成的代码块）设为 `true`，probably because GitHub's eager adoption of them is starting to make them inescapable. Redcarpet's normal `fenced_code_blocks` extension is inert when used with Jekyll; instead, you can use this inverted version of the extension for disabling fenced code.

    Note that you can also specify a language for highlighting after the first delimiter:

        ```ruby
        # ...ruby code
        ```

    With both fenced code blocks and pygments enabled, this will statically highlight the code; without pygments, it will add a `class="LANGUAGE"` attribute to the `<code>` element, which can be used as a hint by various JavaScript code highlighting libraries.
- `smart` --- This pseudo-extension turns on SmartyPants, which converts straight quotes to curly quotes and runs of hyphens to em (`---`) and en (`--`) dashes.

All other extensions retain their usual names from Redcarpet, and no renderer options aside from `smart` can be specified in Jekyll. [A list of available extensions can be found in the Redcarpet README file.][redcarpet_extensions] Make sure you're looking at the README for the right version of Redcarpet: Jekyll currently uses v2.2.x, and extensions like `footnotes` and `highlight` weren't added until after version 3.0.0. The most commonly used extensions are:

- `tables`
- `no_intra_emphasis`
- `autolink`

[redcarpet_extensions]: https://github.com/vmg/redcarpet/blob/v2.2.2/README.markdown#and-its-like-really-simple-to-use
