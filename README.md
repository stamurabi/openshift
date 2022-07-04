# openshift

test oc binary

oc new-app --name echo https://github.com/stamurabi/openshift.git#ubi --context-dir ubi-echo

  #ubi => branch name

  --context-dir => subdir with Dockerfile
