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
# <a name="compression-attribute"></a><span data-ttu-id="8ddc7-103">Attribut de compression</span><span class="sxs-lookup"><span data-stu-id="8ddc7-103">Compression Attribute</span></span>

<span data-ttu-id="8ddc7-104">Sur un volume de système de fichiers NTFS, chaque fichier et répertoire a un *attribut de compression*.</span><span class="sxs-lookup"><span data-stu-id="8ddc7-104">On an NTFS file system volume, each file and directory has a *compression attribute*.</span></span> <span data-ttu-id="8ddc7-105">D’autres systèmes de fichiers peuvent également implémenter un attribut de compression pour des fichiers et des répertoires individuels.</span><span class="sxs-lookup"><span data-stu-id="8ddc7-105">Other file systems may also implement a compression attribute for individual files and directories.</span></span>

<span data-ttu-id="8ddc7-106">Vous pouvez déterminer si un système de fichiers prend en charge un attribut de compression pour les fichiers et les répertoires en appelant la fonction [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) et en examinant l’indicateur de bit de **compression de \_ fichier \_ de fichier** .</span><span class="sxs-lookup"><span data-stu-id="8ddc7-106">You can determine whether a file system supports a compression attribute for files and directories by calling the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examining the **FILE\_FILE\_COMPRESSION** bit flag.</span></span>

<span data-ttu-id="8ddc7-107">Utilisez la fonction [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) ou [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) pour déterminer l’attribut de compression d’un fichier ou d’un répertoire.</span><span class="sxs-lookup"><span data-stu-id="8ddc7-107">Use the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) or [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) function to determine the compression attribute of a file or directory.</span></span>

<span data-ttu-id="8ddc7-108">Si l’attribut de compression d’un fichier est défini (**attribut de fichier \_ \_ compressé**), toutes les données du fichier sont compressées.</span><span class="sxs-lookup"><span data-stu-id="8ddc7-108">If a file's compression attribute is set (**FILE\_ATTRIBUTE\_COMPRESSED**), all data in the file is compressed.</span></span> <span data-ttu-id="8ddc7-109">Si l’attribut est clair, aucune des données du fichier n’est compressée.</span><span class="sxs-lookup"><span data-stu-id="8ddc7-109">If the attribute is clear, none of the data in the file is compressed.</span></span> <span data-ttu-id="8ddc7-110">Il n’existe aucun état partiellement compressé du point de vue de la programmation en mode utilisateur ; l’attribut de compression est un indicateur booléen simple de l’état de compression.</span><span class="sxs-lookup"><span data-stu-id="8ddc7-110">There is no partially compressed state from a user-mode programming perspective; the compression attribute is a simple Boolean indicator of compression state.</span></span>

<span data-ttu-id="8ddc7-111">L’attribut de compression d’un répertoire fournit un attribut de compression par défaut pour les fichiers et les sous-répertoires nouvellement créés.</span><span class="sxs-lookup"><span data-stu-id="8ddc7-111">A directory's compression attribute provides a default compression attribute for newly created files and subdirectories.</span></span> <span data-ttu-id="8ddc7-112">Quand vous appelez [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ou [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) pour créer un nouveau fichier ou répertoire, le nouveau fichier ou répertoire hérite de l’attribut de compression de son répertoire parent.</span><span class="sxs-lookup"><span data-stu-id="8ddc7-112">When you call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) or [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) to create a new file or directory, the new file or directory inherits the compression attribute of its parent directory.</span></span>

<span data-ttu-id="8ddc7-113">Pour modifier l’attribut de **fichier \_ \_ compressé** Attribute pour un fichier ou un répertoire, vous devez utiliser la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec le code de contrôle de [**\_ \_ compression FSCTL Set**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) .</span><span class="sxs-lookup"><span data-stu-id="8ddc7-113">To modify the **FILE\_ATTRIBUTE\_COMPRESSED** attribute for a file or directory, you must use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the [**FSCTL\_SET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) control code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ddc7-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8ddc7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ddc7-115">**Constantes d’attribut de fichier**</span><span class="sxs-lookup"><span data-stu-id="8ddc7-115">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> </dl>

 

 
