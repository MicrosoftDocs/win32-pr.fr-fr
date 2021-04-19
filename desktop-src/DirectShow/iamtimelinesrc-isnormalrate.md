---
description: La méthode IsNormalRate indique si le clip sera lu à la vitesse de lecture normale ; autrement dit, la vitesse de lecture du fichier d’origine.
ms.assetid: 4a8fe415-f9eb-450d-9a75-e528577050d9
title: 'IAMTimelineSrc :: IsNormalRate, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.IsNormalRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e368efcf29d836cc23fa60ed34dae1a172978f77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537879"
---
# <a name="iamtimelinesrcisnormalrate-method"></a><span data-ttu-id="e6097-103">IAMTimelineSrc :: IsNormalRate, méthode</span><span class="sxs-lookup"><span data-stu-id="e6097-103">IAMTimelineSrc::IsNormalRate method</span></span>

> [!Note]  
> <span data-ttu-id="e6097-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e6097-104">\[Deprecated.</span></span> <span data-ttu-id="e6097-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e6097-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e6097-106">La `IsNormalRate` méthode indique si le clip sera lu à la vitesse de lecture normale ; autrement dit, la vitesse de lecture du fichier d’origine.</span><span class="sxs-lookup"><span data-stu-id="e6097-106">The `IsNormalRate` method indicates whether the clip will play at the normal playback rate; that is, the playback rate of the original file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6097-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6097-107">Syntax</span></span>


```C++
HRESULT IsNormalRate(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e6097-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6097-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6097-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="e6097-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="e6097-110">Reçoit une valeur booléenne indiquant comment le clip sera rendu.</span><span class="sxs-lookup"><span data-stu-id="e6097-110">Receives a Boolean value indicating how the clip will render.</span></span> <span data-ttu-id="e6097-111">Si la valeur est **true**, le clip est lu au taux normal.</span><span class="sxs-lookup"><span data-stu-id="e6097-111">If the value is **TRUE**, the clip will play at the normal rate.</span></span> <span data-ttu-id="e6097-112">Dans le cas contraire, la lecture sera plus rapide ou plus lente que la normale.</span><span class="sxs-lookup"><span data-stu-id="e6097-112">Otherwise, it will play faster or slower than normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6097-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6097-113">Return value</span></span>

<span data-ttu-id="e6097-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e6097-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e6097-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6097-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6097-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e6097-116">Remarks</span></span>

<span data-ttu-id="e6097-117">Le taux de lecture d’un clip est déterminé par les heures de début et de fin du support, par rapport aux heures de la chronologie :</span><span class="sxs-lookup"><span data-stu-id="e6097-117">A clip's playback rate is determined by its media start and stop times, relative to its timeline times:</span></span>


```C++
Playback rate = (Media Stop <entity type="mdash"/> Media Start) / (Timeline Stop <entity type="mdash"/> Timeline Start)
```



<span data-ttu-id="e6097-118">Si ce ratio est égal à 1, le clip est lu à la vitesse de création.</span><span class="sxs-lookup"><span data-stu-id="e6097-118">If this ratio is equal to 1, the clip plays at the authored speed.</span></span> <span data-ttu-id="e6097-119">Dans le cas contraire, la lecture est plus rapide ou plus lente.</span><span class="sxs-lookup"><span data-stu-id="e6097-119">Otherwise, it plays faster or slower.</span></span> <span data-ttu-id="e6097-120">Pour plus d’informations, consultez [heure dans les services de modification DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="e6097-120">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="e6097-121">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="e6097-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e6097-122">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e6097-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e6097-123">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e6097-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e6097-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6097-124">Requirements</span></span>



| <span data-ttu-id="e6097-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6097-125">Requirement</span></span> | <span data-ttu-id="e6097-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6097-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6097-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6097-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e6097-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6097-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e6097-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e6097-129">Library</span></span><br/> | <dl> <span data-ttu-id="e6097-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6097-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6097-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6097-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6097-132">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="e6097-132">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="e6097-133">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="e6097-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




