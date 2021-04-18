---
description: La méthode TransGetCount récupère le nombre de transitions sur cet objet.
ms.assetid: f7fb4a99-c841-4680-b7f1-e4d887f12707
title: 'IAMTimelineTransable :: TransGetCount, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransGetCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 81b5fc6301b319b8716a6db25fce2b1e5c2d4961
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529003"
---
# <a name="iamtimelinetransabletransgetcount-method"></a><span data-ttu-id="3b6cb-103">IAMTimelineTransable :: TransGetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="3b6cb-103">IAMTimelineTransable::TransGetCount method</span></span>

> [!Note]  
> <span data-ttu-id="3b6cb-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="3b6cb-104">\[Deprecated.</span></span> <span data-ttu-id="3b6cb-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3b6cb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3b6cb-106">La `TransGetCount` méthode récupère le nombre de transitions sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="3b6cb-106">The `TransGetCount` method retrieves the number of transitions on this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b6cb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b6cb-107">Syntax</span></span>


```C++
HRESULT TransGetCount(
   long *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="3b6cb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b6cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b6cb-109">*pCount*</span><span class="sxs-lookup"><span data-stu-id="3b6cb-109">*pCount*</span></span> 
</dt> <dd>

<span data-ttu-id="3b6cb-110">Reçoit le nombre de transitions.</span><span class="sxs-lookup"><span data-stu-id="3b6cb-110">Receives the number of transitions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b6cb-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b6cb-111">Return value</span></span>

<span data-ttu-id="3b6cb-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3b6cb-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3b6cb-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3b6cb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b6cb-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3b6cb-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3b6cb-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="3b6cb-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3b6cb-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3b6cb-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3b6cb-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3b6cb-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3b6cb-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b6cb-118">Requirements</span></span>



| <span data-ttu-id="3b6cb-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b6cb-119">Requirement</span></span> | <span data-ttu-id="3b6cb-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b6cb-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b6cb-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b6cb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3b6cb-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b6cb-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3b6cb-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3b6cb-123">Library</span></span><br/> | <dl> <span data-ttu-id="3b6cb-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b6cb-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b6cb-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b6cb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b6cb-126">**Interface IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="3b6cb-126">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="3b6cb-127">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="3b6cb-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




