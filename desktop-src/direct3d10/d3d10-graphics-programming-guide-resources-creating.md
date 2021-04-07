---
description: La création de mémoires tampons requiert la définition des données que la mémoire tampon stockera, la fourniture des données d’initialisation et la configuration des indicateurs d’utilisation et de liaison appropriés. Pour créer des textures, consultez Création de ressources de texture (Direct3D 10).
ms.assetid: 9787b153-9301-4a0f-bd6f-21cc6f7fc650
title: Création de ressources de mémoire tampon (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d711265775c430728fbcffecd364f746580a566
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748516"
---
# <a name="creating-buffer-resources-direct3d-10"></a>Création de ressources de mémoire tampon (Direct3D 10)

La création de mémoires tampons requiert la définition des données que la mémoire tampon stockera, la fourniture des données d’initialisation et la configuration des indicateurs d’utilisation et de liaison appropriés. Pour créer des textures, consultez [création de ressources de texture (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).

-   [Créer une mémoire tampon de vertex](#create-a-vertex-buffer)
    -   [Créer une description de la mémoire tampon](#create-a-buffer-description)
    -   [Créer les données d’initialisation pour la mémoire tampon](#create-the-initialization-data-for-the-buffer)
    -   [Créer la mémoire tampon](#create-the-buffer)
-   [Créer un tampon d’index](#create-an-index-buffer)
-   [Créer une mémoire tampon constante](#create-a-constant-buffer)
-   [Rubriques connexes](#related-topics)

## <a name="create-a-vertex-buffer"></a>Créer une mémoire tampon de vertex

Les étapes de création d’une [mémoire tampon de vertex](d3d10-graphics-programming-guide-resources-types.md) sont les suivantes.

-   [Créer une description de la mémoire tampon](#create-a-buffer-description)
-   [Créer les données d’initialisation pour la mémoire tampon](#create-the-initialization-data-for-the-buffer)
-   [Créer la mémoire tampon](#create-the-buffer)

### <a name="create-a-buffer-description"></a>Créer une description de la mémoire tampon

Lors de la création d’une mémoire tampon de vertex, une description de mémoire tampon (voir [**D3D10 \_ buffer \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) est utilisée pour définir la manière dont les données sont organisées dans la mémoire tampon, comment le pipeline peut accéder à la mémoire tampon et comment la mémoire tampon sera utilisée.

L’exemple suivant montre comment créer une description de mémoire tampon pour un triangle unique avec des sommets qui contiennent des valeurs de position et de couleur.


```
struct SimpleVertex
{
    D3DXVECTOR3 Position;  
    D3DXVECTOR3 Color;  
};

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertex ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
```



Dans cet exemple, la description de la mémoire tampon est initialisée avec presque tous les paramètres par défaut pour [**l’utilisation**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), l’accès de l' [**UC**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) et les [**indicateurs divers**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag). Les autres paramètres concernent l' [**indicateur de liaison**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) qui identifie la ressource comme une mémoire tampon de vertex uniquement et la taille de la mémoire tampon.

Les indicateurs d’accès à l’utilisation et à l’UC sont importants pour les performances. Ces deux indicateurs déterminent la fréquence à laquelle une ressource est accédée, le type de mémoire dans lequel la ressource peut être chargée et le processeur dont elle a besoin pour accéder à la ressource. Utilisation par défaut cette ressource ne sera pas très souvent mise à jour. Le fait de définir un accès processeur à 0 signifie que le processeur n’a pas besoin de lire ou d’écrire la ressource. Pris en charge, cela signifie que le runtime peut charger la ressource dans la mémoire la plus performante pour le GPU puisque la ressource ne requiert pas d’accès au processeur.

Comme prévu, il existe un compromis entre les meilleures performances et l’accessibilité à tout moment par les deux processeurs. Par exemple, l’utilisation par défaut sans accès UC signifie que la ressource peut être mise à la disposition exclusive du GPU. Cela peut inclure le chargement de la ressource dans la mémoire qui n’est pas directement accessible par le processeur. La ressource ne peut être modifiée qu’avec [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource).

### <a name="create-the-initialization-data-for-the-buffer"></a>Créer les données d’initialisation pour la mémoire tampon

Une mémoire tampon n’est qu’une collection d’éléments et est présentée comme un tableau 1D. Par conséquent, le pas de la mémoire système et le pas de la tranche de mémoire système sont les mêmes ; taille de la déclaration de données de vertex. Une application peut fournir des données d’initialisation quand une mémoire tampon est créée à l’aide d’une description de sous- [**ressource**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data), qui contient un pointeur vers les données de ressource réelles et contient des informations sur la taille et la disposition de ces données.

Toute mémoire tampon créée avec une utilisation immuable ( [**voir \_ utilisation \_ de D3D10 immuable**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)) doit être initialisée au moment de la création. Les mémoires tampons qui utilisent l’un des autres indicateurs d’utilisation peuvent être mises à jour après l’initialisation à l’aide de [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)et [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource), ou en accédant à la mémoire sous-jacente à l’aide de la méthode [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) .

### <a name="create-the-buffer"></a>Créer la mémoire tampon

L’utilisation de la description de la mémoire tampon et des données d’initialisation (facultatives) appellent [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) pour créer une mémoire tampon de vertex. L’extrait de code suivant montre comment créer une mémoire tampon de vertex à partir d’un tableau de données de vertex déclarées par l’application.


```
struct SimpleVertexCombined
{
    D3DXVECTOR3 Pos;  
    D3DXVECTOR3 Col;  
};


ID3D10InputLayout* g_pVertexLayout = NULL;
ID3D10Buffer*      g_pVertexBuffer[2] = { NULL, NULL };
ID3D10Buffer*      g_pIndexBuffer = NULL;


SimpleVertexCombined verticesCombo[] =
{
    D3DXVECTOR3( 0.0f, 0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.0f, 0.5f ),
    D3DXVECTOR3( 0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.5f, 0.0f, 0.0f ),
    D3DXVECTOR3( -0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.5f, 0.0f ),
};


    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
    
    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = verticesCombo;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer[0] );
```



## <a name="create-an-index-buffer"></a>Créer un tampon d’index

La création d’un tampon d’index est très similaire à la création d’une mémoire tampon de vertex. avec deux différences. Une mémoire tampon d’index contient uniquement des données 16 bits ou 32 bits (à la place de la large gamme de formats disponibles pour une mémoire tampon de vertex. Un tampon d’index requiert également un indicateur de liaison d’index-buffer.

L’exemple suivant montre comment créer un tampon d’index à partir d’un tableau de données d’index.


```
ID3D10Buffer *g_pIndexBuffer = NULL;

    // Create indices
    unsigned int indices[] = { 0, 1, 2 };

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage           = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
    bufferDesc.BindFlags       = D3D10_BIND_INDEX_BUFFER;
    bufferDesc.CPUAccessFlags  = 0;
    bufferDesc.MiscFlags       = 0;

    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = indices;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
    if( FAILED( hr ) )
        return hr;
  
    g_pd3dDevice->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
```



## <a name="create-a-constant-buffer"></a>Créer une mémoire tampon constante

Direct3D 10 introduit une mémoire tampon constante. Une mémoire tampon constante, ou une mémoire tampon constante de nuanceur, est une mémoire tampon qui contient des constantes de nuanceur. Voici un exemple de création d’une mémoire tampon constante, extrait de l' [exemple HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).


```
ID3D10Buffer*   g_pConstantBuffer10 = NULL;

struct VS_CONSTANT_BUFFER
{
    D3DXMATRIX mWorldViewProj;      //mWorldViewProj will probably be global to all shaders in a project.
                                    //It's a good idea not to move it around between shaders.
    D3DXVECTOR4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                    //fTime may also be global to all shaders in a project.
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};

    D3D10_BUFFER_DESC cbDesc;
    cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
    cbDesc.Usage = D3D10_USAGE_DYNAMIC;
    cbDesc.BindFlags = D3D10_BIND_CONSTANT_BUFFER;
    cbDesc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
    cbDesc.MiscFlags = 0;
    hr = g_pd3dDevice->CreateBuffer( &cbDesc, NULL, &g_pConstantBuffer10 );
    if( FAILED( hr ) )
       return hr;

    g_pd3dDevice->VSSetConstantBuffers( 0, 1, g_pConstantBuffer10 );
```



Notez que, lors de l’utilisation de l’interface d' [**interface ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) , le processus de création, de liaison et de remise d’une mémoire tampon constante est géré par l’instance d' **interface ID3D10Effect** . Dans ce cas, il suffit de nescesary pour récupérer la variable de l’effet avec l’une des méthodes GetVariable comme [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) et mettre à jour la variable avec l’une des méthodes SetVariable comme [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix). Pour obtenir un exemple d’utilisation de l' **interface ID3D10Effect** pour gérer une mémoire tampon constante, consultez le [didacticiel 7 : mappage de texture et mémoires tampons constantes](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



