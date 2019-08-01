# New Project setup:

Do not modify the relative directory structure of these samples. In
particular, for each project sample, the Common folder must be obtained
from it via "../../Common".

## Debug libraries:

d3d11.lib;d3dx11d.lib;D3DCompiler.lib;Effects11d.lib;dxerr.lib;dxgi.lib;dxguid.lib;%(AdditionalDependencies)

## Release libraries:

d3d11.lib;d3dx11.lib;D3DCompiler.lib;Effects11.lib;dxerr.lib;dxgi.lib;dxguid.lib;%(AdditionalDependencies)

## C/C++ Additional Include Directories:

1)  Path to DirectX Header files.
2)  ../../Common (or Absolute Path to Common)

## Linker Additional Library Directories:

1)  Path to DirectX Library files.
2)  ../../Common (or Absolute Path to Common)

## FXC Call

1)  Debug mode: fxc /Fc /Od /Zi /T fx\_5\_0 /Fo
    "%(RelativeDir)%(Filename).fxo" "%(FullPath)"
2)  Release mode: fxc /T fx\_5\_0 /Fo "%(RelativeDir)%(Filename).fxo"
    "%(FullPath)"
3)  Debug Description: fxc compile for debug: %(FullPath)
4)  Release Description: fxc compile for release: %(FullPath)

Outputs: %(RelativeDir)%(Filename).fxo