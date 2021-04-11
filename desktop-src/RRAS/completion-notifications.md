---
title: Notifications de saisie semi-automatique
description: Le gestionnaire de connexions d’accès à distance continue les notifications de progression jusqu’à ce que l’opération de connexion soit terminée.
ms.assetid: 2c3b0d03-1cb7-4fa4-a7fa-bcfe623b791f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b949eb7dcc0f09d05d2fb272f4f3d36da40fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029251"
---
# <a name="completion-notifications"></a>Notifications de saisie semi-automatique

Le gestionnaire de connexions d’accès à distance continue les notifications de progression jusqu’à ce que l’opération de connexion soit terminée. Cela se produit dans les situations suivantes :

-   Le gestionnaire reçoit une \_ notification RASCS Connected ou RASCS \_ Disconnected. L’application cliente RAS peut quitter sans rompre la connexion établie.
-   Une erreur se produit. Le gestionnaire reçoit une notification indiquant l’erreur et l’état de la connexion lorsque l’erreur s’est produite. L’application cliente RAS peut se fermer.

L’application cliente RAS ne doit pas supposer que l’opération de connexion est terminée après l’appel de [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa). Il doit attendre l’une des conditions précédentes avant de quitter.

 

 




