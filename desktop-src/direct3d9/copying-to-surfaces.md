---
description: 'Quand vous utilisez IDirect3DDevice9 :: UpdateSurface, transmettez un rectangle sur la surface source, ou utilisez la valeur NULL pour spécifier la surface entière.'
ms.assetid: 2219d037-8480-4c36-b04e-0c23406a2e7e
title: Copier dans des surfaces (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e28a8518f0792948af7aabda269fffe9679de2c6fc704ee93e2cf05381176b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989289"
---
# <a name="copying-to-surfaces-direct3d-9"></a>Copier dans des surfaces (Direct3D 9)

Quand vous utilisez [**IDirect3DDevice9 :: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface), transmettez un rectangle sur la surface source, ou utilisez la **valeur null** pour spécifier la surface entière. Vous pouvez également passer un point sur la surface de destination vers laquelle la position supérieure gauche du rectangle sur l’image source est copiée. Cette méthode ne prend pas en charge le découpage. L’opération échouera à moins que le rectangle source et le rectangle de destination correspondant soient entièrement contenus dans les surfaces source et de destination, respectivement. Cette méthode ne prend pas en charge la fusion alpha, les clés de couleur ou la conversion de format. Notez que les surfaces source et de destination doivent être distinctes.

Pour d’autres restrictions lors de l’utilisation de UpdateSurface, consultez [**IDirect3DDevice9 :: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).

Les méthodes suivantes sont également disponibles en C++/C pour copier des images sur une surface Direct3D.

-   [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md)
-   [**D3DXLoadSurfaceFromFileInMemory**](d3dxloadsurfacefromfileinmemory.md)
-   [**D3DXLoadSurfaceFromMemory**](d3dxloadsurfacefrommemory.md)
-   [**D3DXLoadSurfaceFromResource**](d3dxloadsurfacefromresource.md)
-   [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)
-   [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

## <a name="updatesurface-example"></a>Exemple UpdateSurface

L’exemple suivant copie deux rectangles de la surface source vers une surface de destination. Le premier rectangle est copié de (0, 0, 50, 50) sur la surface source vers le même emplacement sur la surface de destination, et le deuxième rectangle est copié de (50, 50, 100, 100) sur la surface source vers (150, 150, 200, 200) sur la surface de destination.


```
//The following assumptions are made:
// -d3dDevice is a valid Direct3DDevice9 object.
// -pSource and pDest are valid IDirect3DSurface9 pointers.

RECT  rcSource[] = {  0,  0,  50,  50,
                     50, 50, 100, 100 };
POINT ptDest[]   = {  0,  0, 150, 150 };

d3dDevice->UpdateSurface( pSource, rcSource, 2, pDest, ptDest);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Surfaces Direct3D](direct3d-surfaces.md)
</dt> <dt>

[**IDirect3DDevice9::StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> </dl>

 

 
