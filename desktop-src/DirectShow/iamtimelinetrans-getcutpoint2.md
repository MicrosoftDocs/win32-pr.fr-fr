---
description: 'La méthode GetCutPoint2 récupère le point de coupe. Cette méthode est équivalente à IAMTimelineTrans :: GetCutPoint, mais prend une valeur REFTIME.'
ms.assetid: bf2b7cac-6740-44d8-a889-8c745a23db19
title: 'IAMTimelineTrans :: GetCutPoint2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 68712da95da2f5c21d5e370c688002aa14a8a166
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530027"
---
# <a name="iamtimelinetransgetcutpoint2-method"></a><span data-ttu-id="bc2a9-104">IAMTimelineTrans :: GetCutPoint2, méthode</span><span class="sxs-lookup"><span data-stu-id="bc2a9-104">IAMTimelineTrans::GetCutPoint2 method</span></span>

> [!Note]  
> <span data-ttu-id="bc2a9-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="bc2a9-105">\[Deprecated.</span></span> <span data-ttu-id="bc2a9-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bc2a9-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bc2a9-107">La `GetCutPoint2` méthode récupère le point de coupe.</span><span class="sxs-lookup"><span data-stu-id="bc2a9-107">The `GetCutPoint2` method retrieves the cut point.</span></span> <span data-ttu-id="bc2a9-108">Cette méthode est équivalente à [**IAMTimelineTrans :: GetCutPoint**](iamtimelinetrans-getcutpoint.md), mais prend une valeur [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="bc2a9-108">This method is equivalent to [**IAMTimelineTrans::GetCutPoint**](iamtimelinetrans-getcutpoint.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc2a9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc2a9-109">Syntax</span></span>


```C++
HRESULT GetCutPoint2(
   REFTIME *pTLTime
);
```



## <a name="parameters"></a><span data-ttu-id="bc2a9-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc2a9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc2a9-111">*pTLTime*</span><span class="sxs-lookup"><span data-stu-id="bc2a9-111">*pTLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="bc2a9-112">Reçoit le point de coupe, en secondes, par rapport à l’heure de début de la transition.</span><span class="sxs-lookup"><span data-stu-id="bc2a9-112">Receives the cut point, relative to the start time of the transition, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc2a9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc2a9-113">Return value</span></span>

<span data-ttu-id="bc2a9-114">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc2a9-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="bc2a9-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bc2a9-115">Return code</span></span>                                                                               | <span data-ttu-id="bc2a9-116">Description</span><span class="sxs-lookup"><span data-stu-id="bc2a9-116">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bc2a9-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="bc2a9-117"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="bc2a9-118">Le point de coupe n’a pas été défini.</span><span class="sxs-lookup"><span data-stu-id="bc2a9-118">The cut point was not set.</span></span> <span data-ttu-id="bc2a9-119">La valeur retournée est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="bc2a9-119">The value returned is the default value.</span></span><br/> |
| <dl> <span data-ttu-id="bc2a9-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bc2a9-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="bc2a9-121">Le point de coupe a été défini sur une valeur autre que la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="bc2a9-121">The cut point was set to a value other than the default.</span></span><br/>            |
| <dl> <span data-ttu-id="bc2a9-122"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="bc2a9-122"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="bc2a9-123">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="bc2a9-123">**NULL** pointer argument.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="bc2a9-124">Notes</span><span class="sxs-lookup"><span data-stu-id="bc2a9-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bc2a9-125">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="bc2a9-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bc2a9-126">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bc2a9-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bc2a9-127">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bc2a9-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bc2a9-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc2a9-128">Requirements</span></span>



| <span data-ttu-id="bc2a9-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc2a9-129">Requirement</span></span> | <span data-ttu-id="bc2a9-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc2a9-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc2a9-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc2a9-131">Header</span></span><br/>  | <dl> <span data-ttu-id="bc2a9-132"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc2a9-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bc2a9-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bc2a9-133">Library</span></span><br/> | <dl> <span data-ttu-id="bc2a9-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc2a9-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc2a9-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc2a9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc2a9-136">**Interface IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="bc2a9-136">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="bc2a9-137">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="bc2a9-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




