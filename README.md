# UCL NRV2d decompressor for PDP-11
NRV2d decompression algorithm implementation for PDP-11 compatible microprocessor.

**IMPORTANT**. This code does not accept original packed byte sequences's final marker.
The compression subroutine `ucl_nrv_99_compress` must be modificated to emit short final code prefix:<br>
UCL version: 1.03, file `src\n2_99.ch`, line #605, original:<br>
`code_prefix_ss12(c, UCL_UINT32_C(0x1000000));`<br>
Should be:<br>
`code_prefix_ss12(c, UCL_UINT32_C(0x100));`

You can use `n2dpack` utility in `bin` folder to create packed streams.

### See also

* [NRV2d-i80](https://github.com/usr38259/nrv2d-i80) - NRV2d decompression for Intel 8080
* [n2dpack](https://github.com/usr38259/nrv2d-i80/tree/main/src) - n2dpack utility
