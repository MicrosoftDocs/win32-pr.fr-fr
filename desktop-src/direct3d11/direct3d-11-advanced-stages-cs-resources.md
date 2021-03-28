---
title: Nouveaux types de ressources
description: Plusieurs nouveaux types de ressources ont été ajoutés dans Direct3D 11.
ms.assetid: 597cc12f-dd0e-4603-b670-3f584f25e192
keywords:
- Mémoire tampon d’adresse en octets (vue d’ensemble)
- Mémoire tampon de lecture/écriture (vue d’ensemble)
- Mémoire tampon structurée (vue d’ensemble)
- Mémoire tampon d’accès non triée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b7a75ec95917a5ee819126e42dce3117994574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382291"
---
# <a name="new-resource-types"></a>Nouveaux types de ressources

Plusieurs nouveaux types de ressources ont été ajoutés dans Direct3D 11.

-   [Mémoires tampons et textures en lecture/écriture](#readwrite-buffers-and-textures)
-   [Mémoire tampon structurée](#structured-buffer)
-   [Mémoire tampon d’adresse en octets](#byte-address-buffer)
-   [Tampon ou texture d’accès non ordonné](#unordered-access-buffer-or-texture)
    -   [Ajouter et consommer une mémoire tampon](#append-and-consume-buffer)
-   [Rubriques connexes](#related-topics)

## <a name="readwrite-buffers-and-textures"></a>Mémoires tampons et textures en lecture/écriture

Les ressources du Shader Model 4 sont en lecture seule. Le Shader Model 5 implémente un nouveau jeu correspondant de ressources de lecture/écriture :

-   [RWBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbuffer)
-   [RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)
-   [RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)
-   [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

Ces ressources requièrent une variable de ressource pour accéder à la mémoire (par le biais de l’indexation), car il n’existe aucune méthode permettant d’accéder directement à la mémoire. Une variable de ressource peut être utilisée sur les côtés gauche et droit d’une équation ; s’il est utilisé sur le côté droit, le type de modèle doit être un composant unique (float, int ou uint).

## <a name="structured-buffer"></a>Mémoire tampon structurée

Une mémoire tampon structurée est une mémoire tampon qui contient des éléments de tailles égales. Utilisez une structure avec un ou plusieurs types de membres pour définir un élément. Voici une structure avec trois membres.


```
struct MyStruct
{
    float4 Color;
    float4 Normal;
    bool isAwesome;
};
```



Utilisez cette structure pour déclarer une mémoire tampon structurée comme suit :


```
StructuredBuffer<MyStruct> mySB;
```



Outre l’indexation, une mémoire tampon structurée prend en charge l’accès à un membre unique comme suit :


```
float4 myColor = mySb[27].Color;
```



Utilisez les types d’objets suivants pour accéder à une mémoire tampon structurée :

-   [StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) est une mémoire tampon structurée en lecture seule.
-   [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) est une mémoire tampon structurée en lecture/écriture.

Les [fonctions atomiques](direct3d-11-advanced-stages-cs-atomic-functions.md) qui implémentent des opérations verrouillées sont autorisées sur les éléments int et uint dans un **RWStructuredBuffer**.

## <a name="byte-address-buffer"></a>Mémoire tampon d’adresse en octets

Une mémoire tampon d’adresse en octets est une mémoire tampon dont le contenu est adressable par un décalage d’octet. Normalement, le contenu d’une [mémoire tampon](overviews-direct3d-11-resources-buffers-intro.md) est indexé par élément à l’aide d’un Stride pour chaque élément et le numéro d’élément (N) comme indiqué par S \* N. Une mémoire tampon d’adresse d’octet, qui peut également être appelée mémoire tampon brute, utilise un décalage de valeur d’octet par rapport au début de la mémoire tampon pour accéder aux données. La valeur de l’octet doit être un multiple de quatre afin qu’il soit aligné sur la valeur DWORD. Si une autre valeur est fournie, le comportement n’est pas défini.

Le Shader Model 5 introduit des objets pour accéder à une [mémoire tampon d’adresse en lecture](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) seule, ainsi qu’à une [mémoire tampon d’adresse d’octets en lecture-écriture](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer). Le contenu d’une mémoire tampon d’adresse en octets est conçu pour être un entier non signé 32 bits. Si la valeur de la mémoire tampon n’est pas vraiment un entier non signé, utilisez une fonction telle que [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) pour la lire.

## <a name="unordered-access-buffer-or-texture"></a>Tampon ou texture d’accès non ordonné

Une ressource d’accès non ordonnée (qui comprend des mémoires tampons, des textures et des tableaux de textures sans échantillonnage multiple) autorise un accès en lecture/écriture non ordonné de manière temporelle à partir de plusieurs threads. Cela signifie que ce type de ressource peut être lu/écrit simultanément par plusieurs threads sans générer de conflits de mémoire à l’aide de [fonctions atomiques](direct3d-11-advanced-stages-cs-atomic-functions.md).

Créez une texture ou une mémoire tampon d’accès non triée en appelant une fonction telle que [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) ou [**ID3D11Device :: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) et en passant l’indicateur d’accès non ordonné à la **\_ liaison \_ \_ d3d11** à partir de l’énumération de l' [**\_ \_ indicateur de liaison d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) .

Les ressources d’accès non ordonnées ne peuvent être liées qu’à des nuanceurs de pixels et des nuanceurs de calcul. Pendant l’exécution, les nuanceurs de pixels ou les nuanceurs de calcul exécutés en parallèle ont les mêmes ressources d’accès non ordonnées liées.

### <a name="append-and-consume-buffer"></a>Ajouter et consommer une mémoire tampon

Une mémoire tampon d’ajout et de consommation est un type spécial de ressource non triée qui prend en charge l’ajout et la suppression de valeurs à partir de la fin d’une mémoire tampon de la même manière qu’une pile fonctionne.

Une mémoire tampon d’ajout et de consommation doit être une mémoire tampon structurée :

-   [AppendStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [ConsumeStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)

Utilisez ces ressources par le biais de leurs méthodes, ces ressources n’utilisent pas de variables de ressource.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble du nuanceur de calcul](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 