---
title: Méthode IDWriteTextLayout3 GetLineMetrics
description: Récupère les propriétés de chaque ligne.
ms.assetid: 352ca3e3-7b08-823c-0881-0b051d4ce574
keywords:
- Écriture directe de la méthode GetLineMetrics
- Méthode GetLineMetrics Write directe, interface IDWriteTextLayout3
- Écriture directe de l’interface IDWriteTextLayout3, méthode GetLineMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d10a06cbf123b71e1308b45c747ac8a840a5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465842"
---
# <a name="idwritetextlayout3getlinemetrics-method"></a><span data-ttu-id="36fed-106">IDWriteTextLayout3 :: GetLineMetrics, méthode</span><span class="sxs-lookup"><span data-stu-id="36fed-106">IDWriteTextLayout3::GetLineMetrics method</span></span>

<span data-ttu-id="36fed-107">Récupère les propriétés de chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="36fed-107">Retrieves properties of each line.</span></span>

## <a name="syntax"></a><span data-ttu-id="36fed-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36fed-108">Syntax</span></span>


```C++
HRESULT GetLineMetrics(
  [out] DWRITE_LINE_METRICS1 *lineMetrics,
        UINT32               maxLineCount,
  [out] UINT32               *actualLineCount
);
```



## <a name="parameters"></a><span data-ttu-id="36fed-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36fed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36fed-110">*lineMetrics* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="36fed-110">*lineMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36fed-111">Tableau à remplir avec les informations de ligne.</span><span class="sxs-lookup"><span data-stu-id="36fed-111">The array to fill with line information.</span></span>

</dd> <dt>

<span data-ttu-id="36fed-112">*maxLineCount*</span><span class="sxs-lookup"><span data-stu-id="36fed-112">*maxLineCount*</span></span> 
</dt> <dd>

<span data-ttu-id="36fed-113">Taille maximale du tableau lineMetrics.</span><span class="sxs-lookup"><span data-stu-id="36fed-113">The maximum size of the lineMetrics array.</span></span>

</dd> <dt>

<span data-ttu-id="36fed-114">*actualLineCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="36fed-114">*actualLineCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36fed-115">Taille réelle du tableau lineMetrics nécessaire.</span><span class="sxs-lookup"><span data-stu-id="36fed-115">The actual size of the lineMetrics array that is needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36fed-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36fed-116">Return value</span></span>

<span data-ttu-id="36fed-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="36fed-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="36fed-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="36fed-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="36fed-119">Notes</span><span class="sxs-lookup"><span data-stu-id="36fed-119">Remarks</span></span>

<span data-ttu-id="36fed-120">Si maxLineCount n’est pas assez grand \_ \_ , E \_ mémoire tampon insuffisante, qui est équivalente à HRESULT \_ de \_ Win32 (erreur de \_ mémoire tampon insuffisante \_ ), est retourné et actualLineCount est défini sur le nombre de lignes nécessaires.</span><span class="sxs-lookup"><span data-stu-id="36fed-120">If maxLineCount is not large enough E\_NOT\_SUFFICIENT\_BUFFER, which is equivalent to HRESULT\_FROM\_WIN32(ERROR\_INSUFFICIENT\_BUFFER), is returned and actualLineCount is set to the number of lines needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="36fed-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36fed-121">Requirements</span></span>



| <span data-ttu-id="36fed-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36fed-122">Requirement</span></span> | <span data-ttu-id="36fed-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="36fed-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36fed-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36fed-124">Minimum supported client</span></span><br/> | <span data-ttu-id="36fed-125">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36fed-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="36fed-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36fed-126">Minimum supported server</span></span><br/> | <span data-ttu-id="36fed-127">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36fed-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="36fed-128">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36fed-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="36fed-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="36fed-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="36fed-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="36fed-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="36fed-131"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36fed-131"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="36fed-132">DLL</span><span class="sxs-lookup"><span data-stu-id="36fed-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36fed-133"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36fed-133"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="36fed-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36fed-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36fed-135">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="36fed-135">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





