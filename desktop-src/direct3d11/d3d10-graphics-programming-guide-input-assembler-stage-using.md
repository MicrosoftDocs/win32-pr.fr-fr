---
title: Utilisation des valeurs de System-Generated
description: Les valeurs générées par le système sont générées par l’étape IA (basée sur la sémantique d’entrée fournie par l’utilisateur) pour permettre une certaine efficacité dans les opérations de nuanceur.
ms.assetid: eed1e377-4b0e-4958-b6d4-945b2a952ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbf190ed0c2d5cb4ce38cb3582d64d6d28daddac850e3ae3331254b86714724
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046657"
---
# <a name="using-system-generated-values"></a>Utilisation des valeurs de System-Generated

Les valeurs générées par le système sont générées par l’étape IA (basée sur la [sémantique](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)d’entrée fournie par l’utilisateur) pour permettre une certaine efficacité dans les opérations de nuanceur.

En joignant des données, telles qu’un ID d’instance (visible à VS), un ID de vertex (visible pour VS) ou un ID primitif (visible à GS/PS), une étape de nuanceur ultérieure peut rechercher ces valeurs système pour optimiser le traitement à cette étape. Par exemple, l’étape VS peut Rechercher l’ID d’instance pour récupérer des données par vertex supplémentaires pour le nuanceur ou pour effectuer d’autres opérations. les étapes GS et PS peuvent utiliser l’ID primitif pour extraire les données par primitive de la même façon.

-   [VertexID](#vertexid)
-   [PrimitiveID](#primitiveid)
-   [InstanceID](#instanceid)
-   [Exemple](#example)
-   [Rubriques connexes](#related-topics)

## <a name="vertexid"></a>VertexID

Un ID de vertex est utilisé par chaque étape du nuanceur pour identifier chaque vertex. Il s’agit d’un entier non signé 32 bits dont la valeur par défaut est 0. Elle est assignée à un vertex lorsque la primitive est traitée par l’étape IA. Attachez la sémantique de l’ID de vertex à la déclaration d’entrée du nuanceur pour indiquer à l’étape IA de générer un ID par vertex.

L’IA ajoutera un ID de vertex à chaque vertex pour une utilisation par les étapes du nuanceur. Pour chaque appel de dessin, l’ID de vertex est incrémenté de 1. Dans les appels de dessin indexés, le nombre rétablit la valeur de départ. Pour [**ID3D11DeviceContext ::D rawindexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) et [**ID3D11DeviceContext ::D rawindexedinstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced), l’ID de vertex représente la valeur d’index. Si l’ID de vertex déborde (dépasse 2 ³ ² – 1), il est renvoyé à la ligne à 0.

Pour tous les types primitifs, les vertex ont un ID de vertex qui leur est associé (indépendamment de l’adjacence).

## <a name="primitiveid"></a>PrimitiveID

Un ID primitif est utilisé par chaque étape du nuanceur pour identifier chaque primitive. Il s’agit d’un entier non signé 32 bits dont la valeur par défaut est 0. Elle est assignée à une primitive lorsque la primitive est traitée par l’étape IA. Pour indiquer à l’étape IA de générer un ID primitif, attachez la sémantique de l’ID primitif à la déclaration d’entrée du nuanceur.

L’étape IA ajoutera un ID primitif à chaque primitive pour une utilisation par le nuanceur Geometry ou l’étape nuanceur de pixels (selon la première étape active après l’étape IA). Pour chaque appel de dessin indexé, l’ID primitif est incrémenté de 1. Toutefois, l’ID primitif réinitialise à 0 chaque fois qu’une nouvelle instance commence. Tous les autres appels de dessin ne modifient pas la valeur de l’ID d’instance. Si l’ID d’instance déborde (dépasse 2 ³ ² – 1), il est renvoyé à la ligne à 0.

L’étape du nuanceur de pixels n’a pas d’entrée distincte pour un ID primitif ; Toutefois, toute entrée de nuanceur de pixels qui spécifie un ID primitif utilise un mode d’interpolation constante.

Il n’existe aucune prise en charge pour la génération automatique d’un ID primitif pour les primitives adjacentes. Pour les types primitifs avec contiguïté, tel qu’une bande triangulaire avec contiguïté, un ID primitif est conservé uniquement pour les primitives intérieures (les primitives non adjacentes), tout comme l’ensemble de primitives dans une bande de triangle sans contiguïté.

## <a name="instanceid"></a>InstanceID

Un ID d’instance est utilisé par chaque étape du nuanceur pour identifier l’instance de la géométrie en cours de traitement. Il s’agit d’un entier non signé 32 bits dont la valeur par défaut est 0.

L’étape IA ajoute un ID d’instance à chaque vertex si la déclaration d’entrée du nuanceur de sommets comprend la sémantique de l’ID d’instance. Pour chaque appel de dessin indexé, l’ID d’instance est incrémenté de 1. Tous les autres appels de dessin ne modifient pas la valeur de l’ID d’instance. Si l’ID d’instance déborde (dépasse 2 ³ ² – 1), il est renvoyé à la ligne à 0.

## <a name="example"></a>Exemples

L’illustration suivante montre comment les valeurs système sont attachées à une bande de triangle instance dans l’étape IA.

![illustration des valeurs système pour une bande triangulaire instanciée](images/d3d10-ia-example.png)

Ces tableaux affichent les valeurs système générées pour les deux instances de la même bande triangulaire. La première instance (U d’instance) est affichée en bleu, la deuxième instance (instance V) est affichée en vert. Les lignes pleines connectent les vertex dans les primitives, les lignes en pointillés connectent les vertex adjacents.

Les tableaux suivants indiquent les valeurs générées par le système pour l’instance U.



| Données de vertex    | C, U | D, U | E, U | F, U | G, U | H, U | I, U | J, U | K, U | L, U |
|----------------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **VertexID**   | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| **InstanceID** | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |



 



|                 | Valeur    | Valeur    | Valeur    |
|-----------------|-----|-----|-----|
| **PrimitiveID** | 0   | 1   | 2   |
| **InstanceID**  | 0   | 0   | 0   |



 

Les tableaux suivants indiquent les valeurs générées par le système pour l’instance V.



| Données de vertex    | C, V | D, V | E, V | F, V | G, V | H, V | I, V | J, V | K, V | L, V |
|----------------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **VertexID**   | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| **InstanceID** | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   |



 



|                 |Valeur     | Valeur    |  Valeur   |
|-----------------|-----|-----|-----|
| **PrimitiveID** | 0   | 1   | 2   |
| **InstanceID**  | 1   | 1   | 1   |



 

L’assembleur d’entrée génère les ID (vertex, primitive et instance); Notez également que chaque instance reçoit un ID d’instance unique. Les données se terminent par la bande coupée, qui sépare chaque instance de la bande de triangle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Étape assembleur d’entrée](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 