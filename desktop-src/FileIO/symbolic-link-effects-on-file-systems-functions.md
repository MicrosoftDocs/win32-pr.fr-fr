---
description: La façon dont les liens symboliques affectent les fonctions de fichier standard qui utilisent des noms de chemin d’accès pour spécifier un ou plusieurs fichiers.
ms.assetid: afda53eb-d0db-4844-9dd0-8a7d93ca341f
title: Effets de liens symboliques sur les fonctions des systèmes de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4a2fe1696bf5260a0c55ba8b6e4f107270d6da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519489"
---
# <a name="symbolic-link-effects-on-file-systems-functions"></a><span data-ttu-id="7ecf5-103">Effets de liens symboliques sur les fonctions des systèmes de fichiers</span><span class="sxs-lookup"><span data-stu-id="7ecf5-103">Symbolic Link Effects on File Systems Functions</span></span>

<span data-ttu-id="7ecf5-104">Plusieurs fonctions de fichier standard qui utilisent des noms de chemin d’accès pour spécifier un ou plusieurs fichiers sont affectées par l’utilisation de liens symboliques.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-104">Several standard file functions that use path names to specify one or more files are affected by the use of symbolic links.</span></span> <span data-ttu-id="7ecf5-105">Cette rubrique répertorie ces fonctions et décrit les modifications de comportement :</span><span class="sxs-lookup"><span data-stu-id="7ecf5-105">This topic lists those functions and describes the changes in behavior:</span></span>

