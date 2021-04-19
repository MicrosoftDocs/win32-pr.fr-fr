---
description: La méthode EffectInsBefore insère un effet dans l’objet au niveau de priorité spécifié.
ms.assetid: 6c98e24a-5bac-4273-ae3c-2ab3c9d9465b
title: 'IAMTimelineEffectable :: EffectInsBefore, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eeca130f90cee5985f697a4efa042e3b4cb065b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537916"
---
# <a name="iamtimelineeffectableeffectinsbefore-method"></a><span data-ttu-id="eb0cb-103">IAMTimelineEffectable :: EffectInsBefore, méthode</span><span class="sxs-lookup"><span data-stu-id="eb0cb-103">IAMTimelineEffectable::EffectInsBefore method</span></span>

> [!Note]  
> <span data-ttu-id="eb0cb-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="eb0cb-104">\[Deprecated.</span></span> <span data-ttu-id="eb0cb-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eb0cb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="eb0cb-106">La `EffectInsBefore` méthode insère un effet dans l’objet au niveau de priorité spécifié.</span><span class="sxs-lookup"><span data-stu-id="eb0cb-106">The `EffectInsBefore` method inserts an effect into the object at the specified priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb0cb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb0cb-107">Syntax</span></span>


```C++
HRESULT EffectInsBefore(
   IAMTimelineObj *pFX,
   long           Priority
);
```



## <a name="parameters"></a><span data-ttu-id="eb0cb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb0cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb0cb-109">*pFX*</span><span class="sxs-lookup"><span data-stu-id="eb0cb-109">*pFX*</span></span> 
</dt> <dd>

<span data-ttu-id="eb0cb-110">Pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’effet.</span><span class="sxs-lookup"><span data-stu-id="eb0cb-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the effect.</span></span>

</dd> <dt>

<span data-ttu-id="eb0cb-111">*Priorité*</span><span class="sxs-lookup"><span data-stu-id="eb0cb-111">*Priority*</span></span> 
</dt> <dd>

<span data-ttu-id="eb0cb-112">Niveau de priorité auquel insérer l’effet.</span><span class="sxs-lookup"><span data-stu-id="eb0cb-112">Priority level at which to insert the effect.</span></span> <span data-ttu-id="eb0cb-113">Utilisez la valeur-1 pour insérer l’effet à la fin de la liste de priorités.</span><span class="sxs-lookup"><span data-stu-id="eb0cb-113">Use the value –1 to insert the effect at the end of the priority list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb0cb-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb0cb-114">Return value</span></span>

<span data-ttu-id="eb0cb-115">Retourne S \_ OK en cas de réussite ou E \_ NOTIMPL si l’objet n’est pas un effet.</span><span class="sxs-lookup"><span data-stu-id="eb0cb-115">Returns S\_OK if successful or E\_NOTIMPL if the object is not an effect.</span></span> <span data-ttu-id="eb0cb-116">Sinon, retourne une autre valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="eb0cb-116">Otherwise, returns another **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb0cb-117">Notes</span><span class="sxs-lookup"><span data-stu-id="eb0cb-117">Remarks</span></span>

<span data-ttu-id="eb0cb-118">Les heures de début et de fin de l’effet sont découpées dans les limites de la plage horaire de l’objet, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="eb0cb-118">The start and stop times of the effect are clipped within the bounds of the object's time range, if necessary.</span></span> <span data-ttu-id="eb0cb-119">S’il existe déjà un effet au niveau de priorité spécifié, tous les effets de ce point sur descendent dans la liste des priorités pour faire de la place pour le nouvel effet.</span><span class="sxs-lookup"><span data-stu-id="eb0cb-119">If there is already an effect at the specified priority level, all the effects from that point on move down the priority list to make room for the new effect.</span></span>

> [!Note]  
> <span data-ttu-id="eb0cb-120">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="eb0cb-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="eb0cb-121">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="eb0cb-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="eb0cb-122">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="eb0cb-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eb0cb-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb0cb-123">Requirements</span></span>



| <span data-ttu-id="eb0cb-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb0cb-124">Requirement</span></span> | <span data-ttu-id="eb0cb-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb0cb-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb0cb-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb0cb-126">Header</span></span><br/>  | <dl> <span data-ttu-id="eb0cb-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb0cb-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="eb0cb-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eb0cb-128">Library</span></span><br/> | <dl> <span data-ttu-id="eb0cb-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb0cb-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb0cb-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb0cb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb0cb-131">**Interface IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="eb0cb-131">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="eb0cb-132">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="eb0cb-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




