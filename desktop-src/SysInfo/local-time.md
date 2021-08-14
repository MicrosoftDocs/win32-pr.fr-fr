---
description: Si le système utilise l’heure UTC en interne, vos applications affichent généralement l’heure locale, qui correspond à la date et à l’heure de votre fuseau horaire.
ms.assetid: a6570ec5-ac77-427a-86d9-32cbecc62e37
title: Heure locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95835b76f09ae328c3e1509da68e0fbd989286b2e2669efc9f2280dbce72e35a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763998"
---
# <a name="local-time"></a>Heure locale

Si le système utilise l’heure UTC en interne, vos applications affichent généralement l' **heure locale**, qui correspond à la date et à l’heure de votre fuseau horaire. Par conséquent, pour garantir des résultats corrects, vous devez savoir si une fonction s’attend à recevoir une heure UTC ou une heure locale, et si la fonction retourne une heure UTC ou une heure locale.

Les paramètres de fuseau horaire actuels contrôlent la façon dont le système convertit l’heure UTC et l’heure locale. Vous pouvez récupérer les paramètres de fuseau horaire en cours à l’aide de la fonction [**GetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformation) . La fonction copie le résultat dans une structure d' [**\_ \_ informations de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) et retourne une valeur indiquant si l’heure locale est actuellement en heure d’hiver ou d’heure d’été (DST). Vous pouvez définir les paramètres de fuseau horaire à l’aide de la fonction [**SetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-settimezoneinformation) . Pour prendre en charge les limites de l’heure d’été qui changent d’une année à l’autre, utilisez les fonctions [**GetTimeZoneInformationForYear**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear), [**GetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation) et [**SetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation) .

Pour récupérer l’heure locale, utilisez la fonction [**GetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlocaltime) . **GetLocalTime** convertit l’heure système en heure locale en fonction des paramètres de fuseau horaire en cours et copie le résultat dans une structure [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) . Vous pouvez définir l’heure système à l’aide de la fonction [**SetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime) . **SetLocalTime** suppose que vous avez spécifié une heure locale et convertit en heure UTC avant de définir l’heure système.

Quand vous appelez [**SetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime), le système utilise les informations de fuseau horaire actuelles, y compris le paramètre d’heure d’été, pour effectuer la conversion. Notez que le système utilise le paramètre d’heure d’été de l’heure actuelle, et non la nouvelle heure que vous définissez. Par conséquent, pour garantir le résultat correct, appelez **SetLocalTime** une deuxième fois, maintenant que le premier appel a mis à jour le paramètre d’heure d’été.

Pour convertir une heure UTC en heure locale, utilisez la fonction [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime) . Pour convertir une heure locale en heure UTC, utilisez la fonction [**TzSpecificLocalTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime) .

 

 
