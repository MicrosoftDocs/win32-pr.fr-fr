---
description: Lorsqu’un fichier est ouvert par un processus à l’aide de la fonction CreateFile, un descripteur de fichier lui est associé jusqu’à ce que le processus se termine ou que le handle soit fermé à l’aide de la fonction CloseHandle.
ms.assetid: c8188e28-ec1b-4746-86f6-5996ff271677
title: Descripteurs de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a54db1935108ab18666fb460a071d77c50f793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868245"
---
# <a name="file-handles"></a><span data-ttu-id="e5e0f-103">Descripteurs de fichiers</span><span class="sxs-lookup"><span data-stu-id="e5e0f-103">File Handles</span></span>

<span data-ttu-id="e5e0f-104">Lorsqu’un fichier est ouvert par un processus à l’aide de la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , un *descripteur de fichier* lui est associé jusqu’à ce que le processus se termine ou que le handle soit fermé à l’aide de la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="e5e0f-104">When a file is opened by a process using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function, a *file handle* is associated with it until either the process terminates or the handle is closed using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="e5e0f-105">Le descripteur de fichier est utilisé pour identifier le fichier dans de nombreux appels de fonction.</span><span class="sxs-lookup"><span data-stu-id="e5e0f-105">The file handle is used to identify the file in many function calls.</span></span>

<span data-ttu-id="e5e0f-106">Chaque descripteur de fichier et objet de fichier est généralement unique à chaque processus qui ouvre un fichier ; les seules exceptions sont lorsqu’un descripteur de fichier détenu par un processus est dupliqué, ou lorsqu’un processus enfant hérite des handles de fichiers du processus parent.</span><span class="sxs-lookup"><span data-stu-id="e5e0f-106">Each file handle and file object is generally unique to each process that opens a file—the only exceptions to this are when a file handle held by a process is duplicated, or when a child process inherits the file handles of the parent process.</span></span> <span data-ttu-id="e5e0f-107">Dans ces situations, ces descripteurs de fichiers sont uniques, mais ils voient un seul objet de fichier partagé.</span><span class="sxs-lookup"><span data-stu-id="e5e0f-107">In these situations, these file handles are unique, but see a single, shared file object.</span></span> <span data-ttu-id="e5e0f-108">Consultez [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) pour plus d’informations sur la duplication des descripteurs de fichiers détenus par les processus.</span><span class="sxs-lookup"><span data-stu-id="e5e0f-108">See [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) for more information on duplicating file handles held by processes.</span></span>

<span data-ttu-id="e5e0f-109">Notez que, si les descripteurs de fichiers sont généralement privés pour un processus, les données de fichier sur lesquelles pointe le point de fichier ne sont pas.</span><span class="sxs-lookup"><span data-stu-id="e5e0f-109">Note that while the file handles are typically private to a process, the file data that the file handles point to is not.</span></span> <span data-ttu-id="e5e0f-110">Par conséquent, les processus et les threads qui partagent le même fichier doivent synchroniser leur accès.</span><span class="sxs-lookup"><span data-stu-id="e5e0f-110">Therefore, processes and threads that share the same file must synchronize their access.</span></span> <span data-ttu-id="e5e0f-111">Pour la plupart des opérations sur un fichier, un processus identifie le fichier par le biais de son pool privé de handles.</span><span class="sxs-lookup"><span data-stu-id="e5e0f-111">For most operations on a file, a process identifies the file through its private pool of handles.</span></span>

 

 
