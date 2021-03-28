---
title: Comment créer un tampon d’index
description: Cette rubrique montre comment initialiser un tampon d’index en vue de sa restitution.
ms.assetid: 4b33d32a-27fd-4652-87ac-3b7268881f89
keywords:
- mémoire tampon d’index, création
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c4c99639748876a5f5fd84e546aaf299885c76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197092"
---
# <a name="how-to-create-an-index-buffer"></a>Comment : créer un tampon d’index

Les [tampons d’index](overviews-direct3d-11-resources-buffers-intro.md) contiennent des données d’index. Cette rubrique montre comment initialiser un [tampon d’index](overviews-direct3d-11-resources-buffers-intro.md) en vue de sa restitution.

**Pour initialiser un tampon d’index**

1.  Créez une mémoire tampon qui contient vos informations d’index.
2.  Créez une description de la mémoire tampon en remplissant une structure [**\_ \_ desc de tampon d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) . Transmettez l' \_ indicateur de tampon d’index de liaison d3d11 \_ \_ au membre **BindFlags** et transmettez la taille de la mémoire tampon en octets au membre **ByteWidth** .
3.  Créez une description des données de sous-ressource en remplissant une structure de [**\_ \_ données**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) de sous-ressource d3d11. Le membre **pSysMem** doit pointer directement vers les données d’index créées à l’étape 1.
4.  Appelez [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) lors du passage de la structure DESC de la [**\_ \_ mémoire tampon d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , de la structure de données de la sous- [**\_ ressource \_ d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) et de l’adresse d’un pointeur vers l’interface [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) à initialiser.

L’exemple de code suivant montre comment créer une mémoire tampon d’index. Cet exemple suppose que


```
g_pd3dDevice
```



est un objet [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) valide et


```
g_pd3dContext
```



est un objet [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) valide.


```
ID3D11Buffer *g_pIndexBuffer = NULL;

// Create indices.
unsigned int indices[] = { 0, 1, 2 };

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage           = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
bufferDesc.BindFlags       = D3D11_BIND_INDEX_BUFFER;
bufferDesc.CPUAccessFlags  = 0;
bufferDesc.MiscFlags       = 0;

// Define the resource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = indices;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the buffer with the device.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
if( FAILED( hr ) )
    return hr;

// Set the buffer.
g_pd3dContext->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
    
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




