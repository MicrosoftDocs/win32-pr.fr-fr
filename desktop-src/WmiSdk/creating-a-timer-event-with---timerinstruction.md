---
description: Vous créez un événement de minuterie en créant une instance de classes dérivées de la \_ \_ classe TimerInstruction dans n’importe quel espace de noms WMI.
ms.assetid: 3df2a75a-5231-40d7-ae9d-a7a735fbf316
ms.tgt_platform: multiple
title: Création d’un événement de minuterie avec __TimerInstruction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb943419a255846fbde4e17e357f8ce199824085d542d8ad300fb7e301fa3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030669"
---
# <a name="creating-a-timer-event-with-__timerinstruction"></a>Création d’un événement de minuterie avec \_ \_ TimerInstruction

Vous créez un événement de minuterie en créant une instance de classes dérivées de la classe [**\_ \_ TimerInstruction**](--timerinstruction.md) dans n’importe quel espace de noms WMI. WMI génère ensuite l’événement du minuteur au moment approprié. Si vous manquez un événement de minuteur en raison d’un temps d’arrêt de l’ordinateur, WMI vous avertit de l’événement manqué. WMI prend en charge les événements de minuteur pour la compatibilité descendante et pour les scénarios où vous devez connaître le nombre d’événements manqués depuis le dernier événement remis. Toutefois, pour la plupart des événements de minuterie, vous devez créer un filtre d’événements pour [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) ou [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime). Pour plus d’informations, consultez [création d’un événement de minuterie avec Win32 \_ localtime ou Win32 \_ UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).

La procédure suivante décrit comment créer et recevoir un événement de minuterie avec \_ \_ TimerInstruction.

**Pour créer et recevoir un événement de minuterie avec \_ \_ TimerInstruction**

1.  Créez une instance des classes [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md) ou [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) .

    Les classes [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md) et [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) sont dérivées de la classe [**\_ \_ TimerInstruction**](--timerinstruction.md) , qui contient une chaîne unique assignée par le développeur qui identifie le type d’événement du minuteur. La classe **\_ \_ TimerInstruction** contient également une valeur qui spécifie si WMI doit envoyer une notification tardive si l’événement du minuteur se produit lorsque WMI n’est pas disponible.

    Utilisez [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md) pour envoyer des événements de minuteur absolus, qui se produisent à une date spécifique à un moment donné. Utilisez [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) pour envoyer des événements de minuterie d’intervalle, qui se produisent régulièrement.

2.  Configurez votre application pour qu’elle reçoive une instance [**\_ \_ TimerEvent**](--timerevent.md) .

    Pour générer un événement, WMI crée une instance de la classe [**\_ \_ TimerEvent**](--timerevent.md) et transmet l’instance à votre consommateur. L’instance **\_ \_ TimerEvent** contient l’identificateur d’instruction du minuteur du consommateur. L’instance contient également une valeur qui spécifie combien de fois WMI doit envoyer la notification d’événement du minuteur pendant un intervalle quelconque lorsque WMI ne peut pas atteindre le consommateur.

 

 
