---
title: Appels imbriqués à SRSetRestorePoint
description: Cette rubrique décrit la prise en charge des appels imbriqués à SRSetRestorePoint par le biais des types d’événements de modification de système imbriqué de début \_ \_ et de fin de modification de \_ \_ \_ système imbriqué \_ .
ms.assetid: ee2dea47-f95d-4293-ac33-eff622b84db6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12286a69bdb83cb5fd119280e8996c6612e359bf93b9371b6a088a98bf6fd881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857634"
---
# <a name="nested-calls-to-srsetrestorepoint"></a>Appels imbriqués à SRSetRestorePoint

Cette rubrique décrit la prise en charge des appels imbriqués à [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) par le biais des types d’événements de modification de système imbriqué de début \_ et de fin de modification de \_ \_ \_ \_ système imbriqué \_ .

Les applications peuvent appeler [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) en toute sécurité lors de l’utilisation de ces types d’événements. Le premier appel à la fonction crée un point de restauration. Les appels imbriqués suivants à la fonction ne créent pas de points de restauration. Supposons, par exemple, qu’une application effectue les appels suivants à **SRSetRestorePoint**:<dl> Pour le point de restauration A avec dwEventType = BEGIN \_ Nested \_ System \_ change  
Pour le point de restauration B avec dwEventType = BEGIN la \_ \_ modification du système imbriqué \_  
Pour le point de restauration B avec dwEventType = fin de la \_ \_ modification du système imbriqué \_  
Pour le point de restauration A avec dwEventType = fin de la \_ \_ modification du système imbriqué \_  
</dl>

Le deuxième appel ne crée pas de point de restauration, car l’appel est imbriqué.

 

 




