## Installation

``` bash
gem install loc_counter
```

## Usage

The gem installs a single executable `loc_counter`.

### On a project

If you want to count LOCs in your Rails app or in a gem, you can just pass a path to that project's directory to `loc_counter`:

``` bash
$ loc_counter /path/to/project
48 files processed
Total     1826 lines
Empty     331 lines
Comments  372 lines
Code      1123 lines
```

In 'project mode' it scans `app`, `bin`, `config`, `lib` and top-level directories of your project, processing the following files:

- `Capfile`
- `Gemfile`
- `Rakefile`
- `*.gemspec`
- `*.rake`
- `*.rb`
- `*` in `bin` directory

### On arbitrary files

You can also give `loc_counter` any files you want to measure.

``` bash
$ loc_counter ~/*.rb              
5 files processed
Total     118 lines
Empty     27 lines
Comments  4 lines
Code      87 lines
```