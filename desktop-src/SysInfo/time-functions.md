---
description: Les fonctions suivantes sont utilisées avec l’heure système.
ms.assetid: 3733f611-c6a1-4d48-b21e-ada3490c5de1
title: Fonctions d’heure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1187c029bac34411fdca28dd3b27322478de678
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526200"
---
# <a name="time-functions"></a>Fonctions d’heure

Les fonctions suivantes sont utilisées avec l’heure système.



| Fonction                                                                   | Description                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**GetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtime)                                     | Récupère la date et l’heure système actuelles au format UTC.                                              |
| [**GetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment)                 | Détermine si le système applique des ajustements de temps périodiques à son horloge.          |
| [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata)                                    | Met en forme une heure système sous la forme d’une chaîne d’heure pour les paramètres régionaux spécifiés.                                         |
| [**NtQuerySystemTime**](/windows/desktop/api/Winternl/nf-winternl-ntquerysystemtime)                             | Retourne l’heure système.                                                                               |
| [**RtlLocalTimeToSystemTime**](/windows/desktop/api/Winternl/nf-winternl-rtllocaltimetosystemtime)               | Convertit l’heure locale spécifiée en heure système.                                                      |
| [**RtlTimeToSecondsSince1970**](/windows/desktop/api/Winternl/nf-winternl-rtltimetosecondssince1970)             | Convertit l’heure système spécifiée en nombre de secondes depuis la première seconde du 1er janvier 1970. |
| [**SetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtime)                                     | Définit la date et l’heure système actuelles.                                                                 |
| [**SetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment)                 | Active ou désactive les ajustements de temps périodiques de l’horloge du système.                       |
| [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)                       | Convertit une heure système en heure de fichier.                                                                 |
| [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime) | Convertit une heure UTC en heure locale correspondante d’un fuseau horaire spécifié.                               |
| [**TzSpecificLocalTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime) | Convertit une heure locale en heure UTC.                                                                   |



 

Les fonctions suivantes sont utilisées avec l’heure locale.



| Fonction                                                                                           | Description                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-enumdynamictimezoneinformation)                           | Énumère les entrées d’informations d’heure d’été dynamiques stockées dans le registre.                                                             |
| [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime)                                         | Convertit l’heure UTC d’un fichier en heure locale.                                                                                                  |
| [**GetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation)                             | Récupère les paramètres du fuseau horaire actuel et de l’heure d’été dynamique.                                                                      |
| [**GetDynamicTimeZoneInformationEffectiveYears**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformationeffectiveyears) | Récupère une plage, exprimée en années, pour laquelle les [**\_ \_ \_ informations relatives aux fuseaux horaires dynamiques**](/windows/win32/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information) comportent des entrées valides. |
| [**GetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlocaltime)                                                               | Récupère la date et l’heure locales actuelles.                                                                                                      |
| [**GetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)                                           | Récupère les paramètres de fuseau horaire en cours.                                                                                                       |
| [**GetTimeZoneInformationForYear**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear)                             | Récupère les paramètres de fuseau horaire pour l’année et le fuseau horaire spécifiés.                                                                          |
| [**RtlLocalTimeToSystemTime**](/windows/desktop/api/Winternl/nf-winternl-rtllocaltimetosystemtime)                                       | Convertit l’heure locale spécifiée en heure système.                                                                                               |
| [**SetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation)                             | Définit les paramètres du fuseau horaire actuel et de l’heure d’été dynamique.                                                                           |
| [**SetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime)                                                               | Définit la date et l’heure locales actuelles.                                                                                                           |
| [**SetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-settimezoneinformation)                                           | Définit les paramètres du fuseau horaire actuel.                                                                                                            |
| [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)                         | Convertit une heure UTC en heure locale correspondante d’un fuseau horaire spécifié.                                                                        |
| [**SystemTimeToTzSpecificLocalTimeEx**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltimeex)                     | Convertit une heure UTC avec les paramètres d’heure d’été dynamiques en l’heure locale correspondante d’un fuseau horaire spécifié.                             |
| [**TzSpecificLocalTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime)                         | Convertit une heure locale en heure UTC.                                                                                                            |
| [**TzSpecificLocalTimeToSystemTimeEx**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtimeex)                     | Convertit une heure locale avec les paramètres d’heure d’été dynamiques en heure UTC.                                                                   |



 

