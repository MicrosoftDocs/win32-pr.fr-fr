---
description: 'Méthode IAMTimelineTrack :: MoveEverythingBy-cette méthode n’est pas prise en charge.'
ms.assetid: f263116b-e492-4468-9829-124a096c9d74
title: 'IAMTimelineTrack :: MoveEverythingBy, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.MoveEverythingBy
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fe85cf17c92c0809189e12e8ad40ceb1d1f3fd25
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094587"
---
# <a name="iamtimelinetrackmoveeverythingby-method"></a><span data-ttu-id="8bfa7-103">IAMTimelineTrack :: MoveEverythingBy, méthode</span><span class="sxs-lookup"><span data-stu-id="8bfa7-103">IAMTimelineTrack::MoveEverythingBy method</span></span>

<span data-ttu-id="8bfa7-104">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-104">This method is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bfa7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8bfa7-105">Syntax</span></span>


```C++
HRESULT MoveEverythingBy(
   REFERENCE_TIME Start,
   REFERENCE_TIME MoveBy
);
```



## <a name="parameters"></a><span data-ttu-id="8bfa7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8bfa7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bfa7-107">*Start*</span><span class="sxs-lookup"><span data-stu-id="8bfa7-107">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="8bfa7-108">Réservé.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-108">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="8bfa7-109">*MoveBy*</span><span class="sxs-lookup"><span data-stu-id="8bfa7-109">*MoveBy*</span></span> 
</dt> <dd>

<span data-ttu-id="8bfa7-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bfa7-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8bfa7-111">Return value</span></span>

<span data-ttu-id="8bfa7-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8bfa7-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8bfa7-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bfa7-114">Notes </span><span class="sxs-lookup"><span data-stu-id="8bfa7-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8bfa7-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8bfa7-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8bfa7-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8bfa7-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8bfa7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8bfa7-118">Requirements</span></span>



| <span data-ttu-id="8bfa7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8bfa7-119">Requirement</span></span> | <span data-ttu-id="8bfa7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8bfa7-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bfa7-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="8bfa7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8bfa7-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bfa7-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8bfa7-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8bfa7-123">Library</span></span><br/> | <dl> <span data-ttu-id="8bfa7-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bfa7-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bfa7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bfa7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bfa7-126">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="8bfa7-126">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> </dl>

 

 




