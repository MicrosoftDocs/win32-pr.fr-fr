---
description: Commence le traitement pour créer une image décodée.
ms.assetid: 80471cc6-c66d-49d9-8593-780e41ac39b9
title: 'IDirect3DDXVADevice9 :: BeginFrame, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.BeginFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3090d7868316d08fa91f36dffcc938eb31e06a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518203"
---
# <a name="idirect3ddxvadevice9beginframe-method"></a><span data-ttu-id="cb868-103">IDirect3DDXVADevice9 :: BeginFrame, méthode</span><span class="sxs-lookup"><span data-stu-id="cb868-103">IDirect3DDXVADevice9::BeginFrame method</span></span>

<span data-ttu-id="cb868-104">Commence le traitement pour créer une image décodée.</span><span class="sxs-lookup"><span data-stu-id="cb868-104">Begins the processing to create a decoded picture.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb868-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb868-105">Syntax</span></span>


```C++
HRESULT BeginFrame(
   IDirect3DSurface9 *pDstSurface,
   DWORD             SizeInputData,
   VOID              *pInputData,
   DWORD             *pSizeOutputData,
   VOID              *pOutputData
);
```



## <a name="parameters"></a><span data-ttu-id="cb868-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb868-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb868-107">*pDstSurface*</span><span class="sxs-lookup"><span data-stu-id="cb868-107">*pDstSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="cb868-108">Pointeur vers l’interface **IDirect3DSurface9** de la surface de destination non compressée.</span><span class="sxs-lookup"><span data-stu-id="cb868-108">A pointer to the **IDirect3DSurface9** interface of the uncompressed destination surface.</span></span>

</dd> <dt>

<span data-ttu-id="cb868-109">*SizeInputData*</span><span class="sxs-lookup"><span data-stu-id="cb868-109">*SizeInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="cb868-110">Taille de la mémoire tampon spécifiée par *pInputData*, en octets.</span><span class="sxs-lookup"><span data-stu-id="cb868-110">The size of the buffer specified by *pInputData*, in bytes.</span></span> <span data-ttu-id="cb868-111">La valeur doit être 2.</span><span class="sxs-lookup"><span data-stu-id="cb868-111">The value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="cb868-112">*pInputData*</span><span class="sxs-lookup"><span data-stu-id="cb868-112">*pInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="cb868-113">Pointeur vers une mémoire tampon qui contient des données pour l’accélérateur vidéo.</span><span class="sxs-lookup"><span data-stu-id="cb868-113">Pointer to a buffer that contains data for the video accelerator.</span></span> <span data-ttu-id="cb868-114">Cette mémoire tampon doit contenir l’index de frame de base zéro, spécifié sous la forme d’une valeur de **mot** .</span><span class="sxs-lookup"><span data-stu-id="cb868-114">This buffer must contain the zero-based frame index, specified as a **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="cb868-115">*pSizeOutputData*</span><span class="sxs-lookup"><span data-stu-id="cb868-115">*pSizeOutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="cb868-116">Taille de la mémoire tampon spécifiée par *pOutputData*, en octets.</span><span class="sxs-lookup"><span data-stu-id="cb868-116">The size of the buffer specified by *pOutputData*, in bytes.</span></span> <span data-ttu-id="cb868-117">La valeur doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="cb868-117">The value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cb868-118">*pOutputData*</span><span class="sxs-lookup"><span data-stu-id="cb868-118">*pOutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="cb868-119">Pointeur vers une mémoire tampon dans laquelle l’accélérateur vidéo peut écrire.</span><span class="sxs-lookup"><span data-stu-id="cb868-119">Pointer to a buffer that the video accelerator can write to.</span></span> <span data-ttu-id="cb868-120">Affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="cb868-120">Set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb868-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb868-121">Return value</span></span>

<span data-ttu-id="cb868-122">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cb868-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cb868-123">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cb868-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb868-124">Notes</span><span class="sxs-lookup"><span data-stu-id="cb868-124">Remarks</span></span>

<span data-ttu-id="cb868-125">Pour chaque appel à **BeginFrame**, le décodeur doit effectuer un appel correspondant à [**IDirect3DDXVADevice9 :: EndFrame**](idirect3ddxvadevice9-endframe.md).</span><span class="sxs-lookup"><span data-stu-id="cb868-125">For each call to **BeginFrame**, the decoder must make a corresponding call to [**IDirect3DDXVADevice9::EndFrame**](idirect3ddxvadevice9-endframe.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb868-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb868-126">Requirements</span></span>



| <span data-ttu-id="cb868-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb868-127">Requirement</span></span> | <span data-ttu-id="cb868-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb868-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cb868-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb868-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cb868-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb868-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cb868-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb868-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cb868-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb868-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cb868-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb868-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb868-134"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb868-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb868-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb868-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb868-136">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="cb868-136">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




