---
title: Message MMIOM_SEEK (mmsystem. h)
description: Le \_ message de recherche MMIOM est envoyé à une procédure d’e/s par la fonction mmioSeek pour demander que la position actuelle du fichier soit déplacée.
ms.assetid: 428b231a-6e00-4458-9ba2-e9b0b028843a
keywords:
- Message MMIOM_SEEK Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4855ec4e610f1456e1bf26ee05800e31933f05fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510781"
---
# <a name="mmiom_seek-message"></a><span data-ttu-id="73cc4-104">MMIOM le \_ message de recherche</span><span class="sxs-lookup"><span data-stu-id="73cc4-104">MMIOM\_SEEK message</span></span>

<span data-ttu-id="73cc4-105">Le message de **\_ recherche MMIOM** est envoyé à une procédure d’e/s par la fonction [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) pour demander que la position actuelle du fichier soit déplacée.</span><span class="sxs-lookup"><span data-stu-id="73cc4-105">The **MMIOM\_SEEK** message is sent to an I/O procedure by the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function to request that the current file position be moved.</span></span>


```C++
MMIOM_SEEK 
lParam1 = (LPARAM) lNewFilePos 
lParam2 = (LPARAM) lChangeFlag 
```



## <a name="parameters"></a><span data-ttu-id="73cc4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73cc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73cc4-107"><span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*</span><span class="sxs-lookup"><span data-stu-id="73cc4-107"><span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*</span></span>
</dt> <dd>

<span data-ttu-id="73cc4-108">Nouvelle position de fichier.</span><span class="sxs-lookup"><span data-stu-id="73cc4-108">New file position.</span></span> <span data-ttu-id="73cc4-109">La signification de cette valeur dépend de l’indicateur spécifié dans **lChangeFlag**.</span><span class="sxs-lookup"><span data-stu-id="73cc4-109">The meaning of this value is dependent on the flag specified in **lChangeFlag**.</span></span>

</dd> <dt>

<span data-ttu-id="73cc4-110"><span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*</span><span class="sxs-lookup"><span data-stu-id="73cc4-110"><span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*</span></span>
</dt> <dd>

<span data-ttu-id="73cc4-111">Indicateur spécifiant le mode de modification de la position de fichier.</span><span class="sxs-lookup"><span data-stu-id="73cc4-111">Flag specifying how the file position is changed.</span></span> <span data-ttu-id="73cc4-112">Les valeurs suivantes sont définies :</span><span class="sxs-lookup"><span data-stu-id="73cc4-112">The following values are defined:</span></span>



| <span data-ttu-id="73cc4-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73cc4-113">Requirement</span></span> | <span data-ttu-id="73cc4-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="73cc4-114">Value</span></span> |
|-----------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73cc4-115">SEEK \_ cur</span><span class="sxs-lookup"><span data-stu-id="73cc4-115">SEEK\_CUR</span></span> | <span data-ttu-id="73cc4-116">Déplacez la position de fichier en octets *lNewFilePos* à partir de la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="73cc4-116">Move the file position to be *lNewFilePos* bytes from the current position.</span></span> <span data-ttu-id="73cc4-117">*lNewFilePos* peut être positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="73cc4-117">*lNewFilePos* can be positive or negative.</span></span> |
| <span data-ttu-id="73cc4-118">fin de recherche \_</span><span class="sxs-lookup"><span data-stu-id="73cc4-118">SEEK\_END</span></span> | <span data-ttu-id="73cc4-119">Déplacez la position de fichier à *lNewFilePos* octets à partir de la fin du fichier.</span><span class="sxs-lookup"><span data-stu-id="73cc4-119">Move the file position to be *lNewFilePos* bytes from the end of the file.</span></span>                                             |
| <span data-ttu-id="73cc4-120">ensemble de recherches \_</span><span class="sxs-lookup"><span data-stu-id="73cc4-120">SEEK\_SET</span></span> | <span data-ttu-id="73cc4-121">Déplacez la position de fichier à *lNewFilePos* octets à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="73cc4-121">Move the file position to be *lNewFilePos* bytes from the beginning of the file.</span></span>                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73cc4-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="73cc4-122">Return Value</span></span>

<span data-ttu-id="73cc4-123">Retourne la nouvelle position de fichier.</span><span class="sxs-lookup"><span data-stu-id="73cc4-123">Returns the new file position.</span></span> <span data-ttu-id="73cc4-124">En cas d’erreur, la valeur de retour est 1.</span><span class="sxs-lookup"><span data-stu-id="73cc4-124">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="73cc4-125">Notes</span><span class="sxs-lookup"><span data-stu-id="73cc4-125">Remarks</span></span>

<span data-ttu-id="73cc4-126">La procédure d’e/s est responsable de la gestion de la position de fichier actuelle dans le membre **lDiskOffset** de la structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="73cc4-126">The I/O procedure is responsible for maintaining the current file position in the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="73cc4-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73cc4-127">Requirements</span></span>



| <span data-ttu-id="73cc4-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73cc4-128">Requirement</span></span> | <span data-ttu-id="73cc4-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="73cc4-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73cc4-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73cc4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="73cc4-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73cc4-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="73cc4-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73cc4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="73cc4-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73cc4-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="73cc4-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="73cc4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="73cc4-135"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73cc4-135"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

