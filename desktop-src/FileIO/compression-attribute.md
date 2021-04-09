---
description: Sur un volume de système de fichiers NTFS, chaque fichier et répertoire a un attribut de compression.
ms.assetid: 8aca120c-22a7-4dc8-a921-dfcec1277452
title: Attribut de compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e8e86eebe919476851f35f77cf10d6a07035d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869093"
---
# <a name="compression-attribute"></a>Attribut de compression

Sur un volume de système de fichiers NTFS, chaque fichier et répertoire a un *attribut de compression*. D’autres systèmes de fichiers peuvent également implémenter un attribut de compression pour des fichiers et des répertoires individuels.

Vous pouvez déterminer si un système de fichiers prend en charge un attribut de compression pour les fichiers et les répertoires en appelant la fonction [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) et en examinant l’indicateur de bit de **compression de \_ fichier \_ de fichier** .

Utilisez la fonction [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) ou [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) pour déterminer l’attribut de compression d’un fichier ou d’un répertoire.

Si l’attribut de compression d’un fichier est défini (**attribut de fichier \_ \_ compressé**), toutes les données du fichier sont compressées. Si l’attribut est clair, aucune des données du fichier n’est compressée. Il n’existe aucun état partiellement compressé du point de vue de la programmation en mode utilisateur ; l’attribut de compression est un indicateur booléen simple de l’état de compression.

L’attribut de compression d’un répertoire fournit un attribut de compression par défaut pour les fichiers et les sous-répertoires nouvellement créés. Quand vous appelez [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ou [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) pour créer un nouveau fichier ou répertoire, le nouveau fichier ou répertoire hérite de l’attribut de compression de son répertoire parent.

Pour modifier l’attribut de **fichier \_ \_ compressé** Attribute pour un fichier ou un répertoire, vous devez utiliser la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec le code de contrôle de [**\_ \_ compression FSCTL Set**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Constantes d’attribut de fichier**](file-attribute-constants.md)
</dt> </dl>

 

 
