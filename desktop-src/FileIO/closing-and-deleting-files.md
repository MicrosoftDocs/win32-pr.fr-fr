---
description: Pour utiliser efficacement les ressources du système d’exploitation, une application doit fermer les fichiers lorsqu’ils ne sont plus nécessaires à l’aide de la fonction CloseHandle. Si un fichier est ouvert lorsqu’une application se termine, le système le ferme automatiquement.
ms.assetid: 6cf9694a-00c4-4750-8822-c25a1a102fd4
title: Fermeture et suppression de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3da31fe7ff38a1bbd1555e2685ceab9ae432574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520744"
---
# <a name="closing-and-deleting-files"></a><span data-ttu-id="1613a-104">Fermeture et suppression de fichiers</span><span class="sxs-lookup"><span data-stu-id="1613a-104">Closing and Deleting Files</span></span>

<span data-ttu-id="1613a-105">Pour utiliser efficacement les ressources du système d’exploitation, une application doit fermer les fichiers lorsqu’ils ne sont plus nécessaires à l’aide de la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="1613a-105">To use operating system resources efficiently, an application should close files when they are no longer needed by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="1613a-106">Si un fichier est ouvert lorsqu’une application se termine, le système le ferme automatiquement.</span><span class="sxs-lookup"><span data-stu-id="1613a-106">If a file is open when an application terminates, the system closes it automatically.</span></span>

<span data-ttu-id="1613a-107">La fonction [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) peut être utilisée pour supprimer un fichier à la fermeture.</span><span class="sxs-lookup"><span data-stu-id="1613a-107">The [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) function can be used to delete a file on close.</span></span> <span data-ttu-id="1613a-108">Un fichier ne peut pas être supprimé tant que tous les descripteurs ne sont pas fermés.</span><span class="sxs-lookup"><span data-stu-id="1613a-108">A file cannot be deleted until all handles to it are closed.</span></span> <span data-ttu-id="1613a-109">Si un fichier ne peut pas être supprimé, son nom ne peut pas être réutilisé.</span><span class="sxs-lookup"><span data-stu-id="1613a-109">If a file cannot be deleted, its name cannot be reused.</span></span> <span data-ttu-id="1613a-110">Pour réutiliser un nom de fichier immédiatement, renommez le fichier existant.</span><span class="sxs-lookup"><span data-stu-id="1613a-110">To reuse a file name immediately, rename the existing file.</span></span>

<span data-ttu-id="1613a-111">Si vous supprimez un fichier ou un répertoire ouvert sur un ordinateur distant et qu’il a déjà été ouvert sur l’ordinateur distant sans le jeu d’autorisations lire le partage, n’appelez pas [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ou [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) pour ouvrir d’abord le fichier ou le répertoire pour la suppression.</span><span class="sxs-lookup"><span data-stu-id="1613a-111">If you are deleting an open file or directory on a remote machine and it has already been opened on the remote machine without the read share permission set, do not call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) or [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) to open the file or directory for deletion first.</span></span> <span data-ttu-id="1613a-112">Cela entraînera une violation de partage.</span><span class="sxs-lookup"><span data-stu-id="1613a-112">Doing so will result in a sharing violation.</span></span>

 

 
