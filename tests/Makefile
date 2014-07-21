test:
	GOPATH=$(CURDIR)/_vendor:$(GOPATH) \
	go test -tags integration -v -run TestGlobal
	go test -tags integration -v -run TestApps

test-smoke:
	GOPATH=$(CURDIR)/_vendor:$(GOPATH) \
	go test -tags integration -short -v -run TestSmoke

nuke_from_orbit:
	-docker kill `docker ps -q`
	-docker rm `docker ps -a -q`
	-docker rmi -f `docker images -q`
