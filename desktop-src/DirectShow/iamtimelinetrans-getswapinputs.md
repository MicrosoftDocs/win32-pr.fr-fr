---
description: La méthode GetSwapInputs récupère une valeur qui indique si les entrées de transition sont échangées.
ms.assetid: 84cb5c3d-7c3a-4c35-aac7-97d812d99a38
title: 'IAMTimelineTrans :: GetSwapInputs, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a2acdff1007bd26773ce495d024676632eee1767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543191"
---
# <a name="iamtimelinetransgetswapinputs-method"></a><span data-ttu-id="01392-103">IAMTimelineTrans :: GetSwapInputs, méthode</span><span class="sxs-lookup"><span data-stu-id="01392-103">IAMTimelineTrans::GetSwapInputs method</span></span>

> [!Note]  
> <span data-ttu-id="01392-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="01392-104">\[Deprecated.</span></span> <span data-ttu-id="01392-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="01392-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="01392-106">La `GetSwapInputs` méthode récupère une valeur qui indique si les entrées de transition sont échangées.</span><span class="sxs-lookup"><span data-stu-id="01392-106">The `GetSwapInputs` method retrieves a value that indicates whether the transition inputs are swapped.</span></span>

<span data-ttu-id="01392-107">Par défaut, une transition va du composite de toutes les couches de faible priorité à la couche où la transition réside.</span><span class="sxs-lookup"><span data-stu-id="01392-107">By default, a transition goes from the composite of all lower-priority layers to the layer where the transition resides.</span></span> <span data-ttu-id="01392-108">Vous pouvez inverser cette progression, de sorte que la transition va de la couche où elle réside vers l’composite des couches de faible priorité.</span><span class="sxs-lookup"><span data-stu-id="01392-108">You can reverse this progression, so the transition goes from the layer where it resides back to the composite of lower-priority layers.</span></span>

## <a name="syntax"></a><span data-ttu-id="01392-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01392-109">Syntax</span></span>


```C++
HRESULT GetSwapInputs(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="01392-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01392-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01392-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="01392-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="01392-112">Reçoit une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="01392-112">Receives a Boolean value.</span></span> <span data-ttu-id="01392-113">Si la valeur est **false**, la transition passe de l’composite de toutes les couches de faible priorité à la couche de transition.</span><span class="sxs-lookup"><span data-stu-id="01392-113">If the value is **FALSE**, the transition goes from the composite of all lower-priority layers to the transition layer.</span></span> <span data-ttu-id="01392-114">Si la valeur est **true**, la transition passe dans la direction opposée.</span><span class="sxs-lookup"><span data-stu-id="01392-114">If the value is **TRUE**, the transition goes in the opposite direction.</span></span> <span data-ttu-id="01392-115">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="01392-115">The default value is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01392-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="01392-116">Return value</span></span>

<span data-ttu-id="01392-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="01392-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="01392-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="01392-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="01392-119">Notes</span><span class="sxs-lookup"><span data-stu-id="01392-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="01392-120">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="01392-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="01392-121">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="01392-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="01392-122">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="01392-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="01392-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01392-123">Requirements</span></span>



| <span data-ttu-id="01392-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01392-124">Requirement</span></span> | <span data-ttu-id="01392-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="01392-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01392-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="01392-126">Header</span></span><br/>  | <dl> <span data-ttu-id="01392-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="01392-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="01392-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="01392-128">Library</span></span><br/> | <dl> <span data-ttu-id="01392-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01392-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01392-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01392-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01392-131">**Interface IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="01392-131">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="01392-132">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="01392-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




