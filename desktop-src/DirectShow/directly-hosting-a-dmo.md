---
description: Hébergement direct d’un DMO
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: Hébergement direct d’un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f421ed470ae1d39c04054e1cb4ec6252652ed2083ea336a58525f60a6e525b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982989"
---
# <a name="directly-hosting-a-dmo"></a>Hébergement direct d’un DMO

Cette section décrit comment une application peut agir en tant que client direct d’un DMO. l’application fournit une entrée à l’DMO, le DMO crée une sortie et l’application utilise la sortie pour le rendu, le traitement supplémentaire ou autre chose. L’application est responsable des problèmes tels que l’allocation de mémoire, le minutage et la synchronisation et le Threading. Ces exigences dépendent de la nature de l’application.

les informations contenues dans cette section s’appliquent également si vous écrivez un composant qui agit comme une couche entre une application et un DMO (par exemple, un contrôle ActiveX qui héberge un DMO). en outre, vous devez lire cette section si vous écrivez une DMO, car elle décrit les fonctionnalités que votre DMO doit implémenter.

Cette section contient les rubriques suivantes :

-   [Définition des types de média sur un DMO](setting-media-types-on-a-dmo.md)
-   [Traitement des données dans une DMO](processing-data-in-a-dmo.md)
-   [Traitement sur place](in-place-processing.md)
-   [Flux facultative](optional-streams.md)
-   [Implémentation de IMediaBuffer](implementing-imediabuffer.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de DMOs](using-dmos.md)
</dt> </dl>

 

 



