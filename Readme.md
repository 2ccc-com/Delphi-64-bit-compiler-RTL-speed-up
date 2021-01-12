Delphi 64 bit compiler RTL speed up

Object Pascal wrappers from Intel Integrated Performance Primitives and Intel Threading Building Blocks royalty-free packages

Copyright 17 June 2019 Roberto Della Pasqua (updated 9 March 2020)

This folder contains:

- SeaMM.dll lock-free scalable allocator
- SeaRTL.dll simd enabled rtl subset routines
- SeaZIP.dll accelerated zlib deflate compression
- RDPMM64.pas wrapper for memory manager (put this unit as first unit clause in project source)
- RDPSimd64.pas wrapper for simd rtl
- RDPZlib64.pas wrapper for zlib compression
- RDPWebBroker64.pas utils to enhance webbroker
- License.txt for legal terms

If you want to enable zlib speed up into your WebBroker apps, add one line of code in AfterDispatch event:

- procedure TWebModule.WebModuleAfterDispatch(Sender: TObject; Request: TWebRequest; Response: TWebResponse; var Handled: Boolean); 
- begin 
-   Response.ZlibDeflate; 
- end;

The library is well tested, but if you found any trouble please notify me.

Thank you and best regards

Roberto Della Pasqua

www.dellapasqua.com
