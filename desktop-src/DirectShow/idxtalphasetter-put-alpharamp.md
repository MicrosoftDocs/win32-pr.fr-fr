---
description: La \_ méthode put AlphaRamp spécifie la propriété de rampe alpha. La rampe alpha est le pourcentage d’ajustement des valeurs alpha dans l’image d’origine. Par exemple, si la rampe alpha est 0,5, les valeurs alpha de l’image sont réduites à 50%.
ms.assetid: 19ea5828-54fc-43a1-be7c-f6c12cf84648
title: IDxtAlphaSetter ::p ut_AlphaRamp, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc6c0eb4d5286081de9abe0c7c6d58092d111573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538159"
---
# <a name="idxtalphasetterput_alpharamp-method"></a><span data-ttu-id="1a2b8-105">IDxtAlphaSetter ::p ut \_ AlphaRamp, méthode</span><span class="sxs-lookup"><span data-stu-id="1a2b8-105">IDxtAlphaSetter::put\_AlphaRamp method</span></span>

> [!Note]  
> <span data-ttu-id="1a2b8-106">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="1a2b8-106">\[Deprecated.</span></span> <span data-ttu-id="1a2b8-107">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1a2b8-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1a2b8-108">La `put_AlphaRamp` méthode spécifie la propriété de rampe alpha.</span><span class="sxs-lookup"><span data-stu-id="1a2b8-108">The `put_AlphaRamp` method specifies the alpha ramp property.</span></span> <span data-ttu-id="1a2b8-109">La rampe alpha est le pourcentage d’ajustement des valeurs alpha dans l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="1a2b8-109">The alpha ramp is the percentage by which the alpha values in the original image are adjusted.</span></span> <span data-ttu-id="1a2b8-110">Par exemple, si la rampe alpha est 0,5, les valeurs alpha de l’image sont réduites à 50%.</span><span class="sxs-lookup"><span data-stu-id="1a2b8-110">For example, if the alpha ramp is 0.5, the alpha values in the image are reduced 50%.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a2b8-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a2b8-111">Syntax</span></span>


```C++
HRESULT put_AlphaRamp(
  [in] double Alpha
);
```



## <a name="parameters"></a><span data-ttu-id="1a2b8-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a2b8-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a2b8-113">*Alpha* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a2b8-113">*Alpha* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a2b8-114">Rampe alpha sous la forme d’un pourcentage.</span><span class="sxs-lookup"><span data-stu-id="1a2b8-114">The alpha ramp as a percentage.</span></span> <span data-ttu-id="1a2b8-115">Par exemple, 1,0 est 100%.</span><span class="sxs-lookup"><span data-stu-id="1a2b8-115">For example, 1.0 is 100%.</span></span> <span data-ttu-id="1a2b8-116">Pour désactiver cette propriété, définissez une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="1a2b8-116">To disable this property, set a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a2b8-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a2b8-117">Return value</span></span>

<span data-ttu-id="1a2b8-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1a2b8-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1a2b8-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1a2b8-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a2b8-120">Notes</span><span class="sxs-lookup"><span data-stu-id="1a2b8-120">Remarks</span></span>

<span data-ttu-id="1a2b8-121">Si vous affectez une valeur non négative à cette propriété, vous devez également désactiver la propriété alpha en appelant **put \_ alpha** avec une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="1a2b8-121">If you set this property to a non-negative value, you must also disable the alpha property, by calling **put\_Alpha** with a negative value.</span></span> <span data-ttu-id="1a2b8-122">Dans le cas contraire, l’effet ne sera pas correctement rendu.</span><span class="sxs-lookup"><span data-stu-id="1a2b8-122">Otherwise the effect will not render correctly.</span></span>

> [!Note]  
> <span data-ttu-id="1a2b8-123">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="1a2b8-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1a2b8-124">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1a2b8-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1a2b8-125">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1a2b8-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1a2b8-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a2b8-126">Requirements</span></span>



| <span data-ttu-id="1a2b8-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a2b8-127">Requirement</span></span> | <span data-ttu-id="1a2b8-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a2b8-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a2b8-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a2b8-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1a2b8-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a2b8-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1a2b8-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1a2b8-131">Library</span></span><br/> | <dl> <span data-ttu-id="1a2b8-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a2b8-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a2b8-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a2b8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a2b8-134">**Interface IDxtAlphaSetter**</span><span class="sxs-lookup"><span data-stu-id="1a2b8-134">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> <dt>

[<span data-ttu-id="1a2b8-135">**IDxtAlphaSetter ::p ut \_ alpha**</span><span class="sxs-lookup"><span data-stu-id="1a2b8-135">**IDxtAlphaSetter::put\_Alpha**</span></span>](idxtalphasetter-put-alpha.md)
</dt> </dl>

 

 




