---
description: 'Non pris en charge. Appelez la méthode IAMTimeline :: AddGroup à la place.'
ms.assetid: dd671fa5-ed5a-46e2-b4bd-a37f0e7458ca
title: 'IAMTimelineGroup :: SetTimeline, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 166d65f5ae9a14f58ed7b20763ab5e4a136df598
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525597"
---
# <a name="iamtimelinegroupsettimeline-method"></a><span data-ttu-id="e1856-104">IAMTimelineGroup :: SetTimeline, méthode</span><span class="sxs-lookup"><span data-stu-id="e1856-104">IAMTimelineGroup::SetTimeline method</span></span>

> [!Note]  
> <span data-ttu-id="e1856-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e1856-105">\[Deprecated.</span></span> <span data-ttu-id="e1856-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e1856-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e1856-107">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e1856-107">Not supported.</span></span> <span data-ttu-id="e1856-108">Appelez la méthode [**IAMTimeline :: addgroup**](iamtimeline-addgroup.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="e1856-108">Call the [**IAMTimeline::AddGroup**](iamtimeline-addgroup.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1856-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1856-109">Syntax</span></span>


```C++
HRESULT SetTimeline(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="e1856-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1856-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1856-111">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="e1856-111">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="e1856-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="e1856-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1856-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1856-113">Return value</span></span>

<span data-ttu-id="e1856-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e1856-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e1856-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e1856-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1856-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e1856-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e1856-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="e1856-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e1856-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e1856-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e1856-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e1856-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e1856-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1856-120">Requirements</span></span>



| <span data-ttu-id="e1856-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1856-121">Requirement</span></span> | <span data-ttu-id="e1856-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1856-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1856-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1856-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e1856-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1856-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e1856-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e1856-125">Library</span></span><br/> | <dl> <span data-ttu-id="e1856-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1856-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1856-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1856-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1856-128">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="e1856-128">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> </dl>

 

 




