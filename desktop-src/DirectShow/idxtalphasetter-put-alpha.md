---
description: La \_ méthode put alpha spécifie la valeur alpha de la totalité de l’image.
ms.assetid: ba02a9ae-b722-4771-89c6-e76369d39ed7
title: IDxtAlphaSetter ::p ut_Alpha, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 54bd69993a0dc0880f351f3e9ba7a79c9d926194
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533130"
---
# <a name="idxtalphasetterput_alpha-method"></a><span data-ttu-id="5db54-103">IDxtAlphaSetter ::p ut \_ alpha, méthode</span><span class="sxs-lookup"><span data-stu-id="5db54-103">IDxtAlphaSetter::put\_Alpha method</span></span>

> [!Note]  
> <span data-ttu-id="5db54-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="5db54-104">\[Deprecated.</span></span> <span data-ttu-id="5db54-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5db54-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5db54-106">La `put_Alpha` méthode spécifie la valeur alpha de la totalité de l’image.</span><span class="sxs-lookup"><span data-stu-id="5db54-106">The `put_Alpha` method specifies the alpha value for the entire image.</span></span>

## <a name="syntax"></a><span data-ttu-id="5db54-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5db54-107">Syntax</span></span>


```C++
HRESULT put_Alpha(
  [in] long Alpha
);
```



## <a name="parameters"></a><span data-ttu-id="5db54-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5db54-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5db54-109">*Alpha* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5db54-109">*Alpha* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5db54-110">Valeur alpha.</span><span class="sxs-lookup"><span data-stu-id="5db54-110">The alpha value.</span></span> <span data-ttu-id="5db54-111">Cette valeur sera appliquée à l’intégralité de l’image cible.</span><span class="sxs-lookup"><span data-stu-id="5db54-111">This value will be applied to the entire target image.</span></span> <span data-ttu-id="5db54-112">Pour désactiver cette propriété, définissez une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="5db54-112">To disable this property, set a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5db54-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5db54-113">Return value</span></span>

<span data-ttu-id="5db54-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5db54-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5db54-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5db54-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5db54-116">Notes</span><span class="sxs-lookup"><span data-stu-id="5db54-116">Remarks</span></span>

<span data-ttu-id="5db54-117">Si vous définissez cette propriété sur une valeur non négative, vous devez également désactiver la propriété de rampe alpha, en appelant **put \_ AlphaRamp** avec une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="5db54-117">If you set this property to a non-negative value, you must also disable the alpha ramp property, by calling **put\_AlphaRamp** with a negative value.</span></span> <span data-ttu-id="5db54-118">Dans le cas contraire, l’effet ne sera pas correctement rendu.</span><span class="sxs-lookup"><span data-stu-id="5db54-118">Otherwise the effect will not render correctly.</span></span>

> [!Note]  
> <span data-ttu-id="5db54-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="5db54-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5db54-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5db54-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5db54-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5db54-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5db54-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5db54-122">Requirements</span></span>



| <span data-ttu-id="5db54-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5db54-123">Requirement</span></span> | <span data-ttu-id="5db54-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="5db54-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5db54-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="5db54-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5db54-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5db54-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5db54-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5db54-127">Library</span></span><br/> | <dl> <span data-ttu-id="5db54-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5db54-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5db54-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5db54-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5db54-130">**Interface IDxtAlphaSetter**</span><span class="sxs-lookup"><span data-stu-id="5db54-130">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> <dt>

[<span data-ttu-id="5db54-131">**IDxtAlphaSetter ::p ut \_ AlphaRamp**</span><span class="sxs-lookup"><span data-stu-id="5db54-131">**IDxtAlphaSetter::put\_AlphaRamp**</span></span>](idxtalphasetter-put-alpharamp.md)
</dt> </dl>

 

 




