---
description: Obtenir des informations sur une image déjà chargée en mémoire.
ms.assetid: 6750116a-ad4f-4102-aba9-6ef32c367be4
title: D3DX10GetImageInfoFromMemory, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 677ce6a2ac8e4e165ca0a2bbb64b6254870e4ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523190"
---
# <a name="d3dx10getimageinfofrommemory-function"></a><span data-ttu-id="e2ebb-103">D3DX10GetImageInfoFromMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="e2ebb-103">D3DX10GetImageInfoFromMemory function</span></span>

<span data-ttu-id="e2ebb-104">Obtenir des informations sur une image déjà chargée en mémoire.</span><span class="sxs-lookup"><span data-stu-id="e2ebb-104">Get information about an image already loaded into memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2ebb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2ebb-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="e2ebb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2ebb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2ebb-107">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e2ebb-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2ebb-108">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2ebb-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2ebb-109">Pointeur vers l’image en mémoire.</span><span class="sxs-lookup"><span data-stu-id="e2ebb-109">Pointer to the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="e2ebb-110">*SrcDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e2ebb-110">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2ebb-111">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2ebb-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2ebb-112">Taille de l’image en mémoire, en octets.</span><span class="sxs-lookup"><span data-stu-id="e2ebb-112">Size of the image in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e2ebb-113">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e2ebb-113">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2ebb-114">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2ebb-114">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="e2ebb-115">Pompe de thread facultative qui peut être utilisée pour charger les informations de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e2ebb-115">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="e2ebb-116">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e2ebb-116">Can be **NULL**.</span></span> <span data-ttu-id="e2ebb-117">Consultez [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="e2ebb-117">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2ebb-118">*pSrcInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e2ebb-118">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2ebb-119">Type : **[ **\_ \_ informations sur l’image d3dx10**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2ebb-119">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="e2ebb-120">Informations sur l’image en mémoire.</span><span class="sxs-lookup"><span data-stu-id="e2ebb-120">Information about the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="e2ebb-121">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e2ebb-121">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2ebb-122">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="e2ebb-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="e2ebb-123">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e2ebb-123">A pointer to the return value.</span></span> <span data-ttu-id="e2ebb-124">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e2ebb-124">May be **NULL**.</span></span> <span data-ttu-id="e2ebb-125">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="e2ebb-125">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2ebb-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e2ebb-126">Return value</span></span>

<span data-ttu-id="e2ebb-127">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e2ebb-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e2ebb-128">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e2ebb-128">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2ebb-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2ebb-129">Requirements</span></span>



| <span data-ttu-id="e2ebb-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2ebb-130">Requirement</span></span> | <span data-ttu-id="e2ebb-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2ebb-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2ebb-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2ebb-132">Header</span></span><br/>  | <dl> <span data-ttu-id="e2ebb-133"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2ebb-133"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e2ebb-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e2ebb-134">Library</span></span><br/> | <dl> <span data-ttu-id="e2ebb-135"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2ebb-135"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e2ebb-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2ebb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2ebb-137">Fonctions de texture dans D3DX 10</span><span class="sxs-lookup"><span data-stu-id="e2ebb-137">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
