---
title: Prise en main avec l’étape de Input-Assembler
description: Quelques étapes sont nécessaires pour initialiser l’étape de l’assembleur d’entrée (IA).
ms.assetid: 84c0ca29-2356-4b7f-98ee-ff1758edc540
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513e7452eebf157a80d4239127bf1d04a014375f7bbaf06e4f5814199d7ba053
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858209"
---
# <a name="getting-started-with-the-input-assembler-stage"></a>Prise en main avec l’étape de Input-Assembler

Quelques étapes sont nécessaires pour initialiser l’étape de l’assembleur d’entrée (IA). Par exemple, vous devez créer des ressources de mémoire tampon avec les données de vertex dont le pipeline a besoin, indiquer à l’étape IA où se trouvent les mémoires tampons et le type de données qu’elles contiennent, et spécifier le type de primitives à assembler à partir des données.

Les étapes de base nécessaires à la configuration de l’étape IA, présentées dans le tableau suivant, sont traitées dans cette rubrique.



| Étape                                                                                    | Description                                                                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Créer des mémoires tampons d’entrée](#create-input-buffers)                                           | Créer et initialiser des mémoires tampons d’entrée avec des données de vertex d’entrée.                                           |
| [Créer l’objet Input-Layout](#create-the-input-layout-object)                       | Définissez la façon dont les données de la mémoire tampon du vertex sont diffusées dans l’étape IA à l’aide d’un objet de disposition d’entrée. |
| [Lier des objets à l’étape Input-Assembler](#bind-objects-to-the-input-assembler-stage) | Liez les objets créés (mémoires tampons d’entrée et objet de disposition d’entrée) à l’étape IA.                 |
| [Spécifiez le type primitif](#specify-the-primitive-type)                               | Identifiez la manière dont les vertex seront assemblés en Primitives.                                          |
| [Méthodes Call Draw](#call-draw-methods)                                                 | Envoyez les données liées à l’étape IA via le pipeline.                                             |



 

Une fois que vous avez compris ces étapes, passez à [l’utilisation des valeurs System-Generated](d3d10-graphics-programming-guide-input-assembler-stage-using.md).

## <a name="create-input-buffers"></a>Créer des mémoires tampons d’entrée

Il existe deux types de mémoires tampons d’entrée : les tampons de [vertex](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) et les mémoires tampons d’index. Les mémoires tampons de vertex fournissent des données de vertex à l’étape IA. Les mémoires tampons d’index sont facultatives. ils fournissent des index aux vertex à partir de la mémoire tampon de vertex. Vous pouvez créer une ou plusieurs mémoires tampons de vertex et, éventuellement, un tampon d’index.

Après avoir créé les ressources de mémoire tampon, vous devez créer un objet de disposition d’entrée pour décrire la disposition des données à l’étape IA, puis lier les ressources de la mémoire tampon à l’étape IA. La création et la liaison de mémoires tampons ne sont pas nécessaires si vos nuanceurs n’utilisent pas de tampons. Pour obtenir un exemple de nuanceur de vertex et de pixels simple qui dessine un triangle unique, consultez [utilisation de l’étape Input-Assembler sans tampons](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).

Pour obtenir de l’aide sur la création d’une mémoire tampon de vertex, consultez [créer une mémoire tampon de vertex](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating). Pour obtenir de l’aide sur la création d’un tampon d’index, consultez créer un tampon d’index.

## <a name="create-the-input-layout-object"></a>Créer l’objet Input-Layout

L’objet de disposition d’entrée encapsule l’état d’entrée de l’étape IA. Cela comprend une description des données d’entrée liées à l’étape IA. Les données sont diffusées dans l’étape IA à partir de la mémoire, à partir d’une ou de plusieurs mémoires tampons de vertex. La description identifie les données d’entrée qui sont liées à partir d’une ou de plusieurs mémoires tampons de vertex et donne au runtime la possibilité de vérifier les types de données d’entrée par rapport aux types de paramètres d’entrée du nuanceur. Ce type de vérification vérifie non seulement que les types sont compatibles, mais également que chacun des éléments requis par le nuanceur est disponible dans les ressources de la mémoire tampon.

Un objet de disposition d’entrée est créé à partir d’un tableau de descriptions d’éléments d’entrée et d’un pointeur vers le nuanceur compilé (consultez [**ID3D11Device :: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)). Le tableau contient un ou plusieurs éléments d’entrée ; chaque élément d’entrée décrit un élément de données de vertex unique à partir d’une seule mémoire tampon de vertex. L’ensemble des descriptions d’élément d’entrée décrit tous les éléments de données de vertex de toutes les mémoires tampon de vertex qui seront liées à l’étape IA.

La description de disposition suivante décrit une mémoire tampon de vertex unique qui contient trois éléments de données de vertex :


```
D3D11_INPUT_ELEMENT_DESC layout[] =
{
    { L"POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT, 0, 12, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
};
```



Une description d’élément d’entrée décrit chaque élément contenu par un seul vertex dans une mémoire tampon de vertex, y compris la taille, le type, l’emplacement et l’objectif. Chaque ligne identifie le type de données à l’aide de la sémantique, de l’index sémantique et du format de données. Une [sémantique](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) est une chaîne de texte qui identifie la façon dont les données sont utilisées. Dans cet exemple, la première ligne identifie les données de position à 3 composants (*xyz*, par exemple); la deuxième ligne identifie les données de texture à 2 composants (*UV*, par exemple); la troisième ligne identifie les données normales.

Dans cet exemple de description d’un élément d’entrée, l’index sémantique (qui est le deuxième paramètre) est défini sur zéro pour les trois lignes. L’index sémantique permet de faire la distinction entre deux lignes qui utilisent la même sémantique. Étant donné qu’il n’existe pas de sémantique similaire dans cet exemple, l’index sémantique peut être défini sur sa valeur par défaut, zéro.

Le troisième paramètre est le *format*. Le format (voir [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) spécifie le nombre de composants par élément et le type de données, qui définit la taille des données pour chaque élément. Le format peut être entièrement typé au moment de la création de la ressource, ou vous pouvez créer une ressource à l’aide d’un **\_ format dxgi**, qui identifie le nombre de composants dans un élément, mais laisse le type de données non défini.

### <a name="input-slots"></a>Emplacements d’entrée

Les données entrent dans la phase IA via des entrées appelées *emplacements d’entrée*, comme indiqué dans l’illustration suivante. L’étape IA a *n* emplacements d’entrée, qui sont conçus pour contenir jusqu’à *n* mémoires tampons de vertex qui fournissent des données d’entrée. Chaque mémoire tampon de vertex doit être assignée à un autre emplacement. ces informations sont stockées dans la déclaration de disposition d’entrée lors de la création de l’objet de disposition d’entrée. Vous pouvez également spécifier un décalage à partir du début de chaque mémoire tampon jusqu’au premier élément de la mémoire tampon à lire.

![illustration des emplacements d’entrée pour l’étape IA](images/d3d10-ia-slots.png)

Les deux paramètres suivants sont l' *emplacement d’entrée* et le *décalage d’entrée*. Lorsque vous utilisez plusieurs mémoires tampons, vous pouvez les lier à un ou plusieurs emplacements d’entrée. Le décalage d’entrée est le nombre d’octets entre le début de la mémoire tampon et le début des données.

### <a name="reusing-input-layout-objects"></a>Réutilisation des objets Input-Layout

Chaque objet de disposition d’entrée est créé sur la base d’une signature de nuanceur ; Cela permet à l’API de valider les éléments d’objet de disposition d’entrée par rapport à la signature de nuanceur-entrée pour s’assurer qu’il existe une correspondance exacte entre les types et la sémantique. Vous pouvez créer un objet de disposition d’entrée unique pour de nombreux nuanceurs, à condition que toutes les signatures de nuanceur-entrée correspondent exactement.

## <a name="bind-objects-to-the-input-assembler-stage"></a>Lier des objets à l’étape Input-Assembler

Après avoir créé les ressources de mémoire tampon de vertex et un objet de disposition d’entrée, vous pouvez les lier à l’étape IA en appelant [**ID3D11DeviceContext :: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) et [**ID3D11DeviceContext :: IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout). L’exemple suivant illustre la liaison d’une mémoire tampon de vertex unique et d’un objet de disposition d’entrée à l’étape IA :


```
UINT stride = sizeof( SimpleVertex );
UINT offset = 0;
g_pd3dDevice->IASetVertexBuffers( 
    0,                // the first input slot for binding
    1,                // the number of buffers in the array
    &g_pVertexBuffer, // the array of vertex buffers
    &stride,          // array of stride values, one for each buffer
    &offset );        // array of offset values, one for each buffer

// Set the input layout
g_pd3dDevice->IASetInputLayout( g_pVertexLayout );
```



La liaison de l’objet de disposition d’entrée requiert uniquement un pointeur vers l’objet.

Dans l’exemple précédent, une seule mémoire tampon de vertex est liée ; Toutefois, plusieurs mémoires tampons de vertex peuvent être liées par un appel unique à [**ID3D11DeviceContext :: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers), et le code suivant montre un appel de ce type pour lier trois mémoires tampons de vertex :


```
UINT strides[3];
strides[0] = sizeof(SimpleVertex1);
strides[1] = sizeof(SimpleVertex2);
strides[2] = sizeof(SimpleVertex3);
UINT offsets[3] = { 0, 0, 0 };
g_pd3dDevice->IASetVertexBuffers( 
    0,                 //first input slot for binding
    3,                 //number of buffers in the array
    &g_pVertexBuffers, //array of three vertex buffers
    &strides,          //array of stride values, one for each buffer
    &offsets );        //array of offset values, one for each buffer
```



Un tampon d’index est lié à l’étape IA en appelant [**ID3D11DeviceContext :: IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).

## <a name="specify-the-primitive-type"></a>Spécifiez le type primitif

Une fois les mémoires tampons d’entrée liées, l’étape IA doit être informée de la manière d’assembler les vertex dans des primitives. Pour ce faire, vous spécifiez le [type primitif](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) en appelant [**ID3D11DeviceContext :: IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); le code suivant appelle cette fonction pour définir les données sous la forme d’une liste de triangles sans contiguïté :


```
g_pd3dDevice->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
```



Les autres types primitifs sont répertoriés dans [**la \_ \_ topologie de la primitive D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology).

## <a name="call-draw-methods"></a>Méthodes Call Draw

Une fois que les ressources d’entrée ont été liées au pipeline, une application appelle une méthode de dessin pour afficher les primitives. Il existe plusieurs méthodes de dessin, qui sont présentées dans le tableau suivant : certains utilisent des mémoires tampons d’index, d’autres utilisent des données d’instance et d’autres données de réutilisation de la phase de sortie en continu comme entrée de l’étape assembleur d’entrée.



| Dessiner des méthodes                                                                                  | Description                                                                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**ID3D11DeviceContext ::D RAW**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)                                 | Dessinez des primitives non indexées et non-instanciées.                                                            |
| [**ID3D11DeviceContext ::D rawInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawinstanced)               | Dessinez des primitives non indexées et instanciées.                                                                |
| [**ID3D11DeviceContext ::D rawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)                   | Dessinez des primitives indexées et non instanciées.                                                                |
| [**ID3D11DeviceContext ::D rawIndexedInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) | Dessinez des primitives indexées et indexées.                                                                    |
| [**ID3D11DeviceContext ::D rawAuto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto)                         | Dessinez des primitives non indexées et non instanciées à partir des données d’entrée provenant de l’étape de sortie en continu. |



 

Chaque méthode Draw restitue un type de topologie unique. Pendant le rendu, les primitives incomplètes (celles sans nombre de vertex suffisant, les primitives partielles, etc.) sont ignorées silencieusement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Étape assembleur d’entrée](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 