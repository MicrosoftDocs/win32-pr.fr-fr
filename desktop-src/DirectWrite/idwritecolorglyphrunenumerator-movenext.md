---
title: Méthode MoveNext IDWriteColorGlyphRunEnumerator
description: Passe au glyphe suivant exécuté dans l’énumérateur.
ms.assetid: E6336C0E-F880-485C-9111-A102298257C1
keywords:
- Écriture directe de la méthode MoveNext
- Méthode MoveNext Write directe, interface IDWriteColorGlyphRunEnumerator
- Écriture directe de l’interface IDWriteColorGlyphRunEnumerator, méthode MoveNext
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator.MoveNext
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c9963916c07f1df8cf3cfedb49b9e3fd66d0df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508798"
---
# <a name="idwritecolorglyphrunenumeratormovenext-method"></a><span data-ttu-id="48d59-106">IDWriteColorGlyphRunEnumerator :: MoveNext, méthode</span><span class="sxs-lookup"><span data-stu-id="48d59-106">IDWriteColorGlyphRunEnumerator::MoveNext method</span></span>

<span data-ttu-id="48d59-107">Passe au glyphe suivant exécuté dans l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="48d59-107">Move to the next glyph run in the enumerator.</span></span>

## <a name="syntax"></a><span data-ttu-id="48d59-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48d59-108">Syntax</span></span>


```C++
HRESULT MoveNext(
  [out] BOOL *haveRun
);
```



## <a name="parameters"></a><span data-ttu-id="48d59-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48d59-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48d59-110">*haveRun* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="48d59-110">*haveRun* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48d59-111">Type : \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="48d59-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="48d59-112">Retourne _ *true*\* s’il y a une exécution de glyphe suivante.</span><span class="sxs-lookup"><span data-stu-id="48d59-112">Returns _ *TRUE*\* if there is a next glyph run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48d59-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="48d59-113">Return value</span></span>

<span data-ttu-id="48d59-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="48d59-114">Type: **HRESULT**</span></span>

<span data-ttu-id="48d59-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="48d59-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="48d59-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="48d59-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="48d59-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48d59-117">Requirements</span></span>



| <span data-ttu-id="48d59-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48d59-118">Requirement</span></span> | <span data-ttu-id="48d59-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="48d59-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48d59-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="48d59-120">Minimum supported client</span></span><br/> | <span data-ttu-id="48d59-121">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="48d59-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="48d59-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="48d59-122">Minimum supported server</span></span><br/> | <span data-ttu-id="48d59-123">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="48d59-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="48d59-124">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="48d59-124">Minimum supported phone</span></span><br/>  | <span data-ttu-id="48d59-125">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="48d59-125">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="48d59-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="48d59-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="48d59-127"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48d59-127"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="48d59-128">DLL</span><span class="sxs-lookup"><span data-stu-id="48d59-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48d59-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48d59-129"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="48d59-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48d59-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48d59-131">**IDWriteColorGlyphRunEnumerator**</span><span class="sxs-lookup"><span data-stu-id="48d59-131">**IDWriteColorGlyphRunEnumerator**</span></span>](idwritecolorglyphrunenumerator.md)
</dt> </dl>

 

 





