---
description: La \_ méthode obtenir alpha récupère la valeur alpha de la totalité de l’image.
ms.assetid: ce891149-e964-4239-aeef-c9f4a8354563
title: 'IDxtAlphaSetter :: get_Alpha, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6182590d09df1c816a1a861df8be724798cc75da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523605"
---
# <a name="idxtalphasetterget_alpha-method"></a><span data-ttu-id="0932c-103">IDxtAlphaSetter :: obtient la \_ méthode alpha</span><span class="sxs-lookup"><span data-stu-id="0932c-103">IDxtAlphaSetter::get\_Alpha method</span></span>

> [!Note]  
> <span data-ttu-id="0932c-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0932c-104">\[Deprecated.</span></span> <span data-ttu-id="0932c-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0932c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0932c-106">La `get_Alpha` méthode récupère la valeur alpha de la totalité de l’image.</span><span class="sxs-lookup"><span data-stu-id="0932c-106">The `get_Alpha` method retrieves the alpha value for the entire image.</span></span>

## <a name="syntax"></a><span data-ttu-id="0932c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0932c-107">Syntax</span></span>


```C++
HRESULT get_Alpha(
  [out, retval] long *pAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="0932c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0932c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0932c-109">*pAlpha* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0932c-109">*pAlpha* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0932c-110">Reçoit la valeur alpha.</span><span class="sxs-lookup"><span data-stu-id="0932c-110">Receives the alpha value.</span></span> <span data-ttu-id="0932c-111">Cette valeur alpha sera appliquée à l’intégralité de l’image cible.</span><span class="sxs-lookup"><span data-stu-id="0932c-111">This alpha value will be applied to the entire target image.</span></span> <span data-ttu-id="0932c-112">Une valeur négative indique qu’aucune valeur alpha n’est définie.</span><span class="sxs-lookup"><span data-stu-id="0932c-112">A negative value indicates that no alpha value is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0932c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0932c-113">Return value</span></span>

<span data-ttu-id="0932c-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0932c-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0932c-115">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="0932c-115">Possible values include the following.</span></span>



| <span data-ttu-id="0932c-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0932c-116">Return code</span></span>                                                                               | <span data-ttu-id="0932c-117">Description</span><span class="sxs-lookup"><span data-stu-id="0932c-117">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="0932c-118"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="0932c-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="0932c-119">Argument de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="0932c-119">**NULL** pointer argument</span></span><br/> |
| <dl> <span data-ttu-id="0932c-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0932c-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="0932c-121">Succès</span><span class="sxs-lookup"><span data-stu-id="0932c-121">Success</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="0932c-122">Notes</span><span class="sxs-lookup"><span data-stu-id="0932c-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0932c-123">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="0932c-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0932c-124">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0932c-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0932c-125">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0932c-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0932c-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0932c-126">Requirements</span></span>



| <span data-ttu-id="0932c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0932c-127">Requirement</span></span> | <span data-ttu-id="0932c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="0932c-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0932c-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="0932c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0932c-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0932c-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0932c-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0932c-131">Library</span></span><br/> | <dl> <span data-ttu-id="0932c-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0932c-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0932c-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0932c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0932c-134">**Interface IDxtAlphaSetter**</span><span class="sxs-lookup"><span data-stu-id="0932c-134">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> </dl>

 

 




