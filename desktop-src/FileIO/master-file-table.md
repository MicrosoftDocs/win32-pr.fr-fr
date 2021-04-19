---
description: Toutes les informations relatives à un fichier, y compris sa taille, son horodatage, ses autorisations et son contenu, sont stockées dans des entrées de table de fichiers maîtres (MFT) ou dans un espace en dehors de la MFT qui est décrit par les entrées MFT.
ms.assetid: e0933846-278e-4bc8-8982-c5819c252dad
title: Table de fichiers maîtres (systèmes de fichiers locaux)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260740c03e7b7e4ebe9c7e8ec90035431f6be649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521173"
---
# <a name="master-file-table-local-file-systems"></a>Table de fichiers maîtres (systèmes de fichiers locaux)

Le système de fichiers NTFS contient un fichier appelé *table de fichiers maîtres*(MFT). Il existe au moins une entrée dans la table MFT pour chaque fichier sur un volume de système de fichiers NTFS, y compris la MFT proprement dite. Toutes les informations relatives à un fichier, y compris sa taille, son horodatage, ses autorisations et son contenu, sont stockées dans des entrées MFT ou dans un espace en dehors de la MFT qui est décrit par les entrées MFT.

À mesure que des fichiers sont ajoutés à un volume de système de fichiers NTFS, davantage d’entrées sont ajoutées à la MFT et la taille de la MFT augmente. Lorsque des fichiers sont supprimés d’un volume de système de fichiers NTFS, leurs entrées MFT sont marquées comme étant libres et peuvent être réutilisées. Toutefois, l’espace disque alloué à ces entrées n’est pas réalloué et la taille de la MFT ne diminue pas.

Le système de fichiers NTFS réserve de l’espace pour la MFT afin que la MFT reste la plus contiguë possible au fur et à mesure qu’elle se développe. L’espace réservé par le système de fichiers NTFS pour la MFT dans chaque volume est appelé zone MFT. L’espace pour les fichiers et les répertoires est également alloué à partir de cet espace, mais uniquement après que tout l’espace du volume en dehors de la zone MFT a été alloué.

Selon la taille moyenne des fichiers et d’autres variables, la zone MFT réservée ou l’espace non réservé sur le disque peuvent être alloués en premier au fur et à mesure que le disque se remplit. Les volumes avec un petit nombre de fichiers relativement volumineux allouent l’espace non réservé en premier, tandis que les volumes avec un grand nombre de fichiers relativement petits allouent la zone MFT en premier. Dans les deux cas, la fragmentation de la table MFT commence à avoir lieu lorsqu’une région ou l’autre est entièrement allouée. Si l’espace non réservé est entièrement alloué, l’espace des fichiers et répertoires utilisateur est alloué à partir de la zone MFT. Si la zone MFT est entièrement allouée, l’espace des nouvelles entrées MFT sera alloué à partir de l’espace non réservé.

La table MFT elle-même peut être défragmentée. Pour réduire le risque que la zone MFT devienne entièrement allouée avant la fin du processus de défragmentation, laissez autant d’espace au début de la zone MFT que possible avant de défragmenter le volume. Si la zone MFT est entièrement allouée avant la fin de la défragmentation, il doit y avoir un espace non alloué en dehors de la zone MFT.

La zone MFT par défaut est calculée et réservée par le système lorsqu’elle monte le volume, et est basée sur la taille du volume. Vous pouvez augmenter la zone MFT au moyen de l’entrée de Registre détaillée dans [l’Article 174619 de la base de connaissances Microsoft](https://support.microsoft.com/kb/174619), mais vous ne pouvez pas réduire la taille de la zone MFT par défaut par rapport à ce qui est calculé. L’amélioration de la zone MFT ne diminue pas l’espace disque que les utilisateurs peuvent utiliser pour les fichiers de données.

Pour déterminer la taille actuelle de la MFT, analysez le lecteur du système de fichiers NTFS à l’aide du défragmenteur de disque, puis cliquez sur le bouton **afficher le rapport** . Les statistiques de lecteur s’affichent, y compris la taille MFT actuelle et le nombre de fragments. Vous pouvez également obtenir la taille de la MFT en utilisant le code de contrôle de [**\_ \_ \_ \_ données du volume NTFS FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data) .

 

 
