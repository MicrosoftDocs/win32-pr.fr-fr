---
description: Non pris en charge.
ms.assetid: 7f97b1c4-0508-45a5-a6fd-5dae17f0fa60
title: 'IAMTimelineObj :: GetDirtyRange, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d4f82b34c70cafd49bf21d662cf8b397b8d6316d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540095"
---
# <a name="iamtimelineobjgetdirtyrange-method"></a><span data-ttu-id="287fb-103">IAMTimelineObj :: GetDirtyRange, méthode</span><span class="sxs-lookup"><span data-stu-id="287fb-103">IAMTimelineObj::GetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="287fb-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="287fb-104">\[Deprecated.</span></span> <span data-ttu-id="287fb-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="287fb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="287fb-106">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="287fb-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="287fb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="287fb-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="287fb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="287fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="287fb-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="287fb-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="287fb-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="287fb-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="287fb-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="287fb-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="287fb-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="287fb-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="287fb-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="287fb-113">Return value</span></span>

<span data-ttu-id="287fb-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="287fb-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="287fb-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="287fb-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="287fb-116">Notes</span><span class="sxs-lookup"><span data-stu-id="287fb-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="287fb-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="287fb-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="287fb-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="287fb-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="287fb-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="287fb-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="287fb-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="287fb-120">Requirements</span></span>



| <span data-ttu-id="287fb-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="287fb-121">Requirement</span></span> | <span data-ttu-id="287fb-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="287fb-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="287fb-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="287fb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="287fb-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="287fb-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="287fb-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="287fb-125">Library</span></span><br/> | <dl> <span data-ttu-id="287fb-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="287fb-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="287fb-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="287fb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="287fb-128">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="287fb-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




