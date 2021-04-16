---
title: Récupération des modifications
description: Une fois qu’un client s’est inscrit pour la notification de certaines modifications et qu’une ou plusieurs de ces modifications se produisent, le client reçoit une notification de la part du gestionnaire de tables de routage.
ms.assetid: 5ddebf2d-e3cb-451c-b082-708d2c7d0f79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ccf66d8a1df671cbd9059c444cf26321911bb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507135"
---
# <a name="retrieving-changes"></a>Récupération des modifications

Une fois qu’un client s’est inscrit pour la notification de certaines modifications et qu’une ou plusieurs de ces modifications se produisent, le client reçoit une notification de la part du gestionnaire de tables de routage. Le gestionnaire de table de routage utilise le rappel de [**\_ \_ rappel d’événement RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) fourni dans un appel précédent à [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity). Le gestionnaire de tables de routage indique qu’un \_ événement de notification de modification RTM s’est \_ produit.

Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [utiliser le rappel de notification d’événement](use-the-event-notification-callback.md).

 

 




