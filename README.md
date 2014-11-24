To get the id of an extension use:

```
cat FILE.PEM | \
openssl rsa -pubout -outform DER | \
openssl dgst -sha256 | \
awk '{print $2}' | \
cut -c 1-32 | \
tr '0-9a-f' 'a-p'
```

where FILE.PEM is the private key used to sign the extension.


For more information about installing, using, and/or developing for TrackingObserver,
please visit: http://trackingobserver.cs.washington.edu/

TrackingObserver was created by Franziska Roesner, Chris Rovillos, Alisha Saxena, 
and Tadayoshi Kohno as a research project of the University of Washington Computer 
Science and Engineering. TrackingObserver extends earlier research by Franziska Roesner, 
Tadayoshi Kohno, and David Wetherall.

This work is supported in part by the National Science Foundation (Grant CNS-0846065 and 
a Graduate Research Fellowship under Grant DGE-0718124) and by a Microsoft Research PhD 
Fellowship```
openssl dgst -sha256 | \
.
