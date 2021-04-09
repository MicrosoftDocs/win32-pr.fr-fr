---
title: Démarrage et arrêt de Microsoft Locator
description: Les bibliothèques Runtime RPC démarrent automatiquement le localisateur Microsoft si nécessaire. Vous pouvez arrêter et démarrer manuellement le localisateur si, par exemple, vous devez effacer la base de données lors du débogage d’une application distribuée.
ms.assetid: 06b50a9f-b640-45b2-86e2-2bcea6c16c5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433ffdb11e86b06ee53d9b01f7f7755758538f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028495"
---
# <a name="starting-and-stopping-microsoft-locator"></a>Démarrage et arrêt de Microsoft Locator

Les bibliothèques Runtime RPC démarrent automatiquement le localisateur Microsoft si nécessaire. Vous pouvez arrêter et démarrer manuellement le localisateur si, par exemple, vous devez effacer la base de données lors du débogage d’une application distribuée.

**Pour arrêter et démarrer Microsoft Locator**

1.  Dans le panneau de configuration, cliquez sur l’icône Services.

    La boîte de dialogue **services** s’affiche.

2.  Dans la boîte de dialogue **service** , sélectionnez **Microsoft Locator** , puis cliquez sur **Démarrer** ou **arrêter**.

Vous pouvez également démarrer et arrêter Microsoft Locator à partir de la ligne de commande en tapant ce qui suit :

**\[RPCLOCATOR net start/stop \]**

Seul un administrateur peut démarrer Microsoft Locator une fois qu’il est arrêté. Si elle est arrêtée, elle est redémarrée en fonction des besoins des bibliothèques Runtime RPC.

 

 




