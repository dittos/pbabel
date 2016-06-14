# ⚡️ pbabel

Parallel version of Babel CLI.


## Install

```sh
$ npm install --save-dev pbabel
```

## Usage

Pretty much same with [Babel CLI](http://babeljs.io/docs/usage/cli/).

* You may use `-j N` option to limit concurrency. The number of CPUs is used by default.
* `--watch` mode is not supported.

## Performance

```sh
$ nproc
4

$ time ./node_modules/.bin/pbabel -d parallel frontend/js -q

real	0m2.831s
user	0m7.904s
sys	0m1.912s
```

Compared to the original babel-cli:

```sh
$ time ./node_modules/.bin/babel -d serial frontend/js -q

real	0m4.346s
user	0m4.152s
sys	0m0.768s
```
