---
description: 'La méthode ModifyStopTime2 définit l’heure d’arrêt. Cette méthode est équivalente à IAMTimelineSrc :: ModifyStopTime, mais prend une valeur REFTIME.'
ms.assetid: 8bebda47-3e52-42a2-870c-acc14561fa25
title: 'IAMTimelineSrc :: ModifyStopTime2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 42ca3c9c1f8fa47abc7a9c21a44458540007939f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533459"
---
# <a name="iamtimelinesrcmodifystoptime2-method"></a><span data-ttu-id="5ab89-104">IAMTimelineSrc :: ModifyStopTime2, méthode</span><span class="sxs-lookup"><span data-stu-id="5ab89-104">IAMTimelineSrc::ModifyStopTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="5ab89-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="5ab89-105">\[Deprecated.</span></span> <span data-ttu-id="5ab89-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5ab89-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5ab89-107">La `ModifyStopTime2` méthode définit l’heure d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5ab89-107">The `ModifyStopTime2` method sets the stop time.</span></span> <span data-ttu-id="5ab89-108">Cette méthode est équivalente à [**IAMTimelineSrc :: ModifyStopTime**](iamtimelinesrc-modifystoptime.md), mais prend une valeur [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="5ab89-108">This method is equivalent to [**IAMTimelineSrc::ModifyStopTime**](iamtimelinesrc-modifystoptime.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ab89-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ab89-109">Syntax</span></span>


```C++
HRESULT ModifyStopTime2(
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="5ab89-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ab89-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ab89-111">*Stop*</span><span class="sxs-lookup"><span data-stu-id="5ab89-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="5ab89-112">Nouvelle heure d’arrêt, en secondes.</span><span class="sxs-lookup"><span data-stu-id="5ab89-112">New stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ab89-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5ab89-113">Return value</span></span>

<span data-ttu-id="5ab89-114">Retourne S \_ OK en cas de réussite, ou E \_ INVALIDARG si l’heure spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5ab89-114">Returns S\_OK if successful, or E\_INVALIDARG if the specified time is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ab89-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5ab89-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5ab89-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="5ab89-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5ab89-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5ab89-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5ab89-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5ab89-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5ab89-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ab89-119">Requirements</span></span>



| <span data-ttu-id="5ab89-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ab89-120">Requirement</span></span> | <span data-ttu-id="5ab89-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ab89-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab89-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ab89-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5ab89-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ab89-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5ab89-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5ab89-124">Library</span></span><br/> | <dl> <span data-ttu-id="5ab89-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ab89-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ab89-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ab89-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ab89-127">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="5ab89-127">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="5ab89-128">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="5ab89-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




