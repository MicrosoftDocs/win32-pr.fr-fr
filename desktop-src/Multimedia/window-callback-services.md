---
title: Services de rappel de fenêtre
description: Services de rappel de fenêtre
ms.assetid: 227602e5-7ea1-4afd-ac88-cfeabe746d1f
keywords:
- audio multimédia, services de rappel de fenêtre
- audio, services de rappel de fenêtre
- mixages audio, services de rappel de fenêtre
- mixages, services de rappel de fenêtre
- services de rappel de fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0248928d339dc6c1737ee9dc47f72bac0fb42fe76774e6062177c29064b44257
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781409"
---
# <a name="window-callback-services"></a>Services de rappel de fenêtre

Les services de mixage fournissent des services de rappel de fenêtre afin que votre application puisse traiter les messages des pilotes de mixage. Pour utiliser ces services, spécifiez l' \_ indicateur de fenêtre de rappel dans le paramètre *fdwOpen* et un handle de fenêtre dans le paramètre *DwCallback* de la fonction [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) . Les messages de pilote sont envoyés à la fonction de procédure de fenêtre pour la fenêtre identifiée par le handle dans *dwCallback*. Les messages sont spécifiques au type de périphérique audio.

 

 