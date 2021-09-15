---
description: Utilisation de textures compressées (Direct3D 9)
ms.assetid: 60892a8b-93f4-43ba-87ef-d5c7cc6fb8c6
title: Utilisation de textures compressées (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 643b0618043f12ff3e1a84b806c86edb780ad929
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413238"
---
# <a name="using-compressed-textures-direct3d-9"></a>Utilisation de textures compressées (Direct3D 9)

## <a name="determining-support-for-compressed-textures"></a>Détermination de la prise en charge des textures compressées

Pour tester l’adaptateur, spécifiez un format de pixel qui utilise DXT1, DXT2, DXT3, DXT4 ou DXT5. Si [**IDirect3D9 :: CheckDeviceFormat**](/windows/desktop/api) retourne D3D \_ OK, l’appareil peut créer une texture directement à partir d’une surface de texture compressée qui utilise ce format. Si c’est le cas, vous pouvez utiliser des surfaces de texture compressées directement avec Direct3D en appelant la méthode [**IDirect3DDevice9 :: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) . L’exemple de code suivant montre comment déterminer si l’adaptateur prend en charge un format de texture compressé.


```
BOOL IsCompressedTextureFormatOk( D3DFORMAT TextureFormat, 
                                  D3DFORMAT AdapterFormat ) 
{
    HRESULT hr = pD3D->CheckDeviceFormat( D3DADAPTER_DEFAULT,
                                          D3DDEVTYPE_HAL,
                                          AdapterFormat,
                                          0,
                                          D3DRTYPE_TEXTURE,
                                          TextureFormat);

    return SUCCEEDED( hr );
}
```



Si l’appareil ne prend pas en charge la texturation à partir des surfaces de texture compressées, vous pouvez toujours stocker des données de texture dans une surface formatée compressée, mais vous devez convertir toutes les textures compressées dans un format pris en charge avant de pouvoir les utiliser pour la texturation.

## <a name="creating-compressed-textures"></a>Création de textures compressées

Après avoir créé un appareil qui prend en charge un format de texture compressé sur l’adaptateur, vous pouvez créer une ressource de texture compressée. Appelez [**IDirect3DDevice9 :: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) et spécifiez un format de texture compressé pour le paramètre de format.

Avant de charger une image dans un objet texture, récupérez un pointeur vers la surface de texture en appelant la méthode [**IDirect3DTexture9 :: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) .

À présent, vous pouvez utiliser n’importe quelle fonction D3DXLoadSurfacexxx pour charger une image sur la surface Récupérée à l’aide de [**IDirect3DTexture9 :: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel). Ces fonctions gèrent la conversion vers et à partir des formats de texture compressés.

Vous pouvez créer et convertir des fichiers de texture compressée (DDS) à l’aide de l’éditeur de texture DirectX (Dxtex.exe) fourni avec le kit de développement logiciel (SDK) DirectX. Vous pouvez obtenir Dxtex.exe et en savoir plus à ce sujet à partir du kit de développement logiciel (SDK) DirectX. Pour plus d’informations sur DirectX SDK, consultez [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).

L’avantage de ce comportement est qu’une application peut copier le contenu d’une surface compressée dans un fichier sans calculer la quantité de stockage requise pour une surface d’une largeur et d’une hauteur particulières dans un format spécifique.

Le tableau suivant présente les cinq types de textures compressées. Pour plus d’informations sur la façon dont les données sont stockées, consultez [formats de texture compressés (Direct3D 9)](compressed-texture-formats.md). Vous avez uniquement besoin de ces informations si vous écrivez vos propres routines de compression.



| FOURCC | Description        | Alpha prémultiplié ? |
|--------|--------------------|----------------------|
| DXT1   | Alpha opaque/1 bits | N/A                  |
| DXT2   | Alpha explicite     | Oui                  |
| DXT3   | Alpha explicite     | Non                   |
| DXT4   | Alphabétique interpolé | Oui                  |
| DXT5   | Alphabétique interpolé | Non                   |



 

Lorsque vous transférez des données d’un format nonpremultiplied vers un format prémultiplié, Direct3D met à l’échelle les couleurs en fonction des valeurs alpha. Le transfert de données à partir d’un format prémultiplié vers un format nonpremultiplied n’est pas pris en charge. Si vous essayez de transférer des données à partir d’une source alpha prémultipliée vers une destination alpha nonpremultiplied, la méthode retourne D3DERR \_ INVALIDCALL. Si vous transférez des données à partir d’une source alpha prémultipliée vers une destination qui n’a pas de valeur alpha, les composants de couleur source, qui ont été mis à l’échelle par alpha, sont copiés comme c’est le cas.

## <a name="decompressing-compressed-texture-surfaces"></a>Décompression des surfaces de texture compressées

Comme pour la compression d’une surface de texture, la décompression d’une texture compressée est effectuée via les services de copie Direct3D.

Pour copier une surface de texture compressée dans une surface de texture non compressée, utilisez la fonction [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md). Cette fonction gère la compression vers et à partir des surfaces compressées et non compressées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources de texture compressées](compressed-texture-resources.md)
</dt> </dl>

 

 
