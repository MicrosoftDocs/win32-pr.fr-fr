---
title: Structure BG_FILE_RANGE (Deliveryoptimization. h)
description: La structure BG_FILE_RANGE identifie une plage d’octets à télécharger à partir d’un fichier.
ms.assetid: 58993C51-E42E-4E44-9E8A-15E982B25413
keywords:
- Structure BG_FILE_RANGE
topic_type:
- apiref
api_name:
- BG_FILE_RANGE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cedabfb066a5905adb2ed8eac9996fd77c0e12be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385092"
---
# <a name="bg_file_range-structure"></a><span data-ttu-id="7421b-104">Structure BG_FILE_RANGE</span><span class="sxs-lookup"><span data-stu-id="7421b-104">BG_FILE_RANGE structure</span></span>

<span data-ttu-id="7421b-105">La structure **BG_FILE_RANGE** identifie une plage d’octets à télécharger à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="7421b-105">The **BG_FILE_RANGE** structure identifies a range of bytes to download from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7421b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7421b-106">Syntax</span></span>


```C++
typedef struct {
  UINT64 InitialOffset;
  UINT64 Length;
} BG_FILE_RANGE;
```



## <a name="members"></a><span data-ttu-id="7421b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7421b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7421b-108">**InitialOffset**</span><span class="sxs-lookup"><span data-stu-id="7421b-108">**InitialOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7421b-109">Décalage de base zéro au début de la plage d’octets à télécharger à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="7421b-109">Zero-based offset to the beginning of the range of bytes to download from a file.</span></span>

</dd> <dt>

<span data-ttu-id="7421b-110">**Durée**</span><span class="sxs-lookup"><span data-stu-id="7421b-110">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="7421b-111">Longueur de la plage, en octets.</span><span class="sxs-lookup"><span data-stu-id="7421b-111">The length of the range, in bytes.</span></span> <span data-ttu-id="7421b-112">Ne spécifiez pas de longueur égale à zéro octet.</span><span class="sxs-lookup"><span data-stu-id="7421b-112">Do not specify a zero byte length.</span></span> <span data-ttu-id="7421b-113">Pour indiquer que la plage s’étend jusqu’à la fin du fichier, spécifiez **BG_LENGTH_TO_EOF**.</span><span class="sxs-lookup"><span data-stu-id="7421b-113">To indicate that the range extends to the end of the file, specify **BG_LENGTH_TO_EOF**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7421b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7421b-114">Remarks</span></span>

<span data-ttu-id="7421b-115">La plage doit exister dans le fichier ou générer une erreur **DO_E_INVALID_RANGE** .</span><span class="sxs-lookup"><span data-stu-id="7421b-115">The range must exist in the file or DO generates an **DO_E_INVALID_RANGE** error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7421b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7421b-116">Requirements</span></span>



| <span data-ttu-id="7421b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7421b-117">Requirement</span></span> | <span data-ttu-id="7421b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7421b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7421b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7421b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7421b-120">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7421b-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7421b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7421b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7421b-122">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7421b-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7421b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7421b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7421b-124"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="7421b-124"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7421b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7421b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7421b-126">**IBackgroundCopyFile2::GetFileRanges**</span><span class="sxs-lookup"><span data-stu-id="7421b-126">**IBackgroundCopyFile2::GetFileRanges**</span></span>](ibackgroundcopyfile2-getfileranges-method.md)
</dt> </dl>

 

 





