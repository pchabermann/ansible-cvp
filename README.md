# CVP_Ansible_Modules
Pre Release Work in progress Anisble modules for CVP

**cv_configlet**

 - add, delete, and show configlets.

  Configlets can be created, deleted then added to containers or devices. - also in cv_devices as required to move devices between containers
  Any Tasks that are generated as a result will be returned.
  Need to add the option to check (CVP verify) the configuration contained in the Configlet

**cv_container**
 - add, delete, and show containers

Containers can be created or deleted

**cv_device**
 - add, delete, and show devices

  Devices can be deployed from the undefined container to a provisioned container or moved from one container to another using the add functionality and specifying the target container. Configlets can be added to devices using add and specifying the current parent container.
  Devices can be Removed from CVP using the delete option and specifying "CVP" as the container, equivalent to the REMOVE GUI option.
  Devices can be reset and moved to the undefined container using the delete option and specifying "RESET" as the container.
  Configlets can be removed from a device using the delete option and specifying the configs to be removed and the current parent container as the container.
  show option provide device data and current config.

**cv_image [testing]**
 - add, delete, and show image bundles

  Image bundles must exist in CVP already, this module will allow the manipulation of them in CVP.
  Add and Delete will allow bundles to be applied or removed from Containers and devices
  Show will provide information on the contents of the image bundle.

**cv_tasks [Future]**
 - add, delete, and show tasks

  Tasks must exist in CVP already, this module will allow the manipulation of them in CVP.
  Add and Delete will allow Tasks to be executed or Canceled
  Show will provide information on the current Status or a Task.

**CvpRac**

  To use these modules you will need cvprac.
  The official version can be found here: [Arista Networks cvprac](https://github.com/aristanetworks/cvprac)
  CVPRACV2 in this repository is a tweaked version with additional functionality that has been requested in the official version. See README in CVPRACV2 folder.

  Other CVP Ansible modules can be found here: [Arista EOS+ Ansible Modules](https://github.com/arista-eosplus/ansible-cloudvision)
