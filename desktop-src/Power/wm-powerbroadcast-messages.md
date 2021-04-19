---
description: Le système diffuse un message à toutes les applications et pilotes installables à chaque fois qu’un événement de gestion de l’alimentation se produit.
ms.assetid: a64ed11a-43d6-41f7-aabd-5dca2a2b4a12
title: Messages WM_POWERBROADCAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f70c5848ec5d71666c26fcd4b5b161e31465543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518678"
---
# <a name="wm_powerbroadcast-messages"></a>\_Messages WM POWERBROADCAST

Le système diffuse un message à toutes les applications et pilotes installables à chaque fois qu’un événement de gestion de l’alimentation se produit. Le système diffuse ces événements par le biais du message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) , en définissant le paramètre *wParam* sur l’événement de gestion de l’alimentation approprié. Par exemple, l’événement [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) indique une modification de l’état de l’alimentation du système. Vous devez vous assurer que votre application répond correctement au message **WM \_ POWERBROADCAST** .

Le système diffuse un événement [PBT \_ APMSUSPEND](pbt-apmsuspend.md) immédiatement avant la suspension de l’opération. Cela donne aux applications et aux pilotes une dernière chance de se préparer pour l’événement. Dans de nombreux cas, le système diffuse ces messages sans demander l’autorisation de le faire. Cela se produit, par exemple, si une application force la suspension avec la fonction [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .

Le système diffuse l’événement [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) ou [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) lors de la restauration de l’opération système. Si une application a reçu un événement [PBT \_ APMSUSPEND](pbt-apmsuspend.md) avant la suspension de l’ordinateur, elle recevra l' \_ événement PBT APMRESUMESUSPEND. Dans le cas contraire, il recevra l' \_ événement PBT APMRESUMECRITICAL.

Le système envoie un événement [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) aux applications qui sont inscrites pour l’événement spécifique à l’aide de [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification). Pour plus d’informations, consultez [inscription pour les événements d’alimentation](registering-for-power-events.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la gestion de l’alimentation](about-power-management.md)
</dt> </dl>

 

 



