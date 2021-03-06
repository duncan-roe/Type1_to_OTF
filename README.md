# Type1_to_OTF
Type1_to_OTF converts most of the Type1 (Postscript) fonts in
/usr/share/fonts/Type1 to OTF fonts in /usr/share/fonts/OTF.

The only fonts not converted are ones that libreoffice can't render
(e.g. dingbats), or libreoffice already offers (e.g. luxi mono).

Some italic variants don't translate,
but libreoffice manages to display them as italic anyway.

You need to have installed Adobe Font Development Kit for OpenType (afdko)
http://www.adobe.com/devnet/opentype/afdko.html
to use Type1_to_OTF.

## Usage instructions
You need to create a temporary directory somewhere. In the example below, we use */tmp/t5*.
### As a regular user (not root)
```bash
   mkdir /tmp/t5
   cd Type1_to_OTF-1.0
   cp FontMenuNameDB makeotf.sh /tmp/t5
   cd /tmp/t5
   cp /usr/share/fonts/Type1/*.pf{a,b} .
   ./makeotf.sh
```

### As root

```bash
   cd /usr/share/fonts/OTF
   mv /tmp/t5/*.otf .
   mkfontscale
   mkfontdir
   fc-cache -f
```

### As a regular user again

```bash
   rm -r /tmp/t5
```
