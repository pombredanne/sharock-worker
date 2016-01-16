# Sharock Worker
[![Circle CI](https://img.shields.io/circleci/project/shardsrocks/sharock-worker/master.svg)](https://circleci.com/gh/shardsrocks/sharock-worker/tree/master)

Background worker for Sharock.

## Requirements

- Go v1.5
- [gom](https://github.com/mattn/gom)
- [goworker](https://github.com/benmanns/goworker)
- Redis

## Build

```
$ go get github.com/mattn/gom
$ gom install
$ gom build
```

## Run
### worker

```
$ ./sharock-worker --queues=sharock --use-number
```

### enqueue

```
$ redis-cli RPUSH resque:queue:sharock '{"class":"Resolve","args":[256]}'
```

## License
MIT License
