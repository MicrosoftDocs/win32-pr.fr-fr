---
description: Fonctions à utiliser pour énumérer des dossiers montés sur un volume.
ms.assetid: 052a363f-adfd-4f66-a8b0-5d9d37eedcb0
title: Énumération des dossiers montés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29585100a4b8a94e1b7b78d36b6f0fda228094d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517917"
---
# <a name="enumerating-mounted-folders"></a>Énumération des dossiers montés

Les fonctions suivantes sont utilisées pour énumérer les dossiers montés sur un volume NTFS spécifié :

-   [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)
-   [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)
-   [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)

Ces fonctions fonctionnent de manière très similaire aux fonctions [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)et [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .

Pour énumérer les dossiers montés sur un volume, commencez par déterminer si le volume prend en charge les dossiers montés. Pour ce faire, utilisez le nom de volume retourné par les fonctions [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) et [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) pour appeler la fonction [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) . Les noms retournés incluent une barre oblique inverse de fin ( \) pour être compatible avec la fonction [**GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea) et les fonctions associées. Pour plus d’informations sur les fonctions utilisées pour analyser les volumes d’un ordinateur, consultez [énumération des volumes](enumerating-volumes.md). Lorsque vous appelez la fonction **GetVolumeInformation** , si « NTFS » est retourné dans le paramètre *lpFileSystemNameBuffer* , le volume est un volume NTFS. Le système de fichiers NTFS prend en charge les dossiers montés.

Si le volume est un volume NTFS, commencez par Rechercher les dossiers montés en appelant [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa). Si la recherche est réussie, traitez les résultats en fonction des exigences de votre application. Utilisez ensuite [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa) dans une boucle pour rechercher et traiter les dossiers montés un par un. Lorsqu’il n’y a plus de dossiers montés à énumérer, fermez le handle de recherche en appelant [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose). Notez que la recherche trouvera uniquement les dossiers montés qui se trouvent sur le volume spécifié.

Vous ne devez pas supposer une corrélation entre l’ordre des dossiers montés qui sont retournés par ces fonctions et l’ordre des dossiers montés qui sont retournés par d’autres fonctions ou outils.

 

 



