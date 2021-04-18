---
description: La méthode TransitionsEnabled détermine si les transitions sont activées.
ms.assetid: c961d8d7-4509-444b-a49f-6ab79fc31f7e
title: 'IAMTimeline :: TransitionsEnabled, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.TransitionsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7116ccf4ff2015934c9071f4ce2ef073656b89c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543244"
---
# <a name="iamtimelinetransitionsenabled-method"></a><span data-ttu-id="e76fc-103">IAMTimeline :: TransitionsEnabled, méthode</span><span class="sxs-lookup"><span data-stu-id="e76fc-103">IAMTimeline::TransitionsEnabled method</span></span>

> [!Note]  
> <span data-ttu-id="e76fc-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e76fc-104">\[Deprecated.</span></span> <span data-ttu-id="e76fc-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e76fc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e76fc-106">La méthode **TransitionsEnabled** détermine si les transitions sont activées.</span><span class="sxs-lookup"><span data-stu-id="e76fc-106">The **TransitionsEnabled** method determines whether transitions are enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="e76fc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e76fc-107">Syntax</span></span>


```C++
HRESULT TransitionsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="e76fc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e76fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e76fc-109">*pfEnabled*</span><span class="sxs-lookup"><span data-stu-id="e76fc-109">*pfEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="e76fc-110">Reçoit une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="e76fc-110">Receives a Boolean value.</span></span> <span data-ttu-id="e76fc-111">Si la **valeur est true**, les transitions sont activées.</span><span class="sxs-lookup"><span data-stu-id="e76fc-111">If **TRUE**, transitions are enabled.</span></span> <span data-ttu-id="e76fc-112">Dans le cas contraire, les transitions sont désactivées.</span><span class="sxs-lookup"><span data-stu-id="e76fc-112">Otherwise, transitions are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e76fc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e76fc-113">Return value</span></span>

<span data-ttu-id="e76fc-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e76fc-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e76fc-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e76fc-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e76fc-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e76fc-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e76fc-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="e76fc-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e76fc-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e76fc-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e76fc-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e76fc-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e76fc-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e76fc-120">Requirements</span></span>



| <span data-ttu-id="e76fc-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e76fc-121">Requirement</span></span> | <span data-ttu-id="e76fc-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e76fc-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e76fc-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e76fc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e76fc-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e76fc-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e76fc-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e76fc-125">Library</span></span><br/> | <dl> <span data-ttu-id="e76fc-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e76fc-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e76fc-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e76fc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e76fc-128">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="e76fc-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="e76fc-129">**IAMTimeline::EnableTransitions**</span><span class="sxs-lookup"><span data-stu-id="e76fc-129">**IAMTimeline::EnableTransitions**</span></span>](iamtimeline-enabletransitions.md)
</dt> <dt>

[<span data-ttu-id="e76fc-130">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="e76fc-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




