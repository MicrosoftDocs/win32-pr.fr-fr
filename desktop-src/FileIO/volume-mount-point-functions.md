---
description: Fonctions utilisées pour gérer les dossiers montés.
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: Fonctions du dossier monté
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e984b9bee902f11af9d7b2b956ea0681cd6e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319409"
---
# <a name="mounted-folder-functions"></a>Fonctions du dossier monté

Les fonctions de dossiers montées peuvent être divisées en trois groupes : fonctions à usage général, fonctions utilisées pour rechercher des volumes et fonctions utilisées pour analyser un volume à la recherche de dossiers montés.

## <a name="general-purpose-mounted-folder-functions"></a>Fonctions du dossier monté General-Purpose



| Fonction                                                                     | Description                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)                     | Supprime une lettre de lecteur ou un dossier monté.                                                                                                                   |
| [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) | Récupère le chemin d’accès du GUID du volume associé au point de montage de volume spécifié (lettre de lecteur, chemin d’accès du GUID du volume ou dossier monté). |
| [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)                               | Récupère le dossier monté associé au volume spécifié.                                                                                  |
| [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)                           | Associe un volume à une lettre de lecteur ou à un répertoire sur un autre volume.                                                                                   |



 

## <a name="volume-scanning-functions"></a>Fonctions Volume-Scanning



| Fonction                                   | Description                                                                                                                                    |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) | Retourne le nom d’un volume sur un ordinateur. [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) est utilisé pour commencer à énumérer les volumes d’un ordinateur. |
| [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)   | Continue la recherche d’un volume lancée par un appel à [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).                                                     |
| [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose) | Ferme une recherche de volumes.                                                                                                                   |



 

## <a name="mounted-folder-scanning-functions"></a>Fonctions d’analyse des dossiers montés



| Fonction                                                       | Description                                                                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) | Récupère le nom d’un dossier monté sur le volume spécifié. [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) est utilisé pour commencer l’analyse des dossiers montés sur un volume. |
| [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)   | Poursuit une recherche de dossier montée démarrée par un appel à [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).                                                                    |
| [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) | Ferme une recherche de dossiers montés.                                                                                                                                                      |



 

 

 



