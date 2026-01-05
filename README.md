# About

This repository contains AMP required customizations on vanilla upstream galaxy repository, including both full files not existing in upstream galaxy and patches of the customized files in galaxy. AMP deployment scripts will super-pose these files and patches onto galaxy code base during build process. This allows AMP to utilize upstream galaxy without a forked repository. The patches are generated against the galaxy branch used by AMP (i.e. with AMP's latest galaxy upgrade, ideally pointing to the latest Galaxy release branch, but could be a bit behind).

The major customizations to the upstream galaxy code base include but are not limited to:
- changes in tool command script to include AMP required environment variables for running MGMs.
- extensions to data types related various media formats, as well as workflow outputs in AMP specific JSON formats.
- extensions to JobRunner, mainly for the purpose of running LWLW (light-weight-long-waiting) jobs, such as Human MGMs and various clound-based MGMs.
- configuration files for datatype, job etc.
- changes in galaxy client code to remove extra UI components not allowed in AMP Workflow Editor.
- scripts for deploying galaxy.

# Usage

AMP Galaxy can be run as a standalone application but its UI is advised to be only accessible to AMP Admin and not available to end users. Galaxy APIs are also wrapped by AMP backend and are hiden from external clients for security reasons. AMP Galaxy instance is a required dependency of AMP backend. Detailed information about this component in relationship to other AMP components is described in [AMP System Architecture](https://uisapp2.iu.edu/confluence-prd/display/AMP/System+Architecture?src=contextnavpagetreemode).

To install, config, run AMP Galaxy, as well as contribute to the AMP project, please refer to the instructions on [AMP Bootstrap](https://github.com/AudiovisualMetadataPlatform/amp_bootstrap)
