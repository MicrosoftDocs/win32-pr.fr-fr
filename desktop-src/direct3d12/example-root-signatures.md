---
title: Exemples de signatures racine
description: La section suivante montre les signatures racines qui diffèrent en matière de complexité par rapport à la totalité de l’espace vide.
ms.assetid: 493D35C9-2A90-4688-BD7E-74B9EB2B4E72
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2332a6efb36b309c5dc74a8578a0be9d2f46298375c309872cae8718d5bc5950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118529410"
---
# <a name="example-root-signatures"></a>Exemples de signatures racine

La section suivante montre les signatures racines qui diffèrent en matière de complexité par rapport à la totalité de l’espace vide.

-   [Signature racine vide](#an-empty-root-signature)
-   [Une constante](#one-constant)
-   [Ajout d’une vue de mémoire tampon constante racine](#adding-a-root-constant-buffer-view)
-   [Tables de descripteurs de liaison](#binding-descriptor-tables)
-   [Signature racine plus complexe](#a-more-complex-root-signature)
-   [Affichages de ressources de nuanceur de streaming](#streaming-shader-resource-views)
-   [Rubriques connexes](#related-topics)

## <a name="an-empty-root-signature"></a>Signature racine vide

![une signature racine vide n’a pas de liaisons](images/root-tables-0.png)

Une signature racine vide est peu susceptible d’être utile, mais elle peut être utilisée dans une passe de rendu trivial avec l’utilisation de seul l’assembleur d’entrée, ainsi que des nuanceurs de vertex et de pixels minimaux qui n’accèdent à aucun descripteur. En outre, l’étape de fusion, la cible de rendu et les étapes du stencil de profondeur sont disponibles, même avec une signature racine vide.

## <a name="one-constant"></a>Une constante

![une seule constante racine](images/root-tables-constant.png)

L’emplacement de liaison d’API est l’emplacement où l’argument racine de ce paramètre sera lié au moment de l’enregistrement de la liste de commandes. Le nombre d’emplacements de liaison d’API est implicite, en fonction de l’ordre des paramètres dans la signature racine (le premier est toujours zéro). L’emplacement de liaison HLSL est l’endroit où le nuanceur verra le paramètre racine apparaître. Le type (« uint » dans l’exemple ci-dessus) n’est pas connu du matériel, mais il s’agit simplement d’un commentaire dans l’image, le matériel verra simplement la valeur DWORD unique comme contenu.

Pour lier une constante au moment de l’enregistrement de la liste de commandes, vous devez utiliser une commande similaire à celle-ci :

``` syntax
pCmdList->SetComputeRoot32BitConstant(0,seed); // 0 is the parameter index, seed is used by the shaders
```

## <a name="adding-a-root-constant-buffer-view"></a>Ajout d’une vue de mémoire tampon constante racine

![Ajoute une vue de mémoire tampon constante à la signature racine](images/root-tables-cbv.png)

Cet exemple montre deux constantes racine et une vue de mémoire tampon constante racine (CBV) qui coûte deux emplacements DWORD.

Pour lier une vue de mémoire tampon constante, utilisez une commande telle que la suivante. Notez que le premier paramètre (2) est l’emplacement indiqué dans l’image. En général, un tableau de constantes sera configuré et mis à la disposition des nuanceurs à B0 en tant que CBV.

``` syntax
pCmdList->SetGraphicsRootConstantBufferView(2,GPUVAForCurrDynamicConstants);
```

## <a name="binding-descriptor-tables"></a>Tables de descripteurs de liaison

![Ajoute des tables de descripteurs à la signature racine](images/root-tables-2.png)

Cet exemple illustre l’utilisation de deux tables de descripteurs : l’un déclarant une table de cinq descripteurs qui seront disponibles au moment de l’exécution dans un \_ \_ tas de descripteur UAV SRV CBV, et un autre déclarant une table de deux descripteurs qui s’affichera au moment de l’exécution dans un tas de descripteur d’échantillonnage.

Pour lier des tables de descripteurs lors de l’enregistrement d’une liste de commandes.

``` syntax
pCmdList->SetComputeRootDescriptorTable(1, handleToCurrentMaterialDataInHeap);
pCmdList->SetComputeRootDescriptorTable(2, handleToCurrentMaterialDataInSamplerHeap);
```

Une autre fonctionnalité de la signature racine est la constante racine float4 dont la taille est de quatre DWORDs. La commande suivante lie uniquement les deux DWORDs du milieu des quatre.

``` syntax
pCmdList->SetComputeRoot32BitConstants(0,2,myFloat2Array,1);  // 2 constants starting at offset 1 (middle 2 values in float4)
```

## <a name="a-more-complex-root-signature"></a>Signature racine plus complexe

![signature racine complexe avec de nombreux éléments](images/root-tables-3.png)

Cet exemple montre une signature racine dense avec la plupart des types d’entrées. Deux des tables de descripteurs (aux emplacements 3 et 6) incluent des tableaux de taille illimitée. La charge ici est que l’application ne touche que des descripteurs valides dans un segment de mémoire. Les tableaux non limités ou très grands nécessitent un niveau matériel 2 + de la prise en charge de la liaison de ressources.

Il existe deux échantillonneurs statiques (liés sans nécessiter d’emplacements de signature racine).

À l’emplacement 9, UAV U4 et UAV U5 sont déclarés au même décalage de table de descripteur. Ceci est l’utilisation d’un descripteur avec alias, un descripteur en mémoire s’affiche à la fois comme U4 et U5 dans les nuanceurs HLSL. Dans ce cas, le nuanceur doit être compilé avec l' \_ option les ressources du nuanceur D3D10 peut être un \_ \_ \_ alias ou l' `/res_may_alias` option ou dans fxc. Les descripteurs avec alias permettent à un descripteur d’être lié à plusieurs points de liaison, sans avoir à apporter de modifications aux nuanceurs.

## <a name="streaming-shader-resource-views"></a>Affichages de ressources de nuanceur de streaming

![diffusion en continu des vues de ressources de nuanceur dans cette signature racine](images/root-tables-4.png)

Cette signature racine illustre un scénario dans lequel tous les SRVs sont diffusés dans et en dehors d’un grand tableau. Au moment de l’exécution, une table de descripteurs peut être définie une fois lorsque la signature racine est définie. Ensuite, toutes les lectures de texture sont effectuées en indexant dans le tableau via des constantes alimentées via les premiers arguments racine. Un seul tas de descripteurs est nécessaire et n’est mis à jour que lorsque les textures sont diffusées en continu ou en dehors des emplacements de descripteurs libres.

Les décalages de descripteur dans le tas de grande taille sont identifiés par des nuanceurs utilisant les constantes dans les vues de mémoire tampon constantes. Par exemple, si un nuanceur reçoit un ID de matériau, il peut indexer dans un grand tableau à l’aide de la constante pour accéder au descripteur requis (qui fait référence à la texture requise).

Ce scénario nécessite un matériel avec la liaison de ressource niveau2 +.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Couches matérielles de liaison de ressources](hardware-support.md)
</dt> <dt>

[Liaison de ressource dans HSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Signatures racine](root-signatures.md)
</dt> </dl>

 

 




