# Installing Software
This will obviously need to be expanded.

However you can look at the openbabel module and see the example README.md:
[Openbabel](openbabel "openbabel")

## Installs
1. Make sure you have a checkout of the biocluster-modules repository
2. Login as ```pkgadmin```
3. **Move to the ```opt/src``` directory**
4. **Download and untar the source in ```opt/src```**
5. **Create a directory named ```pkgs/[name of module]/[module version]```**
6. If precompiled, move the binaries to the directory created in step 5
7. Log out of ```pkgadmin```
8. Move to your local biocluster-modules directory
9. Copy any one of the existing directories into a new directory with the same name as the module being installed
10. Go into the newly created directory
11. **Edit the ```.version``` file so that it contains the correct version number**
12. Rename the ```[module version]``` file with the version number of the newly installed module
13. Edit the file from step 12 so that it contains the correct module name, version and paths
14. ```git add``` both files, ```git commit``` the changes then ```git push```
15. After this you can test the installtion by trying ```module load [name of module]``` and ```module avail [name of module]```

## Modules
These are the modules that are currently available on biocluster

Module files now use environment variables to determine the path:
    IIGB_MODULES - Path dynamically built by /etc/profile.d/modules.sh at login to specify install path of modules.
    MODULESHOME - Path set by module system to specify home of module system.
