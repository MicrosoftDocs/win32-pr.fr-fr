---
description: 'Méthode IAMTimeline :: SetInterestRange-non implémentée.'
ms.assetid: b803ba33-d698-449f-a540-3981c4f0826a
title: 'IAMTimeline :: SetInterestRange, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetInterestRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 23485bbdc2292e0d341e3fef0646fb68616698c4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119567"
---
# <a name="iamtimelinesetinterestrange-method"></a><span data-ttu-id="daf16-103">IAMTimeline :: SetInterestRange, méthode</span><span class="sxs-lookup"><span data-stu-id="daf16-103">IAMTimeline::SetInterestRange method</span></span>

> [!Note]  
> <span data-ttu-id="daf16-104">\[Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="daf16-104">\[Deprecated.</span></span> <span data-ttu-id="daf16-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="daf16-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="daf16-106">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="daf16-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="daf16-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="daf16-107">Syntax</span></span>


```C++
HRESULT SetInterestRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="daf16-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="daf16-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daf16-109">*Start*</span><span class="sxs-lookup"><span data-stu-id="daf16-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="daf16-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="daf16-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="daf16-111">*Stop*</span><span class="sxs-lookup"><span data-stu-id="daf16-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="daf16-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="daf16-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daf16-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="daf16-113">Return value</span></span>

<span data-ttu-id="daf16-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="daf16-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="daf16-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="daf16-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="daf16-116">Notes </span><span class="sxs-lookup"><span data-stu-id="daf16-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="daf16-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="daf16-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="daf16-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="daf16-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="daf16-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="daf16-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="daf16-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="daf16-120">Requirements</span></span>



| <span data-ttu-id="daf16-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="daf16-121">Requirement</span></span> | <span data-ttu-id="daf16-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="daf16-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="daf16-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="daf16-123">Header</span></span><br/>  | <dl> <span data-ttu-id="daf16-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="daf16-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="daf16-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="daf16-125">Library</span></span><br/> | <dl> <span data-ttu-id="daf16-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="daf16-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daf16-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="daf16-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daf16-128">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="daf16-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




