---
description: Windows temps est le nombre de millisecondes écoulées depuis le dernier démarrage du système.
ms.assetid: 95c00204-bfdf-4376-9aae-8d8139ba6750
title: Horloge Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 363f455842a144decc9db7f4d15fa3353b16e74290252b911a814eb62832a790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884045"
---
# <a name="windows-time"></a>Horloge Windows

*Windows temps* est le nombre de millisecondes écoulées depuis le dernier démarrage du système. Ce format existe principalement pour la compatibilité descendante avec la Windows 16 bits. pour vous assurer que les applications conçues pour une Windows de 16 bits continuent de fonctionner correctement, la fonction [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) retourne l’heure de Windows actuelle.

en général, vous utilisez la fonction [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) ou [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) pour comparer l’heure actuelle Windows à l’heure retournée par la fonction [**GetMessageTime**](/windows/win32/api/winuser/nf-winuser-getmessagetime) . **GetMessageTime** retourne l’heure de Windows de la création du message spécifié. **GetTickCount** et **GetTickCount64** sont limités à la résolution de la minuterie du système, qui est d’environ 10 millisecondes à 16 millisecondes. Le temps écoulé récupéré par **GetTickCount** ou **GetTickCount64** comprend le temps que le système passe en mode veille ou veille prolongée.

Si vous avez besoin d’un minuteur de résolution plus élevée, utilisez la fonction [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) , un [minuteur multimédia](/windows/desktop/Multimedia/multimedia-timers)ou un [minuteur haute résolution](../winmsg/about-timers.md). Le temps écoulé récupéré par la fonction **QueryUnbiasedInterruptTime** comprend uniquement l’heure à laquelle le système passe à l’état de travail.

**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP/2000 :** la fonction [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) est disponible à partir de Windows 7 et Windows Server 2008 R2.

Vous pouvez utiliser le compteur de performances temps système du système pour obtenir le nombre de secondes écoulées depuis le démarrage de l’ordinateur. Ce compteur de performance peut être récupéré à partir des données de performances de la clé de Registre **HKEY \_ performance \_ Data**. La valeur retournée est une valeur de 8 octets. Pour plus d’informations, consultez [Compteurs de performances](/windows/desktop/PerfCtrs/performance-counters-portal).

 

 
