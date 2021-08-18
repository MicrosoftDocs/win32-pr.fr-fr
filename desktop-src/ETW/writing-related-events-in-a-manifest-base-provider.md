---
description: Utilisez la fonction EventWriteTransfer lorsque plusieurs composants veulent associer leurs événements dans un scénario de suivi de bout en bout.
ms.assetid: 715e3161-d85a-45c0-84df-c6c360b266a1
title: Écriture d’événements connexes dans un fournisseur basé sur un manifeste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f6d09e7e95617b662c3530497b199925921ef9abfd4f3825a5ac799886f95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015207"
---
# <a name="writing-related-events-in-a-manifest-based-provider"></a>Écriture d’événements connexes dans un fournisseur basé sur un manifeste

Utilisez la fonction [**EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) lorsque plusieurs composants veulent associer leurs événements dans un scénario de suivi de bout en bout. Par exemple, les composants A, B et C effectuent des tâches sur une activité associée et veulent lier tous les événements associés à cette activité.

ETW utilise le stockage local des threads pour rendre l’identificateur d’activité du composant précédent disponible pour le composant suivant. Le composant récupère l’identificateur du composant précédent à partir du stockage local et lui affecte l’identificateur d’activité associé. Le consommateur peut ensuite utiliser l’identificateur d’activité associé pour parcourir la chaîne des événements d’un composant à l’autre.

 

 



