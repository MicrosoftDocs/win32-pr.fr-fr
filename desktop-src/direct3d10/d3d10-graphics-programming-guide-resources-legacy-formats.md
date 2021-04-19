---
description: Ce tableau répertorie les formats Direct3D 9 qui peuvent être mappés à un format Direct3D 10.
ms.assetid: 07c9b827-6e2e-4599-b48a-f726484b643d
title: 'Formats hérités : mapper les formats Direct3D 9 à Direct3D 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230b8ed17984d47a3b57ce287aa9b434a2b92aae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544203"
---
# <a name="legacy-formats-map-direct3d-9-formats-to-direct3d-10"></a>Formats hérités : mapper les formats Direct3D 9 à Direct3D 10

Ce tableau répertorie les formats Direct3D 9 qui peuvent être mappés à un format Direct3D 10. Les formats Direct3D 10 se sont diverged des formats Direct3D 9 afin que les formats de vertex et de texture puissent être fusionnés pour permettre l’activation des applications Cross-endian.



| Format de texture/vertex/d’index Direct3D 9 | Format Direct3D 10 équivalent                                        |
|----------------------------------------|----------------------------------------------------------------------|
| D3DFMT \_ inconnu                        | \_format dxgi \_ inconnu                                                |
| D3DFMT \_ R8G8B8                         | Non disponible                                                        |
| D3DFMT \_ A8R8G8B8                       | DXGI \_ format \_ B8G8R8A8 \_ UNORM (DXGI 1,1)                             |
| D3DFMT \_ X8R8G8B8                       | DXGI \_ format \_ B8G8R8X8 \_ UNORM (DXGI 1,1)                             |
| D3DFMT \_ R5G6B5                         | DXGI \_ format \_ B5G6R5 \_ UNORM (DXGI 1,2)                               |
| D3DFMT \_ X1R5G5B5                       | Non disponible                                                        |
| D3DFMT \_ A1R5G5B5                       | DXGI \_ format \_ B5G5R5A1 \_ UNORM (DXGI 1,2)                             |
| D3DFMT \_ A4R4G4B4                       | DXGI \_ format \_ B4G4R4A4 \_ UNORM (DXGI 1,2)                             |
| D3DFMT \_ R3G3B2                         | Non disponible                                                        |
| D3DFMT \_ a8                             | \_Format dxgi \_ a8 \_ UNORM                                              |
| D3DFMT \_ A8R3G3B2                       | Non disponible                                                        |
| D3DFMT \_ X4R4G4B4                       | Non disponible                                                        |
| D3DFMT \_ A2B10G10R10                    | DXGI \_ format \_ R10G10B10A2                                            |
| D3DFMT \_ A8B8G8R8                       | DXGI \_ format \_ R8G8B8A8 \_ UNORM ou dxgi \_ R8G8B8A8 \_ \_ UNORM \_ sRGB |
| D3DFMT \_ X8B8G8R8                       | Non disponible                                                        |
| D3DFMT \_ G16R16                         | DXGI \_ format \_ R16G16 \_ UNORM                                          |
| D3DFMT \_ A2R10G10B10                    | Non disponible                                                        |
| D3DFMT \_ A16B16G16R16                   | DXGI \_ format \_ R16G16B16A16 \_ UNORM                                    |
| D3DFMT \_ A8P8                           | Non disponible                                                        |
| D3DFMT \_ P8                             | Non disponible                                                        |
| D3DFMT \_ N8                             | \_Format dxgi \_ R8 \_ UNORM ¹                                            |
| D3DFMT \_ A8L8                           | Non disponible                                                        |
| D3DFMT \_ A4L4                           | Non disponible                                                        |
| D3DFMT \_ V8U8                           | \_Format dxgi \_ R8G8 \_ ronfler                                            |
| D3DFMT \_ L6V5U5                         | Non disponible                                                        |
| D3DFMT \_ X8L8V8U8                       | Non disponible                                                        |
| D3DFMT \_ Q8W8V8U8                       | \_Format dxgi \_ R8G8B8A8 \_ ronfler                                        |
| D3DFMT \_ V16U16                         | \_Format dxgi \_ R16G16 \_ ronfler                                          |
| D3DFMT \_ W11V11U10                      | Non disponible                                                        |
| D3DFMT \_ A2W10V10U10                    | Non disponible                                                        |
| D3DFMT \_ UYVY                           | Non disponible                                                        |
| D3DFMT \_ R8G8 \_ B8G8                     | DXGI \_ format \_ G8R8 \_ G8B8 \_ UNORM ²                                    |
| D3DFMT \_ YUY2                           | Non disponible                                                        |
| D3DFMT \_ G8R8 \_ G8B8                     | DXGI \_ format \_ R8G8 \_ B8G8 \_ UNORM ²                                    |
| D3DFMT \_ DXT1                           | DXGI \_ format \_ BC1 \_ UNORM ou dxgi \_ BC1 \_ \_ UNORM \_ sRGB           |
| D3DFMT \_ DXT2                           | DXGI \_ format \_ BC2 \_ UNORM ou dxgi \_ format \_ BC2 \_ UNORM \_ sRGB ³         |
| D3DFMT \_ DXT3                           | DXGI \_ format \_ BC2 \_ UNORM ou dxgi \_ BC2 \_ \_ UNORM \_ sRGB           |
| D3DFMT \_ DXT4                           | DXGI \_ format \_ BC3 \_ UNORM ou dxgi \_ format \_ BC3 \_ UNORM \_ sRGB ³         |
| D3DFMT \_ DXT5                           | DXGI \_ format \_ BC3 \_ UNORM ou dxgi \_ BC3 \_ \_ UNORM \_ sRGB           |
| D3DFMT \_ D16 et D3DFMT \_ D16 \_ verrouillable  | DXGI \_ format \_ D16 \_ UNORM                                             |
| D3DFMT \_ d32                            | Non disponible                                                        |
| D3DFMT \_ D15S1                          | Non disponible                                                        |
| D3DFMT \_ D24S8                          | Non disponible                                                        |
| D3DFMT \_ D24X8                          | Non disponible                                                        |
| D3DFMT \_ D24X4S4                        | Non disponible                                                        |
| D3DFMT \_ D16                            | DXGI \_ format \_ D16 \_ UNORM                                             |
| D3DFMT \_ D32F \_ verrouillable                 | DXGI \_ format \_ d32 \_ float                                             |
| D3DFMT \_ D24FS8                         | Non disponible                                                        |
| D3DFMT \_ S1D15                          | Non disponible                                                        |
| D3DFMT \_ S8D24                          | DXGI \_ format \_ D24 \_ UNORM \_ S8 \_ uint                                   |
| D3DFMT \_ X8D24                          | Non disponible                                                        |
| D3DFMT \_ X4S4D24                        | Non disponible                                                        |
| D3DFMT \_ L16                            | DXGI \_ format \_ R16 \_ UNORM ¹                                           |
| D3DFMT \_ INDEX16                        | DXGI \_ format \_ R16 \_ uint                                              |
| D3DFMT \_ INDEX32                        | DXGI \_ format \_ R32 \_ uint                                              |
| D3DFMT \_ Q16W16V16U16                   | \_Format dxgi \_ R16G16B16A16 \_ ronfler                                    |
| D3DFMT \_ MULTI2 \_ ARGB8                  | Non disponible                                                        |
| D3DFMT \_ R16F                           | DXGI \_ format \_ R16 \_ float                                             |
| D3DFMT \_ G16R16F                        | DXGI \_ format \_ R16G16 \_ float                                          |
| D3DFMT \_ A16B16G16R16F                  | DXGI \_ format \_ R16G16B16A16 \_ float                                    |
| D3DFMT \_ R32F                           | DXGI \_ format \_ R32 \_ float                                             |
| D3DFMT \_ G32R32F                        | DXGI \_ format \_ R32G32 \_ float                                          |
| D3DFMT \_ A32B32G32R32F                  | DXGI \_ format \_ R32G32B32A32 \_ float                                    |
| D3DFMT \_ CxV8U8                         | Non disponible                                                        |
| D3DDECLTYPE \_ FLOAT1                    | DXGI \_ format \_ R32 \_ float                                             |
| D3DDECLTYPE \_ FLOAT2                    | DXGI \_ format \_ R32G32 \_ float                                          |
| D3DDECLTYPE \_ FLOAT3                    | DXGI \_ format \_ R32G32B32 \_ float                                       |
| D3DDECLTYPE \_ float4                    | DXGI \_ format \_ R32G32B32A32 \_ float                                    |
| D3DDECLTYPED3DCOLOR                    | Non disponible                                                        |
| D3DDECLTYPE \_ UBYTE4                    | DXGI \_ format \_ R8G8B8A8 \_ uint ⁴                                       |
| D3DDECLTYPE \_ SHORT2                    | \_Format dxgi \_ R16G16 \_ Saint-                                           |
| D3DDECLTYPE \_ SHORT4                    | \_Format dxgi \_ R16G16B16A16 \_ Saint-                                     |
| D3DDECLTYPE \_ UBYTE4N                   | DXGI \_ format \_ R8G8B8A8 \_ UNORM                                        |
| D3DDECLTYPE \_ SHORT2N                   | \_Format dxgi \_ R16G16 \_ ronfler                                          |
| D3DDECLTYPE \_ SHORT4N                   | \_Format dxgi \_ R16G16B16A16 \_ ronfler                                    |
| D3DDECLTYPE \_ USHORT2N                  | DXGI \_ format \_ R16G16 \_ UNORM                                          |
| D3DDECLTYPE \_ USHORT4N                  | DXGI \_ format \_ R16G16B16A16 \_ UNORM                                    |
| D3DDECLTYPE \_ UDEC3                     | Non disponible                                                        |
| D3DDECLTYPE \_ DEC3N                     | Non disponible                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2                | DXGI \_ format \_ R16G16 \_ float                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4                | DXGI \_ format \_ R16G16B16A16 \_ float                                    |



 

1.  Utilisez. r Swizzle dans un nuanceur pour dupliquer le rouge sur d’autres composants pour obtenir le comportement Direct3D 9.
2.  Dans Direct3D 9, les données ont été mises à l’échelle par 255.0 f, ce qui peut être fait dans le code du nuanceur à la place.
3.  DXT2 et DXT3 sont les mêmes du point de vue de l’API ; DXT4 et DXT5 sont les mêmes du point de vue de l’API. La seule différence était prémultipliée alpha, qui peut être suivie par une application et n’a pas besoin d’un format distinct.
4.  Un nuanceur obtient des valeurs UINT, mais si les valeurs float de style intégral Direct3D 9 (0.0 f, 1.0 f... 255. f) sont nécessaires, UINT peut être converti en float32 dans un nuanceur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



