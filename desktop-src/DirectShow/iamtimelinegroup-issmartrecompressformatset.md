---
description: La méthode IsSmartRecompressFormatSet détermine si un format de recompression intelligente a été défini pour le groupe.
ms.assetid: d2b7ecc7-2348-402d-8d96-e0922e06a685
title: 'IAMTimelineGroup :: IsSmartRecompressFormatSet, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.IsSmartRecompressFormatSet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 078649fd42cd44596ff27558b29d14b6f8cbeddc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539686"
---
# <a name="iamtimelinegroupissmartrecompressformatset-method"></a><span data-ttu-id="9ddd9-103">IAMTimelineGroup :: IsSmartRecompressFormatSet, méthode</span><span class="sxs-lookup"><span data-stu-id="9ddd9-103">IAMTimelineGroup::IsSmartRecompressFormatSet method</span></span>

> [!Note]  
> <span data-ttu-id="9ddd9-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-104">\[Deprecated.</span></span> <span data-ttu-id="9ddd9-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9ddd9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9ddd9-106">La `IsSmartRecompressFormatSet` méthode détermine si un format de recompression intelligente a été défini pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-106">The `IsSmartRecompressFormatSet` method determines whether a smart recompression format was set for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ddd9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ddd9-107">Syntax</span></span>


```C++
HRESULT IsSmartRecompressFormatSet(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="9ddd9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ddd9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ddd9-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="9ddd9-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="9ddd9-110">Reçoit une valeur booléenne indiquant si un format de compression a été défini.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-110">Receives a Boolean value indicating whether a compression format was set.</span></span> <span data-ttu-id="9ddd9-111">Si la **valeur est true**, un format de compression a été défini.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-111">If **TRUE**, a compression format was set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ddd9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9ddd9-112">Return value</span></span>

<span data-ttu-id="9ddd9-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9ddd9-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9ddd9-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ddd9-115">Notes</span><span class="sxs-lookup"><span data-stu-id="9ddd9-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9ddd9-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9ddd9-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9ddd9-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9ddd9-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9ddd9-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ddd9-119">Requirements</span></span>



| <span data-ttu-id="9ddd9-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ddd9-120">Requirement</span></span> | <span data-ttu-id="9ddd9-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ddd9-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ddd9-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ddd9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9ddd9-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ddd9-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9ddd9-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9ddd9-124">Library</span></span><br/> | <dl> <span data-ttu-id="9ddd9-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ddd9-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ddd9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ddd9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ddd9-127">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="9ddd9-127">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="9ddd9-128">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="9ddd9-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




