# StorageHelper for Android
Get all storage on a device including USB devices

#### This class retrieves all storages using current Android API.

##### To copy [Doctoror Drive](https://github.com/Doctoror) words from [stackoverflow.com](http://stackoverflow.com/questions/22219312/android-open-external-storage-directorysdcard-for-storing-file):

The internal storage is referred to as "external storage" in the API.

As mentioned in the Environment documentation:

>Note: don't be confused by the word "external" here. This directory can better be thought as media/shared storage. It is a >filesystem that can hold a relatively large amount of data and that is shared across all applications (does not enforce >permissions). Traditionally this is an SD card, but it may also be implemented as built-in storage in a device that is >distinct from the protected internal storage and can be mounted as a filesystem on a computer.


To distinguish whether "Environment.getExternalStorageDirectory()" actually returned physically internal or external storage, call Environment.isExternalStorageEmulated(). If it's emulated, than it's internal. On newer devices that have internal storage and sdcard slot Environment.getExternalStorageDirectory() will always return the internal storage. While on older devices that have only sdcard as a media storage option it will always return the sdcard.

#####There is no way to retrieve all storages using current Android API.

#### End of his words


This class I modified is based on [Vitaliy Polchuk's](http://stackoverflow.com/users/900026/vitaliy-polchuk)
work with modification from [Doctoror Drive](https://github.com/Doctoror)

### License
See [License](/LICENSE)
