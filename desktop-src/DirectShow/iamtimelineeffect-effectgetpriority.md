---
description: La méthode EffectGetPriority récupère le niveau de priorité de l’effet. Pour un objet donné, le moteur de rendu applique les effets par ordre de priorité, en commençant par le niveau de priorité zéro.
ms.assetid: 2504fa0c-f052-4d99-98c3-803b0c0d49e5
title: 'IAMTimelineEffect :: EffectGetPriority, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect.EffectGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 26ea9795e3ffe36a75c354e51ff2f7e64fae40ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535030"
---
# <a name="iamtimelineeffecteffectgetpriority-method"></a><span data-ttu-id="a9051-104">IAMTimelineEffect :: EffectGetPriority, méthode</span><span class="sxs-lookup"><span data-stu-id="a9051-104">IAMTimelineEffect::EffectGetPriority method</span></span>

> [!Note]  
> <span data-ttu-id="a9051-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="a9051-105">\[Deprecated.</span></span> <span data-ttu-id="a9051-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a9051-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a9051-107">La `EffectGetPriority` méthode récupère le niveau de priorité de l’effet.</span><span class="sxs-lookup"><span data-stu-id="a9051-107">The `EffectGetPriority` method retrieves the effect's priority level.</span></span> <span data-ttu-id="a9051-108">Pour un objet donné, le moteur de rendu applique les effets par ordre de priorité, en commençant par le niveau de priorité zéro.</span><span class="sxs-lookup"><span data-stu-id="a9051-108">For a given object, the render engine applies effects in order of priority, starting with priority level zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9051-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9051-109">Syntax</span></span>


```C++
HRESULT EffectGetPriority(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="a9051-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9051-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9051-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="a9051-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="a9051-112">Reçoit le niveau de priorité.</span><span class="sxs-lookup"><span data-stu-id="a9051-112">Receives the priority level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9051-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a9051-113">Return value</span></span>

<span data-ttu-id="a9051-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a9051-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a9051-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a9051-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9051-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a9051-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a9051-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="a9051-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a9051-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a9051-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a9051-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a9051-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a9051-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9051-120">Requirements</span></span>



| <span data-ttu-id="a9051-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9051-121">Requirement</span></span> | <span data-ttu-id="a9051-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9051-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9051-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9051-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a9051-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9051-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a9051-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a9051-125">Library</span></span><br/> | <dl> <span data-ttu-id="a9051-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9051-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9051-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9051-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9051-128">**Interface IAMTimelineEffect**</span><span class="sxs-lookup"><span data-stu-id="a9051-128">**IAMTimelineEffect Interface**</span></span>](iamtimelineeffect.md)
</dt> <dt>

[<span data-ttu-id="a9051-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="a9051-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




