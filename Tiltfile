k8s_yaml('k8s.yaml')

local_resource('write-date', 'date > thedate')
docker_build('parent', '.', dockerfile='Dockerfile.parent')
docker_build('child', '.', dockerfile='Dockerfile.child')

k8s_resource('mypod', resource_deps=['write-date'])
