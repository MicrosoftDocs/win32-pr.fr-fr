---
description: La \_ méthode obtenir AlphaRamp récupère la propriété de rampe alpha. La rampe alpha est le pourcentage d’ajustement des valeurs alpha dans l’image d’origine. Par exemple, si la rampe alpha est 0,5, les valeurs alpha de l’image sont réduites à 50%.
ms.assetid: e142a562-2e78-4418-94e9-b41320d4af57
title: 'IDxtAlphaSetter :: get_AlphaRamp, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 335c227b0ac35ccd730d8ce7014b9a5c7ebc3213
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520866"
---
# <a name="idxtalphasetterget_alpharamp-method"></a><span data-ttu-id="60e36-105">IDxtAlphaSetter :: \_ AlphaRamp, méthode</span><span class="sxs-lookup"><span data-stu-id="60e36-105">IDxtAlphaSetter::get\_AlphaRamp method</span></span>

> [!Note]  
> <span data-ttu-id="60e36-106">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="60e36-106">\[Deprecated.</span></span> <span data-ttu-id="60e36-107">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="60e36-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="60e36-108">La `get_AlphaRamp` méthode récupère la propriété de rampe alpha.</span><span class="sxs-lookup"><span data-stu-id="60e36-108">The `get_AlphaRamp` method retrieves the alpha ramp property.</span></span> <span data-ttu-id="60e36-109">La rampe alpha est le pourcentage d’ajustement des valeurs alpha dans l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="60e36-109">The alpha ramp is the percentage by which the alpha values in the original image are adjusted.</span></span> <span data-ttu-id="60e36-110">Par exemple, si la rampe alpha est 0,5, les valeurs alpha de l’image sont réduites à 50%.</span><span class="sxs-lookup"><span data-stu-id="60e36-110">For example, if the alpha ramp is 0.5, the alpha values in the image are reduced 50%.</span></span>

## <a name="syntax"></a><span data-ttu-id="60e36-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60e36-111">Syntax</span></span>


```C++
HRESULT get_AlphaRamp(
  [out, retval] double *pAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="60e36-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60e36-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60e36-113">*pAlpha* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="60e36-113">*pAlpha* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="60e36-114">Reçoit la rampe alpha.</span><span class="sxs-lookup"><span data-stu-id="60e36-114">Receives the alpha ramp.</span></span> <span data-ttu-id="60e36-115">Une valeur négative indique qu’aucune rampe alpha n’est définie.</span><span class="sxs-lookup"><span data-stu-id="60e36-115">A negative value indicates that no alpha ramp is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60e36-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60e36-116">Return value</span></span>

<span data-ttu-id="60e36-117">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="60e36-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="60e36-118">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="60e36-118">Possible values include the following.</span></span>



| <span data-ttu-id="60e36-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="60e36-119">Return code</span></span>                                                                               | <span data-ttu-id="60e36-120">Description</span><span class="sxs-lookup"><span data-stu-id="60e36-120">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="60e36-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="60e36-121"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="60e36-122">Argument de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="60e36-122">**NULL** pointer argument</span></span><br/> |
| <dl> <span data-ttu-id="60e36-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="60e36-123"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="60e36-124">Succès</span><span class="sxs-lookup"><span data-stu-id="60e36-124">Success</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="60e36-125">Notes</span><span class="sxs-lookup"><span data-stu-id="60e36-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="60e36-126">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="60e36-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="60e36-127">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="60e36-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="60e36-128">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="60e36-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="60e36-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60e36-129">Requirements</span></span>



| <span data-ttu-id="60e36-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60e36-130">Requirement</span></span> | <span data-ttu-id="60e36-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="60e36-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60e36-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="60e36-132">Header</span></span><br/>  | <dl> <span data-ttu-id="60e36-133"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="60e36-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="60e36-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="60e36-134">Library</span></span><br/> | <dl> <span data-ttu-id="60e36-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60e36-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60e36-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60e36-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e36-137">**Interface IDxtAlphaSetter**</span><span class="sxs-lookup"><span data-stu-id="60e36-137">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> </dl>

 

 




