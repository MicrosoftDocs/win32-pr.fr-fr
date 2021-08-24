---
title: Utilisation des ressources dynamiques
description: Vous créez et utilisez des ressources dynamiques lorsque votre application doit modifier des données dans ces ressources. Vous pouvez créer des textures et des mémoires tampons pour une utilisation dynamique.
ms.assetid: E73EA4B0-BD14-430C-89CA-4CFCF92C7548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d85933490d1e3bbbd09cc83720651c4fd634012f8e5aa70562396e87c096ebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633099"
---
# <a name="how-to-use-dynamic-resources"></a>Comment : utiliser des ressources dynamiques

**API importantes**

-   [**ID3D11DeviceContext :: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
-   [**ID3D11DeviceContext :: DEMAPPAGE**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)
-   [**Utilisation de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)

Vous créez et utilisez des ressources dynamiques lorsque votre application doit modifier des données dans ces ressources. Vous pouvez créer des textures et des mémoires tampons pour une utilisation dynamique.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Comment : créer une texture](overviews-direct3d-11-resources-textures-create.md)
-   [Comment : initialiser une texture par programmation](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
-   [Comment : créer une mémoire tampon constante](overviews-direct3d-11-resources-buffers-constant-how-to.md)

### <a name="prerequisites"></a>Prérequis

Nous partons du principe que vous êtes familiarisé avec C++. Vous avez également besoin d’une expérience de base dans les concepts de programmation graphique.

## <a name="instructions"></a>Instructions

### <a name="step-1-specify-dynamic-usage"></a>Étape 1 : spécifier l’utilisation dynamique

Si vous souhaitez que votre application puisse apporter des modifications aux ressources, vous devez spécifier ces ressources comme étant dynamiques et accessibles en écriture au moment de leur création.

**Pour spécifier l’utilisation dynamique**

1.  Spécifiez l’utilisation des ressources comme dynamique. Par exemple, spécifiez la valeur [**\_ \_ dynamique d’utilisation d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) dans le membre **usage** de la description de la [**\_ \_ mémoire tampon d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) pour un vertex ou une mémoire tampon constante et spécifiez la valeur **\_ \_ dynamique d’utilisation d3d11** dans le membre **usage** de [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) pour une texture 2D.
2.  Spécifiez la ressource comme accessible en écriture. Par exemple, spécifiez la valeur d' [**écriture d’accès au \_ processeur \_ \_ d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) dans le membre **cpuaccessflags a** de la description de la [**\_ mémoire tampon \_ d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) ou [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc).
3.  Transmettez la description de la ressource à la fonction de création. Par exemple, transmettez l’adresse de la description de la [**\_ mémoire tampon \_ d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) à [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) et transmettez l’adresse de [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) à [**ID3D11Device :: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).

Voici un exemple de création d’une mémoire tampon de vertex dynamique :


```C++
    // Create a vertex buffer for a triangle.

    float2 triangleVertices[] =
    {
        float2(-0.5f, -0.5f),
        float2(0.0f, 0.5f),
        float2(0.5f, -0.5f),
    };

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(float2)* ARRAYSIZE(triangleVertices);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;
    vertexBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
    vertexBufferDesc.MiscFlags = 0;
    vertexBufferDesc.StructureByteStride = 0;

    D3D11_SUBRESOURCE_DATA vertexBufferData;
    vertexBufferData.pSysMem = triangleVertices;
    vertexBufferData.SysMemPitch = 0;
    vertexBufferData.SysMemSlicePitch = 0;

    DX::ThrowIfFailed(
        m_d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        &vertexBufferData,
        &vertexBuffer2
        )
        );

```



### <a name="step-2-change-a-dynamic-resource"></a>Étape 2 : modifier une ressource dynamique

Si vous avez spécifié une ressource comme dynamique et accessible en écriture au moment de sa création, vous pouvez apporter des modifications ultérieurement à cette ressource.

**Pour modifier des données dans une ressource dynamique**

1.  Configurez les nouvelles données pour la ressource. Déclarez une variable de type de sous- [**\_ \_ ressource mappée d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) et initialisez-la sur zéro. Vous utiliserez cette variable pour modifier la ressource.
2.  Désactivez l’accès à l’unité de traitement graphique (GPU) aux données que vous souhaitez modifier et récupérez un pointeur vers la mémoire qui contient les données. Pour atteindre ce pointeur, transmettez [**d3d11 \_ Map \_ Write \_ ignore**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) au paramètre *maptype* lorsque vous appelez [**ID3D11DeviceContext :: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map). Définissez ce pointeur sur l’adresse de la variable de sous- [**\_ \_ ressource mappée d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) à partir de l’étape précédente.
3.  Écrivez les nouvelles données dans la mémoire.
4.  Appelez [**ID3D11DeviceContext :: DEMAPPAGE**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) pour réactiver l’accès GPU aux données lorsque vous avez terminé d’écrire les nouvelles données.

Voici un exemple de modification d’une mémoire tampon de vertex dynamique :


```C++
// This might get called as the result of a click event to double the size of the triangle.
void TriangleRenderer::MapDoubleVertices()
{
    D3D11_MAPPED_SUBRESOURCE mappedResource;
    ZeroMemory(&mappedResource, sizeof(D3D11_MAPPED_SUBRESOURCE));
    float2 vertices[] =
    {
        float2(-1.0f, -1.0f),
        float2(0.0f, 1.0f),
        float2(1.0f, -1.0f),
    };
    //  Disable GPU access to the vertex buffer data.
    auto m_d3dContext = m_deviceResources->GetD3DDeviceContext();
    m_d3dContext->Map(vertexBuffer2.Get(), 0, D3D11_MAP_WRITE_DISCARD, 0, &mappedResource);
    //  Update the vertex buffer here.
    memcpy(mappedResource.pData, vertices, sizeof(vertices));
    //  Reenable GPU access to the vertex buffer data.
    m_d3dContext->Unmap(vertexBuffer2.Get(), 0);
}
```



## <a name="remarks"></a>Remarques

### <a name="using-dynamic-textures"></a>Utilisation de textures dynamiques

Nous vous recommandons de ne créer qu’une seule texture dynamique par format et éventuellement par taille. Nous vous déconseillons de créer des des mipmaps, des cubes et des volumes dynamiques en raison de la surcharge supplémentaire dans le mappage de chaque niveau. Pour des mipmaps, vous pouvez spécifier [**d3d11 \_ mapper l' \_ écriture \_ ignore**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) uniquement au niveau supérieur. Tous les niveaux sont ignorés en mappant simplement le niveau supérieur. Ce comportement est le même pour les volumes et les cubes. Pour les cubes, le niveau supérieur et le visage 0 sont mappés.

### <a name="using-dynamic-buffers"></a>Utilisation de mémoires tampons dynamiques

Lorsque vous appelez [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) sur une mémoire tampon de vertex statique alors que le GPU utilise la mémoire tampon, vous bénéficiez d’une baisse significative des performances. Dans ce cas, **Map** doit attendre la fin de la lecture des données de vertex ou d’index à partir de la mémoire tampon avant que **Map** puisse revenir à l’application appelante, ce qui entraîne un délai important. L’appel de **Map** , puis le rendu à partir d’une mémoire tampon statique plusieurs fois par trame, empêche également le GPU de mettre en mémoire tampon les commandes de rendu, car il doit terminer les commandes avant de retourner le pointeur de carte. Sans commandes mises en mémoire tampon, le GPU reste inactif jusqu’à ce que l’application ait fini de remplir la mémoire tampon de vertex ou le tampon d’index et envoie une commande de rendu.

Idéalement, les données de vertex ou d’index ne changeraient jamais, mais ce n’est pas toujours possible. Dans de nombreux cas, l’application doit modifier des données de vertex ou d’index à chaque trame, voire plusieurs fois par frame. Dans ce cas, nous vous recommandons de créer le vertex ou le tampon d’index avec [**\_ l’utilisation \_ dynamique de d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). Cet indicateur d’utilisation entraîne l’optimisation du runtime pour les opérations de mappage fréquentes. **D3d11 \_ L’utilisation \_ dynamique** est utile uniquement lorsque la mémoire tampon est mappée fréquemment ; Si les données doivent rester constantes, placez-les dans un tampon statique ou un sommet d’index.

Pour bénéficier d’une amélioration des performances lorsque vous utilisez des mémoires tampons de vertex dynamiques, votre application doit appeler [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) avec les valeurs de [**\_ mappage de d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) appropriées. [**D3d11 \_ Le mappage d' \_ écriture \_ ignore**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indique que l’application n’a pas besoin de conserver les anciennes données de vertex ou d’index dans la mémoire tampon. Si le GPU utilise toujours la mémoire tampon quand vous appelez **Map** avec **d3d11 \_ Map \_ Write \_ ignore**, le runtime retourne un pointeur vers une nouvelle région de mémoire au lieu des anciennes données de mémoire tampon. Cela permet au GPU de continuer à utiliser les anciennes données pendant que l’application place les données dans la nouvelle mémoire tampon. Aucune gestion supplémentaire de la mémoire n’est nécessaire dans l’application. l’ancienne mémoire tampon est réutilisée ou détruite automatiquement lorsque le GPU en a terminé avec celle-ci.

> [!Note]  
> Lorsque vous mappez une mémoire tampon avec l' [**écriture de d3d11 \_ Map \_ \_ ignorée**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map), le runtime ignore toujours l’intégralité de la mémoire tampon. Vous ne pouvez pas conserver les informations dans les zones non mappées de la mémoire tampon en spécifiant un champ d’offset différent de zéro ou une taille limitée.

 

Dans certains cas, la quantité de données dont l’application a besoin pour stocker par carte est petite, par exemple l’ajout de quatre sommets pour le rendu d’un sprite. [**D3d11 \_ MAPPER l' \_ écriture \_ sans \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) remplacement indique que l’application ne remplacera pas les données déjà en cours d’utilisation dans la mémoire tampon dynamique. L’appel [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) retourne un pointeur vers les anciennes données, ce qui permet à l’application d’ajouter de nouvelles données dans les régions inutilisées du vertex ou de la mémoire tampon d’index. L’application ne doit pas modifier les vertex ou les index utilisés dans une opération de dessin, car ils peuvent toujours être utilisés par le GPU. Nous vous recommandons de faire en sorte que l’application utilise ensuite l' [**\_ écriture d3d11 map \_ \_ ignorée**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) une fois que la mémoire tampon dynamique est pleine pour recevoir une nouvelle région de mémoire, qui ignore les anciennes données de vertex ou d’index une fois l’exécution du GPU terminée.

Le mécanisme de requête asynchrone est utile pour déterminer si les vertex sont toujours utilisés par le GPU. Émettez une requête de [**type \_ \_ événement de requête d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) après le dernier appel de dessin qui utilise les vertex. Les vertex ne sont plus utilisés quand [**ID3D11DeviceContext :: GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) retourne S \_ OK. Lorsque vous mappez une mémoire tampon avec [**d3d11 \_ carte d' \_ écriture \_ ignorée**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) ou aucune valeur de mappage, vous avez toujours la garantie que les vertex sont correctement synchronisés avec le GPU. Toutefois, lorsque vous mappez sans valeurs cartographiques, vous subissez la pénalité de performance décrite précédemment.

> [!Note]  
> le runtime Direct3D 11,1, disponible à partir de Windows 8, permet de mapper des mémoires tampons constantes dynamiques et des vues des ressources de nuanceur (SRVs) de mémoires tampons dynamiques avec la [**carte de D3D11 \_ \_ sans remplacer l’écriture \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map). Les runtimes Direct3D 11 et versions antérieures limitent le mappage de mise à jour partielle non-remplacement aux mémoires tampons de vertex ou d’index. Pour déterminer si un périphérique Direct3D prend en charge ces fonctionnalités, appelez [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) avec les [**options de d3d11 de fonctionnalités de d3d11 \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature). **CheckFeatureSupport** remplit les membres d’une structure d' [**\_ \_ \_ \_ options d3d11 des données de la fonctionnalité d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) avec les fonctionnalités de l’appareil. Les membres pertinents ici sont **MapNoOverwriteOnDynamicConstantBuffer** et **MapNoOverwriteOnDynamicBufferSRV**.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




