---
description: La méthode SetCutPoint définit l’heure à laquelle la transition passe d’une source à la suivante, si la transition est rendue sous la forme d’une coupe.
ms.assetid: 2660f4a8-e249-45d7-8866-02a9f2ef52b8
title: 'IAMTimelineTrans :: SetCutPoint, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c1dad934d373a52b7e6c076c8c20dc8e1c6809ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537473"
---
# <a name="iamtimelinetranssetcutpoint-method"></a><span data-ttu-id="0f10e-103">IAMTimelineTrans :: SetCutPoint, méthode</span><span class="sxs-lookup"><span data-stu-id="0f10e-103">IAMTimelineTrans::SetCutPoint method</span></span>

> [!Note]  
> <span data-ttu-id="0f10e-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0f10e-104">\[Deprecated.</span></span> <span data-ttu-id="0f10e-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0f10e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0f10e-106">La `SetCutPoint` méthode définit l’heure à laquelle la transition passe d’une source à la suivante, si la transition est rendue sous la forme d’une coupe.</span><span class="sxs-lookup"><span data-stu-id="0f10e-106">The `SetCutPoint` method sets the time at which the transition cuts from one source to the next, if the transition is rendered as a cut.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f10e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f10e-107">Syntax</span></span>


```C++
HRESULT SetCutPoint(
   REFERENCE_TIME TLTime
);
```



## <a name="parameters"></a><span data-ttu-id="0f10e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f10e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f10e-109">*TLTime*</span><span class="sxs-lookup"><span data-stu-id="0f10e-109">*TLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="0f10e-110">Point de coupe par rapport au début de la transition, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="0f10e-110">Cut point relative to the start of the transition, in 100-nanosecond units.</span></span> <span data-ttu-id="0f10e-111">Si la valeur se trouve en dehors des limites de la transition, elle est tronquée à l’heure valide la plus proche.</span><span class="sxs-lookup"><span data-stu-id="0f10e-111">If the value falls outside the bounds of the transition, it is truncated to the nearest valid time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f10e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f10e-112">Return value</span></span>

<span data-ttu-id="0f10e-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0f10e-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0f10e-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f10e-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f10e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0f10e-115">Remarks</span></span>

<span data-ttu-id="0f10e-116">Par défaut, le point de coupe est le milieu de la transition.</span><span class="sxs-lookup"><span data-stu-id="0f10e-116">By default, the cut-point is the middle of the transition.</span></span> <span data-ttu-id="0f10e-117">Par exemple, dans une transition qui s’étend sur une seconde, le point de coupe par défaut est de 0,5 secondes dans la transition.</span><span class="sxs-lookup"><span data-stu-id="0f10e-117">For example, in a transition that spans one second, the default cut point is 0.5 seconds into the transition.</span></span>

> [!Note]  
> <span data-ttu-id="0f10e-118">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="0f10e-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0f10e-119">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0f10e-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0f10e-120">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0f10e-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0f10e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f10e-121">Requirements</span></span>



| <span data-ttu-id="0f10e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f10e-122">Requirement</span></span> | <span data-ttu-id="0f10e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f10e-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f10e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f10e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0f10e-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f10e-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0f10e-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0f10e-126">Library</span></span><br/> | <dl> <span data-ttu-id="0f10e-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f10e-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f10e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f10e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f10e-129">**Interface IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="0f10e-129">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="0f10e-130">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="0f10e-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




