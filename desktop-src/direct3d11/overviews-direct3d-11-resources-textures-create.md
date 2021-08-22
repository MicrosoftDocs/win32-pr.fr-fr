---
title: Comment créer une texture
description: Cette rubrique montre comment créer une texture.
ms.assetid: dfe88635-b2c2-48f8-a21e-cce845b518fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6539caec121f301dd89906f7cd78134d3b7cd79083c0d185af63d488ef1648eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565549"
---
# <a name="how-to-create-a-texture"></a>Comment : créer une texture

La façon la plus simple de créer une texture est de décrire ses propriétés et d’appeler l’API de création de texture. Cette rubrique montre comment créer une texture.

**Pour créer une texture**

1.  Remplissez une structure [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) avec une description des paramètres de texture.
2.  Créez la texture en appelant [**ID3D11Device :: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) avec la description de la texture.

Cet exemple crée une texture 256 x 256, avec [**utilisation dynamique**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), pour une utilisation en tant que [**ressource de nuanceur**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) avec [**accès en écriture**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)de l’UC.


```
D3D11_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D11_USAGE_DYNAMIC;
desc.BindFlags = D3D11_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
desc.MiscFlags = 0;

ID3D11Device *pd3dDevice; // Don't forget to initialize this
ID3D11Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Textures](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




