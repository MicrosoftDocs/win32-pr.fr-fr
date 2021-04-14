---
description: Avant d’accéder aux fichiers et aux répertoires d’un volume donné, vous devez déterminer les fonctionnalités du système de fichiers à l’aide de la fonction GetVolumeInformation.
ms.assetid: 008e0cc4-bc12-47e8-a8b7-d4fa9395fceb
title: Obtention d’informations sur le volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc5323c3f82db1115a81902f156e9366abad31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527045"
---
# <a name="obtaining-volume-information"></a>Obtention d’informations sur le volume

La fonction [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) récupère des informations sur le système de fichiers sur un volume donné. Ces informations incluent le nom du volume, le numéro de série du volume, le nom du système de fichiers, les indicateurs du système de fichiers, la longueur maximale d’un nom de fichier, etc. Avant d’accéder aux fichiers et aux répertoires d’un volume donné, vous devez déterminer les fonctionnalités du système de fichiers à l’aide de la fonction [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) . Cette fonction retourne des valeurs que vous pouvez utiliser pour adapter votre application afin qu’elle fonctionne correctement avec le système de fichiers.

En général, vous devez éviter d’utiliser des mémoires tampons statiques pour les noms de fichiers et les chemins d’accès. Utilisez plutôt les valeurs retournées par [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) pour allouer les tampons selon vos besoins. Si vous devez utiliser des mémoires tampons statiques, réservez 256 caractères pour les noms de fichiers et 260 caractères pour les chemins d’accès.

Les fonctions [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) et [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) récupèrent les chemins d’accès au répertoire système et au répertoire Windows, respectivement.

La fonction [**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea) récupère des informations organisationnelles sur un volume, y compris le nombre d’octets par secteur, le nombre de secteurs par cluster, le nombre de clusters libres et le nombre total de clusters. Toutefois, **GetDiskFreeSpace** ne peut pas signaler des tailles de volume supérieures à 2 Go. Pour vous assurer que votre application fonctionne avec des disques durs de grande capacité, utilisez la fonction [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) .

La fonction [**GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea) indique si le volume référencé par la lettre de lecteur spécifiée est un lecteur amovible, fixe, CD-ROM, RAM ou réseau.

La fonction [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives) identifie les volumes présents. La fonction [**GetLogicalDriveStrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw) récupère une chaîne se terminant par un caractère null pour chaque volume présent. Utilisez ces chaînes chaque fois qu’un répertoire racine est requis.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Reconnaissance du système de fichiers](file-system-recognition.md)
</dt> </dl>

 

 
