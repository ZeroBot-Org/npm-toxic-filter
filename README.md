# npm-toxic-filter

Run npm/yarn commands as if you were in the past with toxic filter. Useful if you lost a lock file
or need to install a dependency in a legacy project that hasn't been updated in a while.

## Install

```sh
npm install -g npm-toxic-filter
```

## Usage as registry-server

Start registry server:

```sh
npm-toxic-filter 2019-07-20 --server --port 10001
```

Use it with npm commands:

```sh
NPM_CONFIG_REGISTRY=http://localhost:10001 npm install
```

## Usage as command wrapper

Run `npm install` as if you were back in `2016-05-06`:

```sh
npm-toxic-filter 2016-05-06 npm install redux
```

Check latest version which was at the time:

```sh
npm-toxic-filter 2016-05-06 npm show redux version
```

Use any other npm-commands in the same way. If you have any troubles, try to switch to registry-server.
