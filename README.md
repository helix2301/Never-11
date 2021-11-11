# Never-11
This is a fix Microsoft released to stop Windows 11 from being installed on machines that do not want it.

There is an easy way to block Windows 11 from being offered to your PC.

Microsoft introduced a new TargetReleaseVersion specification in Windows 10 1803, which allows you to set which version of Windows 10 you would like your OS to upgrade to or remain at.

To prevent the Windows 11 from being offered to you, you simply need to registry editing on Windows 10 Home.

to press windows + R., type regedit and press log into
Navigate to Computer HKEY_LOCAL_MACHINE SOFTWARE Policies Microsoft Windows Windows Update
Create a new DWORD (32-bit) value called TargetReleaseVersion and assign it a value of 1
Create another DWORD (32-bit) value called TargetReleaseVersionInfo and assign it a value of 21H1
If you have Windows 10 Pro or Enterprise, you can do the same via the Local Group Policy Editor.

Simply go to Local computer policy > Computer configuration > Administrative Templates > Windows components > Windows update > Windows Update for Business and double click Select the target feature upgrade version. Enter 21H1 and hit ok before restarting your computer.

This registry option and or group policy will need to be updated if you want the next build of Windows 10 when its released but at least you will not get Windows 11.
