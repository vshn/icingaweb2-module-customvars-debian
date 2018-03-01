# Packaging instruction

1. Add a tag to source repository to create a release
1. Download .tar.gz from source repository
1. $ gbp import-orig ../downloaded-from-source-repository.tar.gz, enter version number
1. $ dch -v X.Y.Z-1
1. $ dch -r -D xenial
1. $ git commit debian/changelog
1. $ gbp buildpackage 
1. Test the package
1. $ gbp buildpackage -S --git-tag 
1. $ git push --all
1. $ git push --tags
1. $ cd ..
1. $ dput ppa:vshn/icinga source.changes icingaweb2-module-customvars\_X.Y.Z-1\_amd64.changes
