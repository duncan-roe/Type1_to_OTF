# Type1_to_OTF
Type1_to_OTF converts most of the Type1 (Postscript) fonts in
/usr/share/fonts/Type1 to OTF fonts in /usr/share/fonts/OTF.

The only fonts not converted are ones that libreoffice can't render
(e.g. dingbats).

Some italic variants don't translate,
but libreoffice manages to display them as italic anyway.

You need to have installed Adobe Font Development Kit for OpenType (afdko)
http://www.adobe.com/devnet/opentype/afdko.html
to use Type1_to_OTF.
