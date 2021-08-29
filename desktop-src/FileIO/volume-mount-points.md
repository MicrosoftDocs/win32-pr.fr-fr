---
description: À l’aide de dossiers montés, vous pouvez unifier des systèmes de fichiers disparates, tels que le système de fichiers NTFS, un système de fichiers FAT 16 bits et un système de fichiers ISO-9660 sur un lecteur de CD-ROM, dans un système de fichiers logique sur un volume NTFS unique.
ms.assetid: 6de526cd-5537-4411-b43f-3c0bdac70d64
title: Dossiers montés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe4360377ba94fc23701d13fc62defd666ba9cb3074c4385d98ea87a9354200
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746769"
---
# <a name="mounted-folders"></a>Dossiers montés

Le système de fichiers NTFS prend en charge les dossiers montés. Un *dossier monté* est une association entre un volume et un répertoire sur un autre volume. Lorsqu’un dossier monté est créé, les utilisateurs et les applications peuvent accéder au volume cible soit à l’aide du chemin d’accès au dossier monté, soit à l’aide de la lettre de lecteur du volume. Par exemple, un utilisateur peut créer un dossier monté pour associer le lecteur D : au dossier C : \\ mnt \\ DDrive sur le lecteur c. Après avoir créé le dossier monté, l’utilisateur peut utiliser le \\ chemin d’accès « C : mnt \\ DDrive » pour accéder au lecteur D : comme s’il s’agissait d’un dossier sur le lecteur C :.

À l’aide de dossiers montés, vous pouvez unifier des systèmes de fichiers disparates, tels que le système de fichiers NTFS, un système de fichiers FAT 16 bits et un système de fichiers ISO-9660 sur un lecteur de CD-ROM, dans un système de fichiers logique sur un volume NTFS unique. Ni les utilisateurs ni les applications n’ont besoin d’informations sur le volume cible sur lequel se trouve un fichier spécifique. Toutes les informations dont il a besoin pour localiser un fichier spécifié sont un chemin d’accès complet à l’aide d’un dossier monté sur le volume NTFS. Les volumes peuvent être réorganisés, remplacés ou subdivisés en nombreux volumes sans que les utilisateurs ou les applications aient besoin de modifier les paramètres.

Pour plus d’informations sur les dossiers montés, consultez les rubriques suivantes.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                         | Description                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Création de dossiers montés](mounting-and-dismounting-a-volume.md)<br/>                                                  | La création d’un dossier monté est un processus en deux étapes.<br/>                                                                                                                                                                 |
| [Énumération des dossiers montés](enumerating-volume-mount-points.md)<br/>                                                 | Fonctions à utiliser pour énumérer des dossiers montés sur un volume.<br/>                                                                                                                                                       |
| [Déterminer si un répertoire est un dossier monté](determining-whether-a-directory-is-a-volume-mount-point.md)<br/> | Comment déterminer si un répertoire spécifié est un dossier monté.<br/>                                                                                                                                              |
| [Affectation d’une lettre de lecteur à un volume](assigning-a-drive-letter-to-a-volume.md)<br/>                                   | Vous pouvez affecter une lettre de lecteur (par exemple, X : \) à un volume local à l’aide de la fonction [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , à condition qu’il n’y ait aucun volume déjà affecté à cette lettre de lecteur.<br/> |
| [Fonctions du dossier monté](volume-mount-point-functions.md)<br/>                                                       | Fonctions utilisées pour gérer les dossiers montés.<br/>                                                                                                                                                                        |



 

Pour obtenir des exemples, consultez la section [exemples de dossiers montés](volume-mount-point-examples.md).

 

 




