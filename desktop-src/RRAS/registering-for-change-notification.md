---
title: Inscription à la notification de modification
description: Un client peut s’inscrire pour recevoir une notification des modifications apportées aux informations de routage stockées dans le gestionnaire de tables de routage. Cette demande ne peut être effectuée qu’après qu’un client s’est inscrit auprès du gestionnaire de tables de routage.
ms.assetid: 90dc98eb-0d0b-4450-848b-c7cedab75a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3a98062fee73c481c1f47c32fa7eeb5465a112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309842"
---
# <a name="registering-for-change-notification"></a>Inscription à la notification de modification

Un client peut s’inscrire pour recevoir une notification des modifications apportées aux informations de routage stockées dans le gestionnaire de tables de routage. Cette demande ne peut être effectuée qu’après qu’un client s’est inscrit auprès du gestionnaire de tables de routage.

Pour s’inscrire à la notification de modification, un client doit appeler [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification), en spécifiant les types de modifications pour lesquels le client doit recevoir une notification. Si le client doit être averti de la modification de destinations spécifiques, le client appelle [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) une fois pour chaque destination.

Le client peut cesser de recevoir des notifications de modification en appelant [**RtmDeregisterFromChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification).

Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [Register for change notification](register-for-change-notification.md).

 

 




