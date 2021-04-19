---
description: La \_ méthode d’infiltration retourne la taille d’entrée actuelle du filtre de redimensionnement.
ms.assetid: 7066a044-52ea-4851-83f2-f1fb323c2251
title: 'IResize :: get_InputSize, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_InputSize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fab61edf6dc4469f06437483172161fbbe77e76d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541310"
---
# <a name="iresizeget_inputsize-method"></a><span data-ttu-id="3091e-103">IResize :: obtient la \_ méthode Input</span><span class="sxs-lookup"><span data-stu-id="3091e-103">IResize::get\_InputSize method</span></span>

> [!Note]  
> <span data-ttu-id="3091e-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="3091e-104">\[Deprecated.</span></span> <span data-ttu-id="3091e-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3091e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3091e-106">La `get_InputSize` méthode retourne la taille d’entrée actuelle du filtre de redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="3091e-106">The `get_InputSize` method returns the resizer filter's current input size.</span></span>

## <a name="syntax"></a><span data-ttu-id="3091e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3091e-107">Syntax</span></span>


```C++
HRESULT get_InputSize(
  [out] int *piHeight,
  [out] int *piWidth
);
```



## <a name="parameters"></a><span data-ttu-id="3091e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3091e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3091e-109">*piHeight* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3091e-109">*piHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3091e-110">Reçoit la hauteur vidéo, en pixels.</span><span class="sxs-lookup"><span data-stu-id="3091e-110">Receives the video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="3091e-111">*piWidth* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3091e-111">*piWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3091e-112">Reçoit la largeur vidéo, en pixels.</span><span class="sxs-lookup"><span data-stu-id="3091e-112">Receives the video width, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3091e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3091e-113">Return value</span></span>

<span data-ttu-id="3091e-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3091e-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3091e-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3091e-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3091e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="3091e-116">Remarks</span></span>

<span data-ttu-id="3091e-117">Si la broche d’entrée du filtre n’est pas connectée, retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3091e-117">If the filter's input pin is not connected, return an error code.</span></span> <span data-ttu-id="3091e-118">Sinon, retournez la largeur et la hauteur de la vidéo, comme spécifié par le type de média de la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3091e-118">Otherwise, return the width and height of the video, as specified by the input pin's media type.</span></span>

> [!Note]  
> <span data-ttu-id="3091e-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="3091e-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3091e-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3091e-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3091e-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3091e-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3091e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3091e-122">Requirements</span></span>



| <span data-ttu-id="3091e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3091e-123">Requirement</span></span> | <span data-ttu-id="3091e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3091e-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3091e-125">Version</span><span class="sxs-lookup"><span data-stu-id="3091e-125">Version</span></span><br/> | <span data-ttu-id="3091e-126">DirectX 9,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="3091e-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="3091e-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="3091e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3091e-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3091e-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3091e-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3091e-129">Library</span></span><br/> | <dl> <span data-ttu-id="3091e-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3091e-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3091e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3091e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3091e-132">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="3091e-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="3091e-133">**Interface IResize**</span><span class="sxs-lookup"><span data-stu-id="3091e-133">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




