---
title: Tas du descripteur non visible par le nuanceur
description: Certains tas de descripteurs ne peuvent pas être référencés par des nuanceurs par le biais de tables de descripteurs, mais ils existent pour aider l’application à mettre en attente les descripteurs avant l’enregistrement d’une liste de commandes ou parce qu’aucun tas visible par le nuanceur n’est requis.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51d30c7a99250ee0842b79d76ccebb6150bcf9a
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343454"
---
# <a name="non-shader-visible-descriptor-heaps"></a>Tas du descripteur non visible par le nuanceur

Certains tas de descripteurs ne peuvent pas être référencés par des nuanceurs par le biais de tables de descripteurs, mais ils existent pour aider l’application à mettre en attente les descripteurs avant l’enregistrement d’une liste de commandes ou parce qu’aucun tas visible par le nuanceur n’est requis.

-   [Affichages non visibles](#non-visible-views)
-   [Résumé](#summary)
-   [Rubriques connexes](#related-topics)

## <a name="non-visible-views"></a>Affichages non visibles

Tous les tas de descripteurs, y compris les tas de descripteurs accessibles aux nuanceurs décrits précédemment, peuvent être manipulés par les listes d’UC et/ou de commandes selon les propriétés du pool de mémoire et de l’accès au processeur que l’application sélectionne pour un tas de descripteur.

Pour les [tas de descripteurs visibles du nuanceur](shader-visible-descriptor-heaps.md), la raison évidente de refuser l’accès du nuanceur à ces tas de descripteurs est lorsqu’ils sont en cours d’installation. Ces tas sont alors rendus visibles par le Shader et accessibles via les tables de descripteurs au moment de l’exécution de la liste de commandes. Toutefois, il n’est pas nécessaire de préparer les tas visibles par le nuanceur, ils peuvent être remplis directement.

D’autres descripteurs sont liés au pipeline en faisant en sorte que leur contenu soit enregistré directement dans la liste des commandes. Ces descripteurs servent uniquement à traduire les paramètres de vue au moment de l’enregistrement de la liste de commandes. Ces tas sont toujours visibles non-nuanceur et contiennent les éléments suivants.

-   Affichages des cibles de rendu (RTVs)
-   Vues du stencil de profondeur (DSV)

Les vues de mémoire tampon d’index (IBVs), les vues de mémoire tampon de vertex (VBVs) et les vues de sortie de flux (SOVs) sont passées directement aux méthodes d’API, et ne possèdent pas de types de tas spécifiques.

Après l’enregistrement dans la liste de commandes (avec un appel tel que [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), par exemple), la mémoire utilisée pour stocker les descripteurs pour cet appel est immédiatement disponible pour une réutilisation après l’appel.

Même les tables de descripteur ont des options dans lesquelles une application peut permettre à l’implémentation de choisir d’enregistrer le contenu de la table dans l’enregistrement de la liste de commandes (plutôt que de déréférencer le pointeur de table au moment de l’exécution).

## <a name="summary"></a>Résumé



|                   | Nuanceur visible, UC en écriture seule                                   | Non-nuanceur visible, lecture/écriture de l’UC                                       |
|-------------------|------------------------------------|----------------------------------------|
| **CBV, SRV, UAV** | oui                                | oui                                    |
| **ÉCHANTILLONNEUR**       | oui                                | oui                                    |
| **Retour au fournisseur**           | non                                 | oui                                    |
| **VUE**           | non                                 | oui                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tas de descripteurs](descriptor-heaps.md)
</dt> </dl>

 

 




