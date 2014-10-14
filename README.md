# CoderDojo Sign-in App

IMPORTANT: DO NOT COMMIT THE `attendance.dat*` FILES. THESE ARE NOT PUBLIC.

## CSPro installation

Install CSPro on a Windows PC or under Wine with Linux. We're using CSPro 6.0.1
which can be downloaded from http://www.csprousers.org/beta/.

## Installing on tablet

Install the CSEntry for Android (.apk) on the Android table. Detailed
instructions are provided on the CSPro beta page.

Copy the `coderdojo.pen` and `coderdojo.pff` files to the Android tablet and put
them in the `csentry/Coderdojo` directory.

## Resources

http://www.csprousers.org/
http://www.census.gov/population/international/

## Handling the attendance data

The attendance data must never contain sensitive items like create credit cards,
social security numbers, etc. (I'd be surprised if anyone would actually enter
those anyway since we have no use for them.) Nevertheless, we encrypt the
attendance data here since this repository is Internet accessible.

To handle the attendance files, do the following, and replace `pword` with the proper password:

On Linux, do this:
```
# Encrypting the file
7z a -ppword attendance.7z attendance.dat

# Decrypting (erase old files first to avoid any confusion)
rm attendance.dat*
7z e -ppword attendance.7z
```

On Windows, do this:

TBD
