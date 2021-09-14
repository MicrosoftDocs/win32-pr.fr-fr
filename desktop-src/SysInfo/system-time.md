---
description: L’heure système correspond à la date et à l’heure actuelles de la journée.
ms.assetid: 1a1e251e-2375-4134-bbd8-1e4670b9f9d2
title: Temps système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c727e8898fc2bc973d963c3a3c90524ca50958
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193695"
---
# <a name="system-time"></a>Temps système

L' *heure système* correspond à la date et à l’heure actuelles de la journée. Le système conserve le temps nécessaire pour que vos applications soient en mesure d’accéder à un délai précis. Le système base l’heure système sur le *temps universel coordonné* (UTC). L’heure UTC est faiblement définie comme la date et l’heure actuelles de Greenwich, Angleterre.

Lorsque le système démarre pour la première fois, il définit l’heure système sur une valeur en fonction de l’horloge en temps réel de l’ordinateur, puis met régulièrement à jour l’heure. Pour récupérer l’heure système, utilisez la fonction [**GetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtime) . **GetSystemTime** copie l’heure dans une structure [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) qui contient des membres individuels pour le mois, le jour, l’année, le jour de la semaine, l’heure, les minutes, les secondes et les millisecondes. Il est facile d’afficher ce format à un utilisateur.

Vous pouvez également obtenir l’heure système au format d’heure de fichier à l’aide de la fonction [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) . **GetSystemTimeAsFileTime** copie l’heure dans une structure [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .

Pour définir l’heure système, utilisez la fonction [**setsystemtime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtime) . **Setsystemtime** suppose que vous avez spécifié une heure UTC.

Les fonctions [**GetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment) et [**SetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment) synchronisent l’horloge de l’heure avec une autre source de temps à l’aide d’un ajustement de temps périodique appliqué à chaque interruption de l’horloge.

Notez que le système peut actualiser régulièrement l’heure en synchronisant avec une source de temps. Étant donné que l’heure système peut être ajustée vers l’avant ou vers l’arrière, ne comparez pas les lectures temporelles système pour déterminer le temps écoulé. au lieu de cela, utilisez l’une des méthodes décrites dans [Windows heure](windows-time.md).

 

 
