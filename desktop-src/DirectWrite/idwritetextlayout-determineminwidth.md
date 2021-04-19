---
title: Méthode IDWriteTextLayout DetermineMinWidth
description: Détermine la largeur minimale possible pour laquelle la disposition peut être définie sans rupture d’urgence entre les caractères de mots entiers se produisant.
ms.assetid: 8efa1471-1b74-46d4-ac6d-fb1839ce2e74
keywords:
- Écriture directe de la méthode DetermineMinWidth
- Méthode DetermineMinWidth Write directe, interface IDWriteTextLayout
- Écriture directe de l’interface IDWriteTextLayout, méthode DetermineMinWidth
topic_type:
- apiref
api_name:
- IDWriteTextLayout.DetermineMinWidth
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2525f770030b80f0e9c0d6df9e5ec88becbb394b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534783"
---
# <a name="idwritetextlayoutdetermineminwidth-method"></a><span data-ttu-id="25825-106">IDWriteTextLayout ::D méthode etermineMinWidth</span><span class="sxs-lookup"><span data-stu-id="25825-106">IDWriteTextLayout::DetermineMinWidth method</span></span>

<span data-ttu-id="25825-107">Détermine la largeur minimale possible pour laquelle la disposition peut être définie sans rupture d’urgence entre les caractères de mots entiers se produisant.</span><span class="sxs-lookup"><span data-stu-id="25825-107">Determines the minimum possible width the layout can be set to without emergency breaking between the characters of whole words occurring.</span></span>

## <a name="syntax"></a><span data-ttu-id="25825-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25825-108">Syntax</span></span>


```C++
virtual HRESULT DetermineMinWidth(
  [out] FLOAT *minWidth
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="25825-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25825-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25825-110">*minWidth* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="25825-110">*minWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25825-111">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="25825-111">Type: **FLOAT\***</span></span>

<span data-ttu-id="25825-112">Largeur minimale.</span><span class="sxs-lookup"><span data-stu-id="25825-112">Minimum width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25825-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25825-113">Return value</span></span>

<span data-ttu-id="25825-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="25825-114">Type: **HRESULT**</span></span>

<span data-ttu-id="25825-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="25825-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="25825-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="25825-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="25825-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25825-117">Requirements</span></span>



| <span data-ttu-id="25825-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25825-118">Requirement</span></span> | <span data-ttu-id="25825-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="25825-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25825-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="25825-120">Library</span></span><br/> | <dl> <span data-ttu-id="25825-121"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25825-121"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="25825-122">DLL</span><span class="sxs-lookup"><span data-stu-id="25825-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="25825-123"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25825-123"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25825-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25825-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25825-125">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="25825-125">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="25825-126">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="25825-126">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

