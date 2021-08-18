---
title: Comment créer une mémoire tampon de vertex
description: Cette rubrique montre comment initialiser une mémoire tampon de vertex statique, autrement dit, une mémoire tampon de vertex qui ne change pas.
ms.assetid: 584a39d1-7629-429a-b451-64b1432cb48f
keywords:
- mémoire tampon de vertex, création
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f919646dfd4e8f714b925606f342db586ff2b8f09690c58698b7dab2635159e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496899"
---
# <a name="how-to-create-a-vertex-buffer"></a>Comment : créer une mémoire tampon de vertex

Les [mémoires tampons de vertex](overviews-direct3d-11-resources-buffers-intro.md) contiennent des données par vertex. Cette rubrique montre comment initialiser une [mémoire tampon de vertex](overviews-direct3d-11-resources-buffers-intro.md)statique, autrement dit, une mémoire tampon de vertex qui ne change pas. Pour obtenir de l’aide sur l’initialisation d’une mémoire tampon non statique, consultez la section [Notes](#remarks) .

**Pour initialiser une mémoire tampon de vertex statique**

1.  Définissez une structure qui décrit un vertex. Par exemple, si vos données de vertex contiennent des données de position et des données de couleur, votre structure aurait un vecteur qui décrit la position et un autre qui décrit la couleur.
2.  Allouez de la mémoire (à l’aide de malloc ou New) pour la structure que vous avez définie à l’étape 1. Remplissez cette mémoire tampon avec les données de vertex réelles qui décrivent votre géométrie.
3.  Créez une description de la mémoire tampon en remplissant une structure [**\_ \_ desc de tampon d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) . Transmettez l' \_ indicateur de tampon de vertex de liaison d3d11 \_ \_ au membre **BindFlags** et transmettez la taille de la structure de l’étape 1 au membre **ByteWidth** .
4.  Créez une description des données de sous-ressource en remplissant une structure de [**\_ \_ données**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) de sous-ressource d3d11. Le membre **pSysMem** de la structure de données de sous- [**\_ ressources \_ d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) doit pointer directement vers les données de ressources créées à l’étape 2.
5.  Appelez [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) lors du passage de la structure DESC de la [**\_ \_ mémoire tampon d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , de la structure de données de la sous- [**\_ ressource \_ d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) et de l’adresse d’un pointeur vers l’interface [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) à initialiser.

L’exemple de code suivant montre comment créer une mémoire tampon de vertex. Cet exemple suppose que **g \_ pd3dDevice** est un objet [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) valide.


```
ID3D11Buffer*      g_pVertexBuffer;

// Define the data-type that
// describes a vertex.
struct SimpleVertexCombined
{
    XMFLOAT3 Pos;  
    XMFLOAT3 Col;  
};

// Supply the actual vertex data.
SimpleVertexCombined verticesCombo[] =
{
    XMFLOAT3( 0.0f, 0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.0f, 0.5f ),
    XMFLOAT3( 0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.5f, 0.0f, 0.0f ),
    XMFLOAT3( -0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.5f, 0.0f ),
};

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage            = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
bufferDesc.BindFlags        = D3D11_BIND_VERTEX_BUFFER;
bufferDesc.CPUAccessFlags   = 0;
bufferDesc.MiscFlags        = 0;

// Fill in the subresource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = verticesCombo;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the vertex buffer.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer );
    
```



## <a name="remarks"></a>Remarques

Voici quelques méthodes permettant d’initialiser une mémoire tampon de vertex qui change au fil du temps.

1.  Créez une deuxième mémoire tampon avec l' [**\_ utilisation \_ intermédiaire de d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage); remplissez la deuxième mémoire tampon à l’aide de [**ID3D11DeviceContext :: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext :: DEMAPPAGE**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap); utilisez [**ID3D11DeviceContext :: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) pour copier à partir de la mémoire tampon de mise en lots vers la mémoire tampon par défaut.
2.  Utilisez [**ID3D11DeviceContext :: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) pour copier des données à partir de la mémoire.
3.  Créez un tampon avec [**\_ l’utilisation \_ dynamique de d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)et remplissez-le avec [**ID3D11DeviceContext :: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext :: DEMAPPAGE**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) (en utilisant les indicateurs Discard et NoOverwrite de manière appropriée).

\#1 et \# 2 sont utiles pour le contenu qui change moins d’une fois par frame. En général, les lectures GPU sont rapides et les mises à jour de l’UC sont plus lentes.

\#3 est utile pour le contenu qui change plus d’une fois par frame. En général, les lectures GPU sont plus lentes, mais les mises à jour de l’UC sont plus rapides.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




