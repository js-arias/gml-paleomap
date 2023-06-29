# PaleoMap unrotated paleolandscape model

This model is based on the Scotese and Wrigth (2018) paleoDEMs
available at [EarthByte page](https://www.earthbyte.org/paleodem-resource-scotese-and-wright-2018/).
The digitalization uses the following convention,
to make more or less compatible with the [EarthByte model](https://github.com/js-arias/gm-earthbyte):

Elevation      | Key | Environment
-------------- | --- | -----------
4000m or more  |   6 | collision mountains
1500 to 2000m  |   4 | highlands
0 to 1500m     |   3 | lowlands
-200 to 0m     |   2 | continental shelf
-2000 to -200m |   1 | oceanic plateaus

Note that this paleolandscape does not include glacial ice sheets.

The model is then unrotated to present coordinates
using the [PaleoMap plate motion model](https://github.com/js-arias/gm-paleomap)
of Scotese (2016),
so it can be used with any rotation model.

## Time frame

The landscape model is defined from 540 million years ago
to today,
in time stages of 5 million years.

## Pixelation

The model is available in three resolutions:
e360 (360 pixels in the equatorial ring),
e180,
and e120.

## File descriptions

The model is stored in the file `paleomap-landscape-unrot-xxx-5.tab`,
in which `xxx` is the pixel resolution,
and 5 is the time resolution (in million years).

A color key,
which is compatible with color-blindness,
and can be used with `plates timepix map` command
is stored in the file `paleomap-landscape-key.tab`.

## Rotating the model

To rotate the paleolandscape model,
use the command `plates` from the [earth package](https://github.com/js-arias/earth):

```bash
plates timepix --model <your-model> --output <output-landscape-model> paleomap-landscape-unrot-xxx-5.tab
```

Note that in such cases,
only pixels associated with a current plate will be rotated,
then,
some past features that appears in the original PaleoMap landscape model
will be lost.

## Citation and data license

This model is the direct process of the Scotese and Wright (2018) model.
As such,
the original publication should be cited when the model is used.
Relevant papers are given in this file
and provided as bibTeX.

It is not required to cite this repository,
but if you do not include the model in the supplementary material
of your publication,
it might be a good idea to link this repository
and help others to replicate or re-use your analysis.

Data from PaleoMap project
(Scotese and Wrigth, 2018)
is distributed under the CC-BY 4.0 license,
hat can be found in the LICENSE file.

## References

Scotese, C.S.
(2016)
PALEOMAP PaleoAtlas for GPlates.
URL: <https://www.earthbyte.org/paleomap-paleoatlas-for-gplates/>.

Scotese, C.S., Wrigth, N.
(2018)
PALEOMAP Paleodigital elevation models (PaleoDEMs) for Phanerozoic.
URL: <https://www.earthbyte.org/paleodem-resource-scotese-and-wright-2018/>.
