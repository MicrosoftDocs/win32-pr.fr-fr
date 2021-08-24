---
description: Les volumes sont implémentés par un pilote de périphérique appelé gestionnaire de volume.
ms.assetid: 424ddbd9-5692-45ef-95fb-7b00b09e3205
title: À propos de la gestion des volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5446726b7caf448eef74884e8b6afc9d27dc4d4fdc6ffadd4572e667aaeb2cf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766309"
---
# <a name="about-volume-management"></a>À propos de la gestion des volumes

Les volumes sont implémentés par un pilote de périphérique appelé gestionnaire de volume. Les exemples incluent le gestionnaire FtDisk, le gestionnaire de disque logique (LDM) et le gestionnaire de volumes logiques (LVM) VERITAS. Les gestionnaires de volume fournissent une couche d’abstraction physique, de protection des données (à l’aide d’une forme de RAID) et de performances.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                       | Description                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Reconnaissance du système de fichiers](file-system-recognition.md)<br/>           | l’objectif de la reconnaissance du système de fichiers est de permettre au Windows système d’exploitation d’avoir une option supplémentaire pour un système de fichiers valide mais non reconnu autre que « RAW ».<br/>                                                                                                         |
| [Attribution d’un nom à un volume](naming-a-volume.md)<br/>                           | Une étiquette est un nom convivial qui est affecté à un volume, généralement par un utilisateur final, pour faciliter sa reconnaissance. Un volume peut avoir une étiquette, une lettre de lecteur, les deux ou aucune des deux. Pour définir l’étiquette d’un volume, utilisez la fonction [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) .<br/> |
| [Énumération des volumes](enumerating-volumes.md)<br/>                   | Pour obtenir une liste complète des volumes sur un ordinateur, ou pour manipuler chaque volume, vous pouvez énumérer les volumes.<br/>                                                                                                                                                       |
| [Obtention d’informations sur le volume](obtaining-volume-information.md)<br/> | Avant d’accéder aux fichiers et aux répertoires d’un volume donné, vous devez déterminer les fonctionnalités du système de fichiers à l’aide de la fonction [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) .<br/>                                                                              |
| [Journaux des modifications](change-journals.md)<br/>                           | Quand une modification est apportée à un fichier ou à un répertoire dans un volume, le journal des modifications USN pour ce volume est mis à jour avec une description de la modification et le nom du fichier ou du répertoire.<br/>                                                                                        |
| [Dossiers montés](volume-mount-points.md)<br/>                       | À l’aide de dossiers montés, vous pouvez unifier des systèmes de fichiers disparates, tels que le système de fichiers NTFS, un système de fichiers FAT 16 bits et un système de fichiers ISO-9660 sur un lecteur de CD-ROM, dans un système de fichiers logique sur un volume NTFS unique.<br/>                                                      |
| [Table de fichiers maîtres](master-file-table.md)<br/>                       | Toutes les informations relatives à un fichier, y compris sa taille, son horodatage, ses autorisations et son contenu, sont stockées dans des entrées de table de fichiers maîtres (MFT) ou dans un espace en dehors de la MFT qui est décrit par les entrées MFT.<br/>                                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations techniques de référence sur les disques et les volumes de base](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))
</dt> <dt>

[Informations techniques de référence sur les disques et les volumes dynamiques](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))
</dt> <dt>

[Référence sur la gestion des volumes](volume-management-reference.md)
</dt> </dl>

 

