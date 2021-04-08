---
title: Structure BG_FILE_PROGRESS (Deliveryoptimization. h)
description: La structure BG_FILE_PROGRESS fournit des informations de progression relatives aux fichiers, telles que le nombre d’octets transférés.
ms.assetid: 49BDFEEE-D7BF-489A-8BC1-951549B06252
keywords:
- Structure BG_FILE_PROGRESS
topic_type:
- apiref
api_name:
- BG_FILE_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 93507b8aeefa9c0ea16f70f67e221ecc4218427f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742868"
---
# <a name="bg_file_progress-structure"></a><span data-ttu-id="cebd7-104">Structure BG_FILE_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="cebd7-104">BG_FILE_PROGRESS structure</span></span>

<span data-ttu-id="cebd7-105">La structure **BG_FILE_PROGRESS** fournit des informations de progression relatives aux fichiers, telles que le nombre d’octets transférés.</span><span class="sxs-lookup"><span data-stu-id="cebd7-105">The **BG_FILE_PROGRESS** structure provides file-related progress information, such as the number of bytes transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="cebd7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cebd7-106">Syntax</span></span>


```C++
typedef struct _BG_FILE_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  BOOL   Completed;
} BG_FILE_PROGRESS;
```



## <a name="members"></a><span data-ttu-id="cebd7-107">Membres</span><span class="sxs-lookup"><span data-stu-id="cebd7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cebd7-108">**BytesTotal**</span><span class="sxs-lookup"><span data-stu-id="cebd7-108">**BytesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-109">Taille du fichier en octets.</span><span class="sxs-lookup"><span data-stu-id="cebd7-109">Size of the file in bytes.</span></span> <span data-ttu-id="cebd7-110">Si ne peut pas déterminer la taille du fichier (par exemple, si le fichier ou le serveur n’existe pas), la valeur est DO_UNKNOWN_FILE_SIZE.</span><span class="sxs-lookup"><span data-stu-id="cebd7-110">If DO cannot determine the size of the file (for example, if the file or server does not exist), the value is DO_UNKNOWN_FILE_SIZE.</span></span>

<span data-ttu-id="cebd7-111">Si vous téléchargez des plages à partir d’un fichier, **bytesTotal** reflète le nombre total d’octets que vous souhaitez télécharger à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="cebd7-111">If you are downloading ranges from a file, **BytesTotal** reflects the total number of bytes you want to download from the file.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-112">**BytesTransferred**</span><span class="sxs-lookup"><span data-stu-id="cebd7-112">**BytesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-113">Nombre d’octets transférés.</span><span class="sxs-lookup"><span data-stu-id="cebd7-113">Number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="cebd7-114">**Terminé**</span><span class="sxs-lookup"><span data-stu-id="cebd7-114">**Completed**</span></span>
</dt> <dd>

<span data-ttu-id="cebd7-115">Pour les téléchargements, la valeur est **true** si le fichier est disponible pour l’utilisateur ; dans le cas contraire, la valeur est **false**.</span><span class="sxs-lookup"><span data-stu-id="cebd7-115">For downloads, the value is **TRUE** if the file is available to the user; otherwise, the value is **FALSE**.</span></span> <span data-ttu-id="cebd7-116">Les fichiers sont à la disposition de l’utilisateur après l’appel de la méthode [**méthode ibackgroundcopyjob :: Complete**](ibackgroundcopyjob-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="cebd7-116">Files are available to the user after calling the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span> <span data-ttu-id="cebd7-117">Si la méthode **Complete** génère une erreur temporaire, les fichiers traités avant l’erreur sont à la disposition de l’utilisateur. les autres ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="cebd7-117">If the **Complete** method generates a transient error, those files processed before the error occurred are available to the user; the others are not.</span></span> <span data-ttu-id="cebd7-118">Utilisez le membre **terminé** pour déterminer si le fichier est disponible pour l’utilisateur une fois l' **opération terminée** .</span><span class="sxs-lookup"><span data-stu-id="cebd7-118">Use the **Completed** member to determine if the file is available to the user when **Complete** fails.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cebd7-119">Notes</span><span class="sxs-lookup"><span data-stu-id="cebd7-119">Remarks</span></span>

<span data-ttu-id="cebd7-120">Pour déterminer si le fichier doit être transféré, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="cebd7-120">To determine if DO transferred the file, you can:</span></span>

-   <span data-ttu-id="cebd7-121">Comparez **bytesTransferred** à **bytesTotal**.</span><span class="sxs-lookup"><span data-stu-id="cebd7-121">Compare **BytesTransferred** to **BytesTotal**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cebd7-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cebd7-122">Requirements</span></span>



| <span data-ttu-id="cebd7-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cebd7-123">Requirement</span></span> | <span data-ttu-id="cebd7-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="cebd7-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cebd7-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cebd7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cebd7-126">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cebd7-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cebd7-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cebd7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cebd7-128">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cebd7-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cebd7-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="cebd7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="cebd7-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="cebd7-130"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cebd7-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cebd7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cebd7-132">**BG_JOB_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="cebd7-132">**BG_JOB_PROGRESS**</span></span>](bg-job-progress.md)
</dt> <dt>

[<span data-ttu-id="cebd7-133">**IBackgroundCopyFile :: GetProgress**</span><span class="sxs-lookup"><span data-stu-id="cebd7-133">**IBackgroundCopyFile::GetProgress**</span></span>](ibackgroundcopyfile-getprogress-method.md)
</dt> </dl>

 

 





