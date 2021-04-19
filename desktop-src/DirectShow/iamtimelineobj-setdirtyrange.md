---
description: Non implémenté.
ms.assetid: f3be3b5a-7ab9-44ca-8a03-33fb905d3aea
title: 'IAMTimelineObj :: SetDirtyRange, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b8f0adee44de03560b347122a9c9cbdf500db897
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539989"
---
# <a name="iamtimelineobjsetdirtyrange-method"></a><span data-ttu-id="0e9d0-103">IAMTimelineObj :: SetDirtyRange, méthode</span><span class="sxs-lookup"><span data-stu-id="0e9d0-103">IAMTimelineObj::SetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="0e9d0-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0e9d0-104">\[Deprecated.</span></span> <span data-ttu-id="0e9d0-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0e9d0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0e9d0-106">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0e9d0-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e9d0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e9d0-107">Syntax</span></span>


```C++
HRESULT SetDirtyRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="0e9d0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e9d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e9d0-109">*Start*</span><span class="sxs-lookup"><span data-stu-id="0e9d0-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="0e9d0-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="0e9d0-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0e9d0-111">*Stop*</span><span class="sxs-lookup"><span data-stu-id="0e9d0-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="0e9d0-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="0e9d0-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e9d0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e9d0-113">Return value</span></span>

<span data-ttu-id="0e9d0-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0e9d0-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0e9d0-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0e9d0-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e9d0-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0e9d0-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0e9d0-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="0e9d0-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0e9d0-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0e9d0-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0e9d0-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0e9d0-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0e9d0-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e9d0-120">Requirements</span></span>



| <span data-ttu-id="0e9d0-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e9d0-121">Requirement</span></span> | <span data-ttu-id="0e9d0-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e9d0-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e9d0-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e9d0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0e9d0-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e9d0-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0e9d0-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0e9d0-125">Library</span></span><br/> | <dl> <span data-ttu-id="0e9d0-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e9d0-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e9d0-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e9d0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e9d0-128">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="0e9d0-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




