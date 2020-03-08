# Full-context label for VCTK-Corpus

This repository provides full-context label files for [VCTK-Corpus](https://homepages.inf.ed.ac.uk/jyamagis/page3/page58/page58.html).

The label files are created by following the preprocessing in [r9y9/deepvoice3_pytorch](https://github.com/r9y9/deepvoice3_pytorch).


## Data structure

```
├── lab
│   ├── full
│   │   ├── p225
│   │   │   ├── p225_001.lab
│   │   │   ├── p225_002.lab
│   │   │   ├── p225_003.lab
│   │   │   ├── p225_004.lab
│   │   │   ├── p225_005.lab
│   │   │   ...
│   ├── mono
│   │   ├── p225
│   │   │   ├── p225_001.lab
│   │   │   ├── p225_002.lab
│   │   │   ├── p225_003.lab
│   │   │   ├── p225_004.lab
│   │   │   ├── p225_005.lab
│   │   │   ...

```

## Label format

### Mono label

```
         0     850000 pau
    850000    2850000 pau
   2850000    3600000 p
   3600000    3900000 l
   3900000    6000000 iy
   6000000    8450000 z
   8450000    8600000 k
   8600000   11300000 ao
  11300000   11450000 l
  11450000   12800000 s
  12800000   13099999 t
  13099999   15800000 eh
  15800000   16050000 l
  16050000   17600000 ax
  17600000   20400000 pau
```

### Full context label

```
         0     850000 x^x-pau+pau=p@x_x/A:0_0_0/B:x-x-x@x-x&x-x#x-x$x-x!x-x;x-x|x/C:0+0+0/D:0_0/E:x+x@x+x&x+x#x+x/F:0_0/G:0_0/H:x=x@1=1|0/I:0=0/J:4+3-1
    850000    2850000 x^pau-pau+p=l@x_x/A:0_0_0/B:x-x-x@x-x&x-x#x-x$x-x!x-x;x-x|x/C:1+1+4/D:0_0/E:x+x@x+x&x+x#x+x/F:content_1/G:0_0/H:x=x@1=1|0/I:4=3/J:4+3-1
   2850000    3600000 pau^pau-p+l=iy@1_4/A:0_0_0/B:1-1-4@1-1&1-4#1-3$1-4!0-1;0-1|iy/C:1+1+3/D:0_0/E:content+1@1+3&1+2#0+1/F:content_1/G:0_0/H:4=3@1=1|L-L%/I:0=0/J:4+3-1
   3600000    3900000 pau^p-l+iy=z@2_3/A:0_0_0/B:1-1-4@1-1&1-4#1-3$1-4!0-1;0-1|iy/C:1+1+3/D:0_0/E:content+1@1+3&1+2#0+1/F:content_1/G:0_0/H:4=3@1=1|L-L%/I:0=0/J:4+3-1
   3900000    6000000 p^l-iy+z=k@3_2/A:0_0_0/B:1-1-4@1-1&1-4#1-3$1-4!0-1;0-1|iy/C:1+1+3/D:0_0/E:content+1@1+3&1+2#0+1/F:content_1/G:0_0/H:4=3@1=1|L-L%/I:0=0/J:4+3-1
   6000000    8450000 l^iy-z+k=ao@4_1/A:0_0_0/B:1-1-4@1-1&1-4#1-3$1-4!0-1;0-1|iy/C:1+1+3/D:0_0/E:content+1@1+3&1+2#0+1/F:content_1/G:0_0/H:4=3@1=1|L-L%/I:0=0/J:4+3-1
   8450000    8600000 iy^z-k+ao=l@1_3/A:1_1_4/B:1-1-3@1-1&2-3#1-2$1-3!1-1;1-1|ao/C:1+1+3/D:content_1/E:content+1@2+2&2+1#1+1/F:content_2/G:0_0/H:4=3@1=1|L-L%/I:0=0/J:4+3-1
   8600000   11300000 z^k-ao+l=s@2_2/A:1_1_4/B:1-1-3@1-1&2-3#1-2$1-3!1-1;1-1|ao/C:1+1+3/D:content_1/E:content+1@2+2&2+1#1+1/F:content_2/G:0_0/H:4=3@1=1|L-L%/I:0=0/J:4+3-1
  11300000   11450000 k^ao-l+s=t@3_1/A:1_1_4/B:1-1-3@1-1&2-3#1-2$1-3!1-1;1-1|ao/C:1+1+3/D:content_1/E:content+1@2+2&2+1#1+1/F:content_2/G:0_0/H:4=3@1=1|L-L%/I:0=0/J:4+3-1
  11450000   12800000 ao^l-s+t=eh@1_3/A:1_1_3/B:1-1-3@1-2&3-2#2-1$2-2!1-0;1-1|eh/C:0+1+2/D:content_1/E:content+2@3+1&3+0#1+0/F:0_0/G:0_0/H:4=3@1=1|L-L%/I:0=0/J:4+3-1
  12800000   13099999 l^s-t+eh=l@2_2/A:1_1_3/B:1-1-3@1-2&3-2#2-1$2-2!1-0;1-1|eh/C:0+1+2/D:content_1/E:content+2@3+1&3+0#1+0/F:0_0/G:0_0/H:4=3@1=1|L-L%/I:0=0/J:4+3-1
  13099999   15800000 s^t-eh+l=ax@3_1/A:1_1_3/B:1-1-3@1-2&3-2#2-1$2-2!1-0;1-1|eh/C:0+1+2/D:content_1/E:content+2@3+1&3+0#1+0/F:0_0/G:0_0/H:4=3@1=1|L-L%/I:0=0/J:4+3-1
  15800000   16050000 t^eh-l+ax=pau@1_2/A:1_1_3/B:0-1-2@2-1&4-1#3-1$3-1!1-0;1-0|ax/C:0+0+0/D:content_1/E:content+2@3+1&3+0#1+0/F:0_0/G:0_0/H:4=3@1=1|L-L%/I:0=0/J:4+3-1
  16050000   17600000 eh^l-ax+pau=x@2_1/A:1_1_3/B:0-1-2@2-1&4-1#3-1$3-1!1-0;1-0|ax/C:0+0+0/D:content_1/E:content+2@3+1&3+0#1+0/F:0_0/G:0_0/H:4=3@1=1|L-L%/I:0=0/J:4+3-1
  17600000   20400000 l^ax-pau+x=x@x_x/A:0_1_2/B:x-x-x@x-x&x-x#x-x$x-x!x-x;x-x|x/C:0+0+0/D:content_2/E:x+x@x+x&x+x#x+x/F:0_0/G:4_3/H:x=x@1=1|0/I:0=0/J:4+3-1
```

For details, please check [HTS documents](http://hts.sp.nitech.ac.jp).

## Reference

- [VCTK-Corpus](https://homepages.inf.ed.ac.uk/jyamagis/page3/page58/page58.html)
- [r9y9/deepvoice3_pytorch](https://github.com/r9y9/deepvoice3_pytorch)