Les fonctions suivantes sont utilisées avec l’heure de fichier.



| Fonction                                                   | Description                                                                                                     |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**CompareFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-comparefiletime)                 | Compare deux heures de fichier.                                                                                        |
| [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime) | Convertit l’heure UTC d’un fichier en heure locale.                                                                  |
| [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)       | Convertit une heure de fichier au format d’heure système.                                                                     |
| [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime)                         | Récupère la date et l’heure de création, du dernier accès et de la dernière modification du fichier ou du répertoire spécifié. |
| [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) | Récupère la date et l’heure système actuelles au format UTC.                                                       |
| [**LocalFileTimeToFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-localfiletimetofiletime) | Convertit une heure de fichier local en heure de fichier en fonction de l’heure UTC.                                                         |
| [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime)                         | Définit la date et l’heure de création du fichier ou du répertoire spécifié, du dernier accès ou de la dernière modification.       |
| [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)       | Convertit une heure système en heure de fichier.                                                                          |



 

Les fonctions suivantes sont utilisées avec la date et l’heure MS-DOS.



| Fonction                                               | Description                                          |
|--------------------------------------------------------|------------------------------------------------------|
| [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) | Convertit les valeurs de date et d’heure MS-DOS en une heure de fichier. |
| [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) | Convertit une heure de fichier en valeurs de date et d’heure MS-DOS. |



 

Les fonctions suivantes sont utilisées avec l’heure Windows.



| Fonction                                 | Description                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) | Récupère les informations de minutage du système.                                                                  |
| [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount)     | Récupère le nombre de millisecondes qui se sont écoulées depuis le démarrage du système, jusqu’à 49,7 jours. |
| [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) | Récupère le nombre de millisecondes qui se sont écoulées depuis le démarrage du système.                  |



 

Les fonctions suivantes sont utilisées avec les compteurs de performance haute résolution.



| Fonction                                                              | Description                                                             |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)     | Récupère la valeur actuelle du compteur de performance haute résolution. |
| [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) | Récupère la fréquence du compteur de performance haute résolution.     |



 

Les fonctions suivantes sont utilisées avec le compteur de performances auxiliaire.



| Fonction                                                                                           | Description                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QueryAuxiliaryCounterFrequency**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryauxiliarycounterfrequency)                           | Interroge la fréquence des compteurs auxiliaires.                                                                                                                                                                      |
| [**ConvertAuxiliaryCounterToPerformanceCounter**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-convertauxiliarycountertoperformancecounter) | Convertit la valeur de compteur auxiliaire spécifiée en valeur de compteur de performance correspondante ; fournit éventuellement l’erreur de conversion estimée en nanosecondes en raison de la latence et de la dérive maximale possible. |
| [**ConvertPerformanceCounterToAuxiliaryCounter**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-convertperformancecountertoauxiliarycounter) | Convertit la valeur du compteur de performance spécifiée en valeur de compteur auxiliaire correspondante ; fournit éventuellement l’erreur de conversion estimée en nanosecondes en raison de la latence et de la dérive maximale possible. |



 

La fonction suivante est utilisée avec le temps d’interruption.



| Fonction                                                                       | Description                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)                               | Obtient le nombre d’interruptions actuel.                                                                                                                                                                                                                |
| [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)                 | Obtient le nombre actuel d’interruptions, dans une forme plus précise que [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) .                                                                                                                             |
| [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)               | Obtient le nombre actuel d’interruptions non biaisées. Le nombre de temps d’interruption non biaisé n’inclut pas le temps passé par le système en mode veille ou veille prolongée.                                                                                                    |
| [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) | Obtient le nombre actuel d’interruptions non biaisées, dans une forme plus précise que [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) . Le nombre de temps d’interruption non biaisé n’inclut pas le temps passé par le système en mode veille ou veille prolongée. |



 

 

 
