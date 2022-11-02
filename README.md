# Firefox Launcher MOD

## Description

X-firefox is a project developed by winpenpack.it to make portable Mozilla Firefox

It uses a program called X-launcher.

X-Launcher is a launcher, which is a program that launches other programs. 
X-Launcher allows you to freely edit the boot options of programs initiated in order to make them portable,
that is usable on removable storage devices like USB flash drives or external hard drives.


### Issues with firefox launcher

- X-firefox launcher (ver 1.5.4) seems not to be in active development and it uses a old version of autoit compiler.
- Launcher doesn't manage two files in user profile that contain absolute path 
  -- estensions.json (https://bugzilla.mozilla.org/show_bug.cgi?id=1429838)
  -- addonStartup.json.lz4 that is a json compressed in proprietary MozLz4 format

### Approach to resolve issues
- Change code to use AutoIt v3.3.16.1 [Scite 4.4.6]
- Use external program to manage MozLz4 (decompress/compress) https://github.com/jusw85/mozlz4
- Make launcher able to edit estensions.json and addonStartup.json.lz4 changing the absolute paths in the files with the absolute path of current location of the launcher


### Note

- You MUST make a backup of your profile folder in order to try this MOD

