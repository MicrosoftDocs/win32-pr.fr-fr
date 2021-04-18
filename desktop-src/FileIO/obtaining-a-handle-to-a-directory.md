---
description: Chaque fois qu’un processus crée ou ouvre un objet d’annuaire, il reçoit un descripteur de l’objet.
ms.assetid: 841c7daa-360c-4d96-8a14-6dcfa159a875
title: Handles de répertoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4215a75622a7fa35ee36d45e769736bf1224a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526974"
---
# <a name="directory-handles"></a><span data-ttu-id="6a557-103">Handles de répertoire</span><span class="sxs-lookup"><span data-stu-id="6a557-103">Directory Handles</span></span>

<span data-ttu-id="6a557-104">Chaque fois qu’un processus crée ou ouvre un objet d’annuaire, il reçoit un descripteur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6a557-104">Whenever a process creates or opens a directory object, it receives a handle to the object.</span></span>

<span data-ttu-id="6a557-105">Pour obtenir un descripteur d’un répertoire existant, appelez la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) avec l’indicateur de **fichier \_ indicateurs de \_ \_ sémantique de sauvegarde** .</span><span class="sxs-lookup"><span data-stu-id="6a557-105">To obtain a handle to an existing directory, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the **FILE\_FLAG\_BACKUP\_SEMANTICS** flag.</span></span>

<span data-ttu-id="6a557-106">Vous pouvez transmettre un handle de répertoire aux fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="6a557-106">You can pass a directory handle to the following functions.</span></span>



| <span data-ttu-id="6a557-107">Fonction</span><span class="sxs-lookup"><span data-stu-id="6a557-107">Function</span></span>                                                         | <span data-ttu-id="6a557-108">Description</span><span class="sxs-lookup"><span data-stu-id="6a557-108">Description</span></span>                                                                                                                                                      |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a557-109">**BackupRead**</span><span class="sxs-lookup"><span data-stu-id="6a557-109">**BackupRead**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupread)                              | <span data-ttu-id="6a557-110">Sauvegardez un fichier ou un répertoire, y compris les informations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="6a557-110">Back up a file or directory, including the security information.</span></span><br/>                                                                                      |
| [<span data-ttu-id="6a557-111">**BackupSeek**</span><span class="sxs-lookup"><span data-stu-id="6a557-111">**BackupSeek**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupseek)                              | <span data-ttu-id="6a557-112">Effectue une recherche vers l’avant dans un flux de données accédé initialement à l’aide de la fonction [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) ou [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) .</span><span class="sxs-lookup"><span data-stu-id="6a557-112">Seeks forward in a data stream initially accessed by using the [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) or [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) function.</span></span><br/> |
| [<span data-ttu-id="6a557-113">**BackupWrite**</span><span class="sxs-lookup"><span data-stu-id="6a557-113">**BackupWrite**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupwrite)                            | <span data-ttu-id="6a557-114">Restaurez un fichier ou un répertoire qui a été sauvegardé à l’aide de [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread).</span><span class="sxs-lookup"><span data-stu-id="6a557-114">Restore a file or directory that was backed up using [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread).</span></span><br/>                                                             |
| [<span data-ttu-id="6a557-115">**GetFileInformationByHandle**</span><span class="sxs-lookup"><span data-stu-id="6a557-115">**GetFileInformationByHandle**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) | <span data-ttu-id="6a557-116">Récupère des informations de fichier pour le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="6a557-116">Retrieves file information for the specified file.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="6a557-117">**GetFileSize**</span><span class="sxs-lookup"><span data-stu-id="6a557-117">**GetFileSize**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)                               | <span data-ttu-id="6a557-118">Récupère la taille du fichier spécifié, en octets.</span><span class="sxs-lookup"><span data-stu-id="6a557-118">Retrieves the size of the specified file, in bytes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="6a557-119">**GetFileTime**</span><span class="sxs-lookup"><span data-stu-id="6a557-119">**GetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | <span data-ttu-id="6a557-120">Récupère la date et l’heure de création, du dernier accès et de la dernière modification d’un fichier ou d’un répertoire.</span><span class="sxs-lookup"><span data-stu-id="6a557-120">Retrieves the date and time that a file or directory was created, last accessed, and last modified.</span></span><br/>                                                   |
| [<span data-ttu-id="6a557-121">**GetFileType**</span><span class="sxs-lookup"><span data-stu-id="6a557-121">**GetFileType**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)                               | <span data-ttu-id="6a557-122">Récupère le type de fichier du fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="6a557-122">Retrieves the file type of the specified file.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="6a557-123">**ReadDirectoryChangesW**</span><span class="sxs-lookup"><span data-stu-id="6a557-123">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)           | <span data-ttu-id="6a557-124">Récupère des informations qui décrivent les modifications dans le répertoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="6a557-124">Retrieves information that describes the changes within the specified directory.</span></span><br/>                                                                      |
| [<span data-ttu-id="6a557-125">**SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="6a557-125">**SetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | <span data-ttu-id="6a557-126">Définit la date et l’heure de création du fichier ou du répertoire spécifié, du dernier accès ou de la dernière modification.</span><span class="sxs-lookup"><span data-stu-id="6a557-126">Sets the date and time that the specified file or directory was created, last accessed, or last modified.</span></span><br/>                                             |



 

 

