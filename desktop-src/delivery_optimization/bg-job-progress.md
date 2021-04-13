---
title: Structure BG_JOB_PROGRESS (Deliveryoptimization. h)
description: La structure BG_JOB_PROGRESS fournit des informations de progression relatives aux tâches, telles que le nombre d’octets et de fichiers transférés. Pour les travaux de chargement, la progression s’applique au fichier de téléchargement, pas au fichier de réponse.
ms.assetid: F07BBDDE-FD34-4779-9E17-3789A8098616
keywords:
- Structure BG_JOB_PROGRESS
topic_type:
- apiref
api_name:
- BG_JOB_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e45c4a2833f80644ff763fc85a6846f9858fb3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509089"
---
# <a name="bg_job_progress-structure"></a><span data-ttu-id="fbf6a-105">Structure BG_JOB_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="fbf6a-105">BG_JOB_PROGRESS structure</span></span>

<span data-ttu-id="fbf6a-106">La structure **BG_JOB_PROGRESS** fournit des informations de progression relatives aux tâches, telles que le nombre d’octets et de fichiers transférés.</span><span class="sxs-lookup"><span data-stu-id="fbf6a-106">The **BG_JOB_PROGRESS** structure provides job-related progress information, such as the number of bytes and files transferred.</span></span> <span data-ttu-id="fbf6a-107">Pour les travaux de chargement, la progression s’applique au fichier de téléchargement, pas au fichier de réponse.</span><span class="sxs-lookup"><span data-stu-id="fbf6a-107">For upload jobs, the progress applies to the upload file, not the reply file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf6a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbf6a-108">Syntax</span></span>


```C++
typedef struct _BG_JOB_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  ULONG  FilesTotal;
  ULONG  FilesTransferred;
} BG_JOB_PROGRESS;
```



## <a name="members"></a><span data-ttu-id="fbf6a-109">Membres</span><span class="sxs-lookup"><span data-stu-id="fbf6a-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="fbf6a-110">**BytesTotal**</span><span class="sxs-lookup"><span data-stu-id="fbf6a-110">**BytesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="fbf6a-111">Nombre total d’octets à transférer pour tous les fichiers du travail.</span><span class="sxs-lookup"><span data-stu-id="fbf6a-111">Total number of bytes to transfer for all files in the job.</span></span> <span data-ttu-id="fbf6a-112">Si la valeur est BG_SIZE_UNKNOWN, la taille totale de tous les fichiers du travail n’a pas été déterminée.</span><span class="sxs-lookup"><span data-stu-id="fbf6a-112">If the value is BG_SIZE_UNKNOWN, the total size of all files in the job has not been determined.</span></span> <span data-ttu-id="fbf6a-113">NE définissez pas cette valeur si elle ne peut pas déterminer la taille de l’un des fichiers.</span><span class="sxs-lookup"><span data-stu-id="fbf6a-113">DO does not set this value if it cannot determine the size of one of the files.</span></span> <span data-ttu-id="fbf6a-114">Par exemple, si le fichier ou le serveur spécifié n’existe pas, ne pouvez pas déterminer la taille du fichier.</span><span class="sxs-lookup"><span data-stu-id="fbf6a-114">For example, if the specified file or server does not exist, DO cannot determine the size of the file.</span></span>

<span data-ttu-id="fbf6a-115">Si vous téléchargez des plages à partir du fichier, **bytesTotal** comprend le nombre total d’octets que vous souhaitez télécharger à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="fbf6a-115">If you are downloading ranges from the file, **BytesTotal** includes the total number of bytes you want to download from the file.</span></span>

</dd> <dt>

<span data-ttu-id="fbf6a-116">**BytesTransferred**</span><span class="sxs-lookup"><span data-stu-id="fbf6a-116">**BytesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="fbf6a-117">Nombre d’octets transférés.</span><span class="sxs-lookup"><span data-stu-id="fbf6a-117">Number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="fbf6a-118">**FilesTotal**</span><span class="sxs-lookup"><span data-stu-id="fbf6a-118">**FilesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="fbf6a-119">Nombre total de fichiers à transférer pour ce travail.</span><span class="sxs-lookup"><span data-stu-id="fbf6a-119">Total number of files to transfer for this job.</span></span>

</dd> <dt>

<span data-ttu-id="fbf6a-120">**FilesTransferred**</span><span class="sxs-lookup"><span data-stu-id="fbf6a-120">**FilesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="fbf6a-121">Nombre de fichiers transférés.</span><span class="sxs-lookup"><span data-stu-id="fbf6a-121">Number of files transferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fbf6a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbf6a-122">Requirements</span></span>



| <span data-ttu-id="fbf6a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbf6a-123">Requirement</span></span> | <span data-ttu-id="fbf6a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbf6a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf6a-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbf6a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf6a-126">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbf6a-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fbf6a-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbf6a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf6a-128">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbf6a-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fbf6a-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="fbf6a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbf6a-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbf6a-130"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbf6a-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbf6a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf6a-132">**BG_FILE_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="fbf6a-132">**BG_FILE_PROGRESS**</span></span>](bg-file-progress.md)
</dt> <dt>

[<span data-ttu-id="fbf6a-133">**Méthode ibackgroundcopyjob :: GetProgress**</span><span class="sxs-lookup"><span data-stu-id="fbf6a-133">**IBackgroundCopyJob::GetProgress**</span></span>](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





