---
description: Une heure de fichier est une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes qui se sont écoulés depuis 12:00 h 00. Le 1er janvier 1601 temps universel coordonné (UTC). Le système enregistre les heures de fichier lorsque les applications créent, accèdent et écrivent dans des fichiers.
ms.assetid: 52d80b82-9ab0-4631-9e70-85df21da4946
title: Heures du fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1492597b4e71775974ed8b19f6109c5900a8a28720b769c1c10dcf2f70166b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764491"
---
# <a name="file-times"></a>Heures du fichier

Une *heure de fichier* est une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes qui se sont écoulés depuis 12:00 h 00. Le 1er janvier 1601 temps universel coordonné (UTC). Le système enregistre les heures de fichier lorsque les applications créent, accèdent et écrivent dans des fichiers.

Le système de fichiers NTFS stocke les valeurs d’heure au format UTC. elles ne sont donc pas affectées par les modifications apportées au fuseau horaire ou à l’heure d’été. Le système de fichiers FAT stocke les valeurs d’heure en fonction de l’heure locale de l’ordinateur. Par exemple, un fichier enregistré à l’adresse 3:14:00 PST à Washington s’affiche sous la forme 6:14:00 est à New York sur un volume NTFS, mais il est considéré comme 3:14:00 est à New York sur un volume FAT.

Les horodatages sont mis à jour à différents moments et pour diverses raisons. La seule garantie concernant un horodatage de fichier est que l’heure du fichier est correctement reflétée lorsque le handle qui rend la modification est fermé.

Tous les systèmes de fichiers ne peuvent pas enregistrer les heures de création et de dernier accès, et tous les systèmes de fichiers ne les enregistrent pas de la même manière. Par exemple, la résolution de l’heure de création sur la FAT est de 10 millisecondes, tandis que le temps d’écriture a une résolution de 2 secondes et le temps d’accès a une résolution de 1 jour. il s’agit donc vraiment de la date d’accès. Le système de fichiers NTFS retarde les mises à jour de l’heure du dernier accès pour un fichier jusqu’à 1 heure après le dernier accès.

Pour récupérer l’heure du fichier d’un fichier spécifié, utilisez la fonction [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) . **GetFileTime** copie les heures de création, de dernier accès et de dernière écriture dans les structures [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) individuelles. Vous pouvez également récupérer des heures de fichier à l’aide des fonctions [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) et [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) . Ces fonctions copient les heures de fichier dans les structures **fileTime** dans une structure de [**\_ \_ données de recherche Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) . Lors de l’écriture dans un fichier, l’heure de la dernière écriture n’est pas entièrement mise à jour jusqu’à ce que tous les handles utilisés pour l’écriture soient fermés.

Pour définir l’heure d’un fichier, utilisez la fonction [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime) . Cette fonction vous permet de modifier les heures de création, de dernier accès et de dernière écriture sans modifier le contenu du fichier. Vous pouvez comparer les heures des différents fichiers à l’aide de la fonction [**CompareFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-comparefiletime) . La fonction compare deux heures de fichier et retourne une valeur qui indique l’heure ultérieure ou retourne 0 (zéro) si les heures sont égales.

Si vous envisagez de modifier les heures de fichier des fichiers spécifiés, vous pouvez convertir une date et une heure en une heure de fichier à l’aide de la fonction [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) . Vous pouvez également obtenir l’heure système dans une structure [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) en appelant la fonction [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) .

Pour faciliter l’affichage de l’heure d’un fichier pour un utilisateur, utilisez la fonction [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) . **FileTimeToSystemTime** convertit l’heure du fichier et copie le mois, le jour, l’année et l’heure du jour à partir de l’heure du fichier vers une structure [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) .

## <a name="file-times-and-daylight-saving-time"></a>Heures du fichier et heure de l’heure d’été

Vous devez être prudent lorsque vous utilisez des heures de fichier si l’utilisateur a défini le système pour qu’il s’ajuste automatiquement à l’heure d’été.

Pour convertir une heure de fichier en heure locale, utilisez la fonction [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime) . Toutefois, **FileTimeToLocalFileTime** utilise les paramètres actuels pour le fuseau horaire et l’heure d’été. Par conséquent, s’il s’agit de l’heure d’été, il prend en compte l’heure d’été, même si l’heure du fichier que vous convertissez est en heure d’hiver.

Le système de fichiers FAT enregistre les temps sur le disque en heure locale. [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) récupère les heures UTC mises en cache à partir du système de fichiers FAT. Lorsqu’il s’agit de l’heure d’été, le temps récupéré par **GetFileTime** est en retard d’une heure, car le cache n’est pas mis à jour. Lorsque vous redémarrez l’ordinateur, la durée de mise en cache que **GetFileTime** récupère est correcte. [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) récupère l’heure locale à partir du système de fichiers FAT et la convertit en heure UTC en utilisant les paramètres actuels pour le fuseau horaire et l’heure d’été. Par conséquent, s’il s’agit de l’heure d’été, **FindFirstFile** prend en compte l’heure d’été, même si l’heure du fichier que vous convertissez est en heure d’hiver.

Le système de fichiers NTFS enregistre les temps sur le disque au format UTC. Pour tenir compte de l’heure d’été lors de la conversion d’une heure de fichier en heure locale, utilisez la séquence de fonctions suivante au lieu d’utiliser [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime):

-   [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)
-   [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)
-   [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)

## <a name="file-times-and-cdfs"></a>Heures du fichier et CDFS

Les horodatages des fichiers qui se trouvent sur le support ou proviennent d’un média à l’aide du système CDFS (Compact Disc File System) sont ajustés pour le fuseau horaire local. ISO 9660 déclare que CDFS doit afficher les informations de date correctement pour le fuseau horaire local. Cela a pour effet que les dates des fichiers sur CDFS sont affichées de la même façon que sur le format de disque universel (UDF). UDF est la norme la plus récente pour le support de distribution. Si votre code dépend des informations de date non modifiées pour un fichier qui réside sur ou provient d’un média à l’aide de CDFS, il peut ne pas fonctionner correctement.

 

 