-   [<span data-ttu-id="7ecf5-106">CopyFile et CopyFileTransacted</span><span class="sxs-lookup"><span data-stu-id="7ecf5-106">CopyFile and CopyFileTransacted</span></span>](#copyfile-and-copyfiletransacted)
-   [<span data-ttu-id="7ecf5-107">CopyFileEx</span><span class="sxs-lookup"><span data-stu-id="7ecf5-107">CopyFileEx</span></span>](#copyfileex)
-   [<span data-ttu-id="7ecf5-108">CreateFile et CreateFileTransacted</span><span class="sxs-lookup"><span data-stu-id="7ecf5-108">CreateFile and CreateFileTransacted</span></span>](#createfile-and-createfiletransacted)
-   [<span data-ttu-id="7ecf5-109">CreateHardLink et CreateHardLinkTransacted</span><span class="sxs-lookup"><span data-stu-id="7ecf5-109">CreateHardLink and CreateHardLinkTransacted</span></span>](#createhardlink-and-createhardlinktransacted)
-   [<span data-ttu-id="7ecf5-110">DeleteFile et DeleteFileTransacted</span><span class="sxs-lookup"><span data-stu-id="7ecf5-110">DeleteFile and DeleteFileTransacted</span></span>](#deletefile-and-deletefiletransacted)
-   [<span data-ttu-id="7ecf5-111">FindFirstChangeNotification</span><span class="sxs-lookup"><span data-stu-id="7ecf5-111">FindFirstChangeNotification</span></span>](#findfirstchangenotification)
-   [<span data-ttu-id="7ecf5-112">FindFirstFile et FindFirstFileTransacted</span><span class="sxs-lookup"><span data-stu-id="7ecf5-112">FindFirstFile and FindFirstFileTransacted</span></span>](#findfirstfile-and-findfirstfiletransacted)
-   [<span data-ttu-id="7ecf5-113">FindFirstFileEx</span><span class="sxs-lookup"><span data-stu-id="7ecf5-113">FindFirstFileEx</span></span>](#findfirstfileex)
-   [<span data-ttu-id="7ecf5-114">FindNextFile</span><span class="sxs-lookup"><span data-stu-id="7ecf5-114">FindNextFile</span></span>](#findnextfile)
-   [<span data-ttu-id="7ecf5-115">GetBinaryType</span><span class="sxs-lookup"><span data-stu-id="7ecf5-115">GetBinaryType</span></span>](#getbinarytype)
-   [<span data-ttu-id="7ecf5-116">GetCompressedFileSize et GetCompressedFileSizeTransacted</span><span class="sxs-lookup"><span data-stu-id="7ecf5-116">GetCompressedFileSize and GetCompressedFileSizeTransacted</span></span>](#getcompressedfilesize-and-getcompressedfilesizetransacted)
-   [<span data-ttu-id="7ecf5-117">GetDiskFreeSpace</span><span class="sxs-lookup"><span data-stu-id="7ecf5-117">GetDiskFreeSpace</span></span>](#getdiskfreespaceex)
-   [<span data-ttu-id="7ecf5-118">GetDiskFreeSpaceEx</span><span class="sxs-lookup"><span data-stu-id="7ecf5-118">GetDiskFreeSpaceEx</span></span>](#getdiskfreespaceex)
-   [<span data-ttu-id="7ecf5-119">GetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="7ecf5-119">GetFileAttributes</span></span>](#getfileattributesex)
-   [<span data-ttu-id="7ecf5-120">GetFileAttributesEx</span><span class="sxs-lookup"><span data-stu-id="7ecf5-120">GetFileAttributesEx</span></span>](#getfileattributesex)
-   [<span data-ttu-id="7ecf5-121">GetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="7ecf5-121">GetFileSecurity</span></span>](#getfilesecurity)
-   [<span data-ttu-id="7ecf5-122">GetTempPath</span><span class="sxs-lookup"><span data-stu-id="7ecf5-122">GetTempPath</span></span>](#gettemppath)
-   [<span data-ttu-id="7ecf5-123">GetVolumeInformation</span><span class="sxs-lookup"><span data-stu-id="7ecf5-123">GetVolumeInformation</span></span>](#getvolumeinformation)
-   [<span data-ttu-id="7ecf5-124">SetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="7ecf5-124">SetFileAttributes</span></span>](#setfileattributes)
-   [<span data-ttu-id="7ecf5-125">SetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="7ecf5-125">SetFileSecurity</span></span>](#setfilesecurity)
-   [<span data-ttu-id="7ecf5-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7ecf5-126">Related topics</span></span>](#related-topics)

<span data-ttu-id="7ecf5-127">Dans les descriptions ci-dessous, les termes suivants sont utilisés :</span><span class="sxs-lookup"><span data-stu-id="7ecf5-127">In the descriptions below, the following terms are used:</span></span>

-   <span data-ttu-id="7ecf5-128">Fichier source : fichier d’origine à copier.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-128">Source file—The original file that is to be copied.</span></span>
-   <span data-ttu-id="7ecf5-129">Fichier de destination : copie nouvellement créée du fichier.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-129">Destination file—The newly created copy of the file.</span></span>
-   <span data-ttu-id="7ecf5-130">Cible : entité vers laquelle pointe un lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-130">Target—The entity that a symbolic link points to.</span></span>

> [!Note]  
> <span data-ttu-id="7ecf5-131">Le comportement des fonctions qui acceptent un descripteur créé à l’aide de la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , telle que la fonction [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) , varie selon que la fonction **CreateFile** a été appelée ou non à l’aide de l’indicateur de fichier ouvrir l’indicateur de **\_ \_ \_ \_ point d’analyse** .</span><span class="sxs-lookup"><span data-stu-id="7ecf5-131">The behavior of functions that accept a handle created using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function, such as the [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) function, will differ based on whether or not the **CreateFile** function was called using the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag.</span></span> <span data-ttu-id="7ecf5-132">Pour plus d’informations, consultez [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) et les sections [CreateFile et CreateFileTransacted](#createfile-and-createfiletransacted) suivantes.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-132">For more information, see [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and the following [CreateFile and CreateFileTransacted](#createfile-and-createfiletransacted) section.</span></span>

 

## <a name="copyfile-and-copyfiletransacted"></a><span data-ttu-id="7ecf5-133">CopyFile et CopyFileTransacted</span><span class="sxs-lookup"><span data-stu-id="7ecf5-133">CopyFile and CopyFileTransacted</span></span>

<span data-ttu-id="7ecf5-134">Si le fichier source est un lien symbolique, le fichier copié réel est la cible du lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-134">If the source file is a symbolic link, the actual file copied is the target of the symbolic link.</span></span>

<span data-ttu-id="7ecf5-135">Si le fichier de destination existe déjà et qu’il s’agit d’un lien symbolique, le lien symbolique est remplacé par le fichier source.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-135">If the destination file already exists and is a symbolic link, the symbolic link is overwritten by the source file.</span></span>

## <a name="copyfileex"></a><span data-ttu-id="7ecf5-136">CopyFileEx</span><span class="sxs-lookup"><span data-stu-id="7ecf5-136">CopyFileEx</span></span>

<span data-ttu-id="7ecf5-137">Si **la \_ \_ copie du \_ lien symbolique** de copie de fichier est spécifiée et :</span><span class="sxs-lookup"><span data-stu-id="7ecf5-137">If **COPY\_FILE\_COPY\_SYMLINK** is specified and:</span></span>

-   <span data-ttu-id="7ecf5-138">Si le fichier source est un lien symbolique, le lien symbolique est copié, et non le fichier cible.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-138">If the source file is a symbolic link, the symbolic link is copied, not the target file.</span></span>
-   <span data-ttu-id="7ecf5-139">Si le fichier source n’est pas un lien symbolique, le comportement n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-139">If the source file is not a symbolic link, there is no change in behavior.</span></span>
-   <span data-ttu-id="7ecf5-140">Si le fichier de destination est un lien symbolique existant, le lien symbolique est remplacé, et non le fichier cible.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-140">If the destination file is an existing symbolic link, the symbolic link is overwritten, not the target file.</span></span>
-   <span data-ttu-id="7ecf5-141">Si **le \_ fichier de copie \_ échoue \_ si \_ Exists** est également spécifié et que le fichier de destination est un lien symbolique existant, l’opération échoue dans tous les cas.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-141">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is also specified, and the destination file is an existing symbolic link, the operation fails in all cases.</span></span>

<span data-ttu-id="7ecf5-142">Si **le \_ \_ \_ lien symbolique** copie du fichier de copie n’est pas spécifié et :</span><span class="sxs-lookup"><span data-stu-id="7ecf5-142">If **COPY\_FILE\_COPY\_SYMLINK** is not specified and:</span></span>

-   <span data-ttu-id="7ecf5-143">Si **le \_ fichier de copie \_ échoue \_ si \_ Exists** est également spécifié et que le fichier de destination est un lien symbolique existant, l’opération échoue uniquement si la cible du lien symbolique existe.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-143">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is also specified, and the destination file is an existing symbolic link, the operation fails only if the target of the symbolic link exists.</span></span>
-   <span data-ttu-id="7ecf5-144">Si **le \_ fichier de copie \_ échoue \_ si \_ Exists** n’est pas spécifié, le comportement n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-144">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is not specified, there is no change in behavior.</span></span>

<span data-ttu-id="7ecf5-145">**Windows Server 2003 et Windows XP :** L' **indicateur \_ \_ \_ symlink de copie** de copie de fichier n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-145">**Windows Server 2003 and Windows XP:** The **COPY\_FILE\_COPY\_SYMLINK** flag is not supported.</span></span> <span data-ttu-id="7ecf5-146">Si le fichier source est un lien symbolique, le fichier copié réel est la cible du lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-146">If the source file is a symbolic link, the actual file copied is the target of the symbolic link.</span></span>

## <a name="createfile-and-createfiletransacted"></a><span data-ttu-id="7ecf5-147">CreateFile et CreateFileTransacted</span><span class="sxs-lookup"><span data-stu-id="7ecf5-147">CreateFile and CreateFileTransacted</span></span>

<span data-ttu-id="7ecf5-148">Si l’appel à cette fonction crée un nouveau fichier, le comportement n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-148">If the call to this function creates a new file, there is no change in behavior.</span></span>

<span data-ttu-id="7ecf5-149">Si **l' \_ indicateur de fichier ouvrir le \_ \_ \_ point d’analyse** est spécifié et :</span><span class="sxs-lookup"><span data-stu-id="7ecf5-149">If **FILE\_FLAG\_OPEN\_REPARSE\_POINT** is specified and:</span></span>

-   <span data-ttu-id="7ecf5-150">Si un fichier existant est ouvert et qu’il s’agit d’un lien symbolique, le handle retourné est un handle vers le lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-150">If an existing file is opened and it is a symbolic link, the handle returned is a handle to the symbolic link.</span></span>
-   <span data-ttu-id="7ecf5-151">Si l’option **créer \_ toujours**, **tronquer le fichier \_ existant** ou **Supprimer l' \_ indicateur de fichier \_ \_ lors de la \_ fermeture** est spécifiée, le fichier affecté est un lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-151">If **CREATE\_ALWAYS**, **TRUNCATE\_EXISTING**, or **FILE\_FLAG\_DELETE\_ON\_CLOSE** are specified, the file affected is a symbolic link.</span></span>

<span data-ttu-id="7ecf5-152">Si aucun indicateur de fichier n’est ouvert, le **\_ \_ \_ \_ point d’analyse** n’est pas spécifié et :</span><span class="sxs-lookup"><span data-stu-id="7ecf5-152">If **FILE\_FLAG\_OPEN\_REPARSE\_POINT** is not specified and:</span></span>

-   <span data-ttu-id="7ecf5-153">Si un fichier existant est ouvert et qu’il s’agit d’un lien symbolique, le handle retourné est un handle vers la cible.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-153">If an existing file is opened and it is a symbolic link, the handle returned is a handle to the target.</span></span>
-   <span data-ttu-id="7ecf5-154">Si l’option **créer \_ toujours**, **tronquer le fichier \_ existant** ou **Supprimer l' \_ indicateur de fichier \_ \_ lors de la \_ fermeture** est spécifiée, le fichier affecté est la cible.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-154">If **CREATE\_ALWAYS**, **TRUNCATE\_EXISTING**, or **FILE\_FLAG\_DELETE\_ON\_CLOSE** are specified, the file affected is the target.</span></span>

## <a name="createhardlink-and-createhardlinktransacted"></a><span data-ttu-id="7ecf5-155">CreateHardLink et CreateHardLinkTransacted</span><span class="sxs-lookup"><span data-stu-id="7ecf5-155">CreateHardLink and CreateHardLinkTransacted</span></span>

<span data-ttu-id="7ecf5-156">Si le chemin d’accès pointe vers un lien symbolique, la fonction crée un lien physique vers la cible.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-156">If the path points to a symbolic link, the function creates a hard link to the target.</span></span>

## <a name="deletefile-and-deletefiletransacted"></a><span data-ttu-id="7ecf5-157">DeleteFile et DeleteFileTransacted</span><span class="sxs-lookup"><span data-stu-id="7ecf5-157">DeleteFile and DeleteFileTransacted</span></span>

<span data-ttu-id="7ecf5-158">Si le chemin d’accès pointe vers un lien symbolique, le lien symbolique est supprimé, et non pas la cible.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-158">If the path points to a symbolic link, the symbolic link is deleted, not the target.</span></span> <span data-ttu-id="7ecf5-159">Pour supprimer une cible, vous devez appeler [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) et spécifier **l' \_ indicateur \_ de fichier supprimer \_ lors de la \_ fermeture**.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-159">To delete a target, you must call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and specify **FILE\_FLAG\_DELETE\_ON\_CLOSE**.</span></span>

## <a name="findfirstchangenotification"></a><span data-ttu-id="7ecf5-160">FindFirstChangeNotification</span><span class="sxs-lookup"><span data-stu-id="7ecf5-160">FindFirstChangeNotification</span></span>

<span data-ttu-id="7ecf5-161">Si le chemin d’accès pointe vers un lien symbolique, le descripteur de notification est créé pour la cible.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-161">If the path points to a symbolic link, the notification handle is created for the target.</span></span> <span data-ttu-id="7ecf5-162">Si une application s’est inscrite pour recevoir des notifications de modification pour un répertoire qui contient des liens symboliques, l’application est notifiée uniquement lorsque les liens symboliques ont été modifiés, et non les fichiers cibles.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-162">If an application has registered to receive change notifications for a directory that contains symbolic links, the application is only notified when the symbolic links have been changed, not the target files.</span></span>

## <a name="findfirstfile-and-findfirstfiletransacted"></a><span data-ttu-id="7ecf5-163">FindFirstFile et FindFirstFileTransacted</span><span class="sxs-lookup"><span data-stu-id="7ecf5-163">FindFirstFile and FindFirstFileTransacted</span></span>

<span data-ttu-id="7ecf5-164">Si le chemin d’accès pointe vers un lien symbolique, le tampon de [**\_ \_ données de recherche Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contient des informations sur le lien symbolique, et non sur la cible.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-164">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="findfirstfileex"></a><span data-ttu-id="7ecf5-165">FindFirstFileEx</span><span class="sxs-lookup"><span data-stu-id="7ecf5-165">FindFirstFileEx</span></span>

<span data-ttu-id="7ecf5-166">Si le chemin d’accès pointe vers un lien symbolique, le tampon de [**\_ \_ données de recherche Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contient des informations sur le lien symbolique, et non sur la cible.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-166">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="findnextfile"></a><span data-ttu-id="7ecf5-167">FindNextFile</span><span class="sxs-lookup"><span data-stu-id="7ecf5-167">FindNextFile</span></span>

<span data-ttu-id="7ecf5-168">Si le chemin d’accès pointe vers un lien symbolique, le tampon de [**\_ \_ données de recherche Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contient des informations sur le lien symbolique, et non sur la cible.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-168">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="getbinarytype"></a><span data-ttu-id="7ecf5-169">GetBinaryType</span><span class="sxs-lookup"><span data-stu-id="7ecf5-169">GetBinaryType</span></span>

<span data-ttu-id="7ecf5-170">Si le chemin d’accès pointe vers un lien symbolique, le fichier cible est utilisé.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-170">If the path points to a symbolic link, the target file is used.</span></span>

## <a name="getcompressedfilesize-and-getcompressedfilesizetransacted"></a><span data-ttu-id="7ecf5-171">GetCompressedFileSize et GetCompressedFileSizeTransacted</span><span class="sxs-lookup"><span data-stu-id="7ecf5-171">GetCompressedFileSize and GetCompressedFileSizeTransacted</span></span>

<span data-ttu-id="7ecf5-172">Si le chemin d’accès pointe vers un lien symbolique, la fonction retourne la taille de fichier de la cible.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-172">If the path points to a symbolic link, the function returns the file size of the target.</span></span>

## <a name="getdiskfreespace"></a><span data-ttu-id="7ecf5-173">GetDiskFreeSpace</span><span class="sxs-lookup"><span data-stu-id="7ecf5-173">GetDiskFreeSpace</span></span>

<span data-ttu-id="7ecf5-174">Si le chemin d’accès pointe vers un lien symbolique, l’opération est effectuée sur la cible.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-174">If the path points to a symbolic link, the operation is performed on the target.</span></span>

## <a name="getdiskfreespaceex"></a><span data-ttu-id="7ecf5-175">GetDiskFreeSpaceEx</span><span class="sxs-lookup"><span data-stu-id="7ecf5-175">GetDiskFreeSpaceEx</span></span>

<span data-ttu-id="7ecf5-176">Si le chemin d’accès pointe vers un lien symbolique, l’opération est effectuée sur la cible.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-176">If the path points to a symbolic link, the operation is performed on the target.</span></span>

## <a name="getfileattributes"></a><span data-ttu-id="7ecf5-177">GetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="7ecf5-177">GetFileAttributes</span></span>

<span data-ttu-id="7ecf5-178">Si le chemin d’accès pointe vers un lien symbolique, la fonction retourne les attributs du lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-178">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="getfileattributesex"></a><span data-ttu-id="7ecf5-179">GetFileAttributesEx</span><span class="sxs-lookup"><span data-stu-id="7ecf5-179">GetFileAttributesEx</span></span>

<span data-ttu-id="7ecf5-180">Si le chemin d’accès pointe vers un lien symbolique, la fonction retourne les attributs du lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-180">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="getfilesecurity"></a><span data-ttu-id="7ecf5-181">GetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="7ecf5-181">GetFileSecurity</span></span>

<span data-ttu-id="7ecf5-182">Si le chemin d’accès pointe vers un lien symbolique, la fonction retourne les attributs du lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-182">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="gettemppath"></a><span data-ttu-id="7ecf5-183">GetTempPath</span><span class="sxs-lookup"><span data-stu-id="7ecf5-183">GetTempPath</span></span>

<span data-ttu-id="7ecf5-184">Si le chemin d’accès pointe vers un lien symbolique, le nom du chemin d’accès temporaire conserve les liens symboliques.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-184">If the path points to a symbolic link, the temp path name maintains any symbolic links.</span></span>

## <a name="getvolumeinformation"></a><span data-ttu-id="7ecf5-185">GetVolumeInformation</span><span class="sxs-lookup"><span data-stu-id="7ecf5-185">GetVolumeInformation</span></span>

<span data-ttu-id="7ecf5-186">Si le chemin d’accès pointe vers un lien symbolique, la fonction retourne les informations de volume de la cible.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-186">If the path points to a symbolic link, the function returns volume information for the target.</span></span>

## <a name="setfileattributes"></a><span data-ttu-id="7ecf5-187">SetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="7ecf5-187">SetFileAttributes</span></span>

<span data-ttu-id="7ecf5-188">Si le chemin d’accès pointe vers un lien symbolique, la fonction récupère les attributs du lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-188">If the path points to a symbolic link, the function retrieves attributes for the symbolic link.</span></span>

## <a name="setfilesecurity"></a><span data-ttu-id="7ecf5-189">SetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="7ecf5-189">SetFileSecurity</span></span>

<span data-ttu-id="7ecf5-190">Si le chemin d’accès pointe vers un lien symbolique, la fonction retourne les attributs du lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="7ecf5-190">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ecf5-191">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7ecf5-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ecf5-192">**CopyFile**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-192">**CopyFile**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfile)
</dt> <dt>

[<span data-ttu-id="7ecf5-193">**CopyFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-193">**CopyFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
</dt> <dt>

[<span data-ttu-id="7ecf5-194">**CopyFileEx**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-194">**CopyFileEx**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
</dt> <dt>

[<span data-ttu-id="7ecf5-195">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-195">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="7ecf5-196">**CreateFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-196">**CreateFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[<span data-ttu-id="7ecf5-197">**CreateHardLink**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-197">**CreateHardLink**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createhardlinka)
</dt> <dt>

[<span data-ttu-id="7ecf5-198">**CreateHardLinkTransacted**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-198">**CreateHardLinkTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
</dt> <dt>

[<span data-ttu-id="7ecf5-199">**DeleteFile**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-199">**DeleteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea)
</dt> <dt>

[<span data-ttu-id="7ecf5-200">**DeleteFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-200">**DeleteFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
</dt> <dt>

[<span data-ttu-id="7ecf5-201">**FindFirstChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-201">**FindFirstChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)
</dt> <dt>

[<span data-ttu-id="7ecf5-202">**FindFirstFile**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-202">**FindFirstFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)
</dt> <dt>

[<span data-ttu-id="7ecf5-203">**FindFirstFileEx**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-203">**FindFirstFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)
</dt> <dt>

[<span data-ttu-id="7ecf5-204">**FindFirstFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-204">**FindFirstFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
</dt> <dt>

[<span data-ttu-id="7ecf5-205">**FindNextFile**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-205">**FindNextFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)
</dt> <dt>

[<span data-ttu-id="7ecf5-206">**GetBinaryType**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-206">**GetBinaryType**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getbinarytypea)
</dt> <dt>

[<span data-ttu-id="7ecf5-207">**GetCompressedFileSize**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-207">**GetCompressedFileSize**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea)
</dt> <dt>

[<span data-ttu-id="7ecf5-208">**GetCompressedFileSizeTransacted**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-208">**GetCompressedFileSizeTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
</dt> <dt>

[<span data-ttu-id="7ecf5-209">**GetDiskFreeSpace**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-209">**GetDiskFreeSpace**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)
</dt> <dt>

[<span data-ttu-id="7ecf5-210">**GetDiskFreeSpaceEx**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-210">**GetDiskFreeSpaceEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)
</dt> <dt>

[<span data-ttu-id="7ecf5-211">**GetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-211">**GetFileAttributes**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[<span data-ttu-id="7ecf5-212">**GetFileAttributesEx**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-212">**GetFileAttributesEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[<span data-ttu-id="7ecf5-213">**GetFileSecurity**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-213">**GetFileSecurity**</span></span>](/windows/desktop/api/winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[<span data-ttu-id="7ecf5-214">**GetTempPath**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-214">**GetTempPath**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)
</dt> <dt>

[<span data-ttu-id="7ecf5-215">**GetVolumeInformation**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-215">**GetVolumeInformation**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)
</dt> <dt>

[<span data-ttu-id="7ecf5-216">**SetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-216">**SetFileAttributes**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[<span data-ttu-id="7ecf5-217">**SetFileSecurity**</span><span class="sxs-lookup"><span data-stu-id="7ecf5-217">**SetFileSecurity**</span></span>](/windows/desktop/api/winbase/nf-winbase-setfilesecuritya)
</dt> </dl>

 

 
