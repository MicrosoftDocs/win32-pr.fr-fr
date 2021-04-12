---
title: Méthode IDWriteTextLayout3 InvalidateLayout
description: Invalide la disposition, en forçant la disposition à la mesure avant d’appeler les mesures ou les fonctions de dessin. Cela est utile si la localité d’une police change et si la disposition doit être redessinée, ou si la taille d’un client implémentant IDWriteInlineObject est modifiée.
ms.assetid: 65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7
keywords:
- Écriture directe de la méthode InvalidateLayout
- Méthode InvalidateLayout Write directe, interface IDWriteTextLayout3
- Écriture directe de l’interface IDWriteTextLayout3, méthode InvalidateLayout
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.InvalidateLayout
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5df97d4590f62f586a570d52428b6560a7d88df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104404"
---
# <a name="idwritetextlayout3invalidatelayout-method"></a><span data-ttu-id="ea56f-107">IDWriteTextLayout3 :: InvalidateLayout, méthode</span><span class="sxs-lookup"><span data-stu-id="ea56f-107">IDWriteTextLayout3::InvalidateLayout method</span></span>

<span data-ttu-id="ea56f-108">Invalide la disposition, en forçant la disposition à la mesure avant d’appeler les mesures ou les fonctions de dessin.</span><span class="sxs-lookup"><span data-stu-id="ea56f-108">Invalidates the layout, forcing layout to remeasure before calling the metrics or drawing functions.</span></span> <span data-ttu-id="ea56f-109">Cela est utile si la localité d’une police change et si la disposition doit être redessinée, ou si la taille d’un client implémentant IDWriteInlineObject est modifiée.</span><span class="sxs-lookup"><span data-stu-id="ea56f-109">This is useful if the locality of a font changes, and layout should be redrawn, or if the size of a client implemented IDWriteInlineObject changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea56f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea56f-110">Syntax</span></span>


```C++
HRESULT InvalidateLayout();
```



## <a name="parameters"></a><span data-ttu-id="ea56f-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea56f-111">Parameters</span></span>

<span data-ttu-id="ea56f-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ea56f-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea56f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea56f-113">Return value</span></span>

<span data-ttu-id="ea56f-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ea56f-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ea56f-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ea56f-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea56f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea56f-116">Requirements</span></span>



| <span data-ttu-id="ea56f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea56f-117">Requirement</span></span> | <span data-ttu-id="ea56f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea56f-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea56f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea56f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ea56f-120">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea56f-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ea56f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea56f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ea56f-122">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea56f-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ea56f-123">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea56f-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="ea56f-124">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="ea56f-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="ea56f-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ea56f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="ea56f-126"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea56f-126"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ea56f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ea56f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea56f-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea56f-128"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ea56f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea56f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea56f-130">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="ea56f-130">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





