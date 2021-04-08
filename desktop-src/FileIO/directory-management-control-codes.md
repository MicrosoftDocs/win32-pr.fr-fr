---
description: Codes de contrôle utilisés avec la compression et la décompression de fichiers et avec des points d’analyse.
ms.assetid: e2e671c7-ef65-4401-8016-649e86f84fec
title: Codes de contrôle de gestion d’annuaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef0463860e3c899178ec5b8f9d44bd05cf4278e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867694"
---
# <a name="directory-management-control-codes"></a><span data-ttu-id="dec9f-103">Codes de contrôle de gestion d’annuaire</span><span class="sxs-lookup"><span data-stu-id="dec9f-103">Directory Management Control Codes</span></span>

<span data-ttu-id="dec9f-104">Les codes de contrôle suivants sont utilisés avec la [compression et la décompression des fichiers](file-compression-and-decompression.md).</span><span class="sxs-lookup"><span data-stu-id="dec9f-104">The following control codes are used with [file compression and decompression](file-compression-and-decompression.md).</span></span>



| <span data-ttu-id="dec9f-105">Code de contrôle</span><span class="sxs-lookup"><span data-stu-id="dec9f-105">Control Code</span></span>                                             | <span data-ttu-id="dec9f-106">Signification</span><span class="sxs-lookup"><span data-stu-id="dec9f-106">Meaning</span></span>                                                                                                                                     |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dec9f-107">**FSCTL \_ recevoir la \_ compression**</span><span class="sxs-lookup"><span data-stu-id="dec9f-107">**FSCTL\_GET\_COMPRESSION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) | <span data-ttu-id="dec9f-108">Récupère l’état de compression actuel d’un fichier ou d’un répertoire sur un volume dont le système de fichiers prend en charge la compression par flux.</span><span class="sxs-lookup"><span data-stu-id="dec9f-108">Retrieves the current compression state of a file or directory on a volume whose file system supports per-stream compression.</span></span><br/>    |
| [<span data-ttu-id="dec9f-109">**FSCTL \_ définir la \_ compression**</span><span class="sxs-lookup"><span data-stu-id="dec9f-109">**FSCTL\_SET\_COMPRESSION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) | <span data-ttu-id="dec9f-110">Définit l’état de compression d’un fichier ou d’un répertoire sur un volume dont le système de fichiers prend en charge la compression par fichier et par répertoire.</span><span class="sxs-lookup"><span data-stu-id="dec9f-110">Sets the compression state of a file or directory on a volume whose file system supports per-file and per-directory compression.</span></span><br/> |



 

<span data-ttu-id="dec9f-111">Les codes de contrôle suivants sont utilisés avec des [points d’analyse](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="dec9f-111">The following control codes are used with [reparse points](reparse-points.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dec9f-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="dec9f-112">In this section</span></span>



| <span data-ttu-id="dec9f-113">Code de contrôle</span><span class="sxs-lookup"><span data-stu-id="dec9f-113">Control Code</span></span>                                                                   | <span data-ttu-id="dec9f-114">Description</span><span class="sxs-lookup"><span data-stu-id="dec9f-114">Description</span></span>                                                                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dec9f-115">**FSCTL \_ supprimer le \_ point d’analyse \_**</span><span class="sxs-lookup"><span data-stu-id="dec9f-115">**FSCTL\_DELETE\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point)<br/> | <span data-ttu-id="dec9f-116">Supprime un point d’analyse du fichier ou du répertoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="dec9f-116">Deletes a reparse point from the specified file or directory.</span></span><br/>                                              |
| [<span data-ttu-id="dec9f-117">**FSCTL \_ recevoir le \_ point d’analyse \_**</span><span class="sxs-lookup"><span data-stu-id="dec9f-117">**FSCTL\_GET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)<br/>       | <span data-ttu-id="dec9f-118">Récupère les données du point d’analyse associées au fichier ou au répertoire identifié par le handle spécifié.</span><span class="sxs-lookup"><span data-stu-id="dec9f-118">Retrieves the reparse point data associated with the file or directory identified by the specified handle.</span></span><br/> |
| [<span data-ttu-id="dec9f-119">**FSCTL \_ définir le \_ point d’analyse \_**</span><span class="sxs-lookup"><span data-stu-id="dec9f-119">**FSCTL\_SET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)<br/>       | <span data-ttu-id="dec9f-120">Définit un point d’analyse sur un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="dec9f-120">Sets a reparse point on a file or directory.</span></span><br/>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="dec9f-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dec9f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dec9f-122">Codes de contrôle de gestion des fichiers</span><span class="sxs-lookup"><span data-stu-id="dec9f-122">File Management Control Codes</span></span>](file-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="dec9f-123">Codes de contrôle de gestion des volumes</span><span class="sxs-lookup"><span data-stu-id="dec9f-123">Volume Management Control Codes</span></span>](volume-management-control-codes.md)
</dt> </dl>

 

