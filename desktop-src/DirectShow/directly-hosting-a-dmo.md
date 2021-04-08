---
description: Hébergement direct d’un DMO
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: Hébergement direct d’un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3c933cf4eb946abb9ffefd5186159595480887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747660"
---
# <a name="directly-hosting-a-dmo"></a>Hébergement direct d’un DMO

Cette section décrit comment une application peut agir en tant que client direct d’un DMO. L’application fournit une entrée à la solution DMO, la solution DMO crée une sortie et l’application utilise la sortie pour le rendu, le traitement supplémentaire ou autre chose. L’application est responsable des problèmes tels que l’allocation de mémoire, le minutage et la synchronisation et le Threading. Ces exigences dépendent de la nature de l’application.

Les informations contenues dans cette section s’appliquent également si vous écrivez un composant qui agit comme une couche entre une application et un DMO (par exemple, un contrôle ActiveX qui héberge un module DMO). En outre, vous devez lire cette section si vous écrivez un DMO, car il décrit les fonctionnalités que votre application DMO doit implémenter.

Cette section contient les rubriques suivantes :

-   [Définition des types de médias sur un DMO](setting-media-types-on-a-dmo.md)
-   [Traitement des données dans une DMO](processing-data-in-a-dmo.md)
-   [Traitement sur place](in-place-processing.md)
-   [Flux facultatifs](optional-streams.md)
-   [Implémentation de IMediaBuffer](implementing-imediabuffer.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de DMOs](using-dmos.md)
</dt> </dl>

 

 



