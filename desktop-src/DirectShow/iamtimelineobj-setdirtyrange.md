---
description: 'Méthode IAMTimelineObj :: SetDirtyRange-non implémentée.'
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
ms.openlocfilehash: 7e3f70e5ba9d01733df154911c4f40d2b9d33776
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119487"
---
# <a name="iamtimelineobjsetdirtyrange-method"></a><span data-ttu-id="a65ee-103">IAMTimelineObj :: SetDirtyRange, méthode</span><span class="sxs-lookup"><span data-stu-id="a65ee-103">IAMTimelineObj::SetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="a65ee-104">\[Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="a65ee-104">\[Deprecated.</span></span> <span data-ttu-id="a65ee-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a65ee-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a65ee-106">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="a65ee-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="a65ee-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a65ee-107">Syntax</span></span>


```C++
HRESULT SetDirtyRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="a65ee-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a65ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a65ee-109">*Start*</span><span class="sxs-lookup"><span data-stu-id="a65ee-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="a65ee-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="a65ee-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a65ee-111">*Stop*</span><span class="sxs-lookup"><span data-stu-id="a65ee-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="a65ee-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="a65ee-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a65ee-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a65ee-113">Return value</span></span>

<span data-ttu-id="a65ee-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a65ee-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a65ee-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a65ee-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a65ee-116">Notes </span><span class="sxs-lookup"><span data-stu-id="a65ee-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a65ee-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="a65ee-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a65ee-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a65ee-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a65ee-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a65ee-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a65ee-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a65ee-120">Requirements</span></span>



| <span data-ttu-id="a65ee-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a65ee-121">Requirement</span></span> | <span data-ttu-id="a65ee-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a65ee-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a65ee-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="a65ee-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a65ee-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a65ee-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a65ee-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a65ee-125">Library</span></span><br/> | <dl> <span data-ttu-id="a65ee-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a65ee-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a65ee-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a65ee-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a65ee-128">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="a65ee-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




