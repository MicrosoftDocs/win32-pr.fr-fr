---
description: 'IAMTimelineObj :: GetDirtyRange2, méthode non prise en charge.'
ms.assetid: 3acd36f2-52f4-4734-a753-c6a6ce7e9187
title: 'IAMTimelineObj :: GetDirtyRange2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetDirtyRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 14c573403bf946b54bbfcc74ae41145a3f1c5c7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119517"
---
# <a name="iamtimelineobjgetdirtyrange2-method"></a><span data-ttu-id="c6cdf-103">IAMTimelineObj :: GetDirtyRange2, méthode</span><span class="sxs-lookup"><span data-stu-id="c6cdf-103">IAMTimelineObj::GetDirtyRange2 method</span></span>

> [!Note]  
> <span data-ttu-id="c6cdf-104">\[Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-104">\[Deprecated.</span></span> <span data-ttu-id="c6cdf-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c6cdf-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c6cdf-106">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6cdf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6cdf-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="c6cdf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6cdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6cdf-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="c6cdf-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="c6cdf-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c6cdf-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="c6cdf-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="c6cdf-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6cdf-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c6cdf-113">Return value</span></span>

<span data-ttu-id="c6cdf-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c6cdf-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c6cdf-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6cdf-116">Notes </span><span class="sxs-lookup"><span data-stu-id="c6cdf-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c6cdf-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c6cdf-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c6cdf-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c6cdf-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c6cdf-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6cdf-120">Requirements</span></span>



| <span data-ttu-id="c6cdf-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6cdf-121">Requirement</span></span> | <span data-ttu-id="c6cdf-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6cdf-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6cdf-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c6cdf-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c6cdf-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6cdf-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c6cdf-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c6cdf-125">Library</span></span><br/> | <dl> <span data-ttu-id="c6cdf-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6cdf-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6cdf-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6cdf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6cdf-128">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="c6cdf-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




