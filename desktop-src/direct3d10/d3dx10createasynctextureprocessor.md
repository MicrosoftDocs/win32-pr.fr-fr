---
description: Créez un processeur de données à utiliser avec une pompe de thread.
ms.assetid: c96b0ebb-7b9c-47d0-ad4f-fa62ddb74fa1
title: D3DX10CreateAsyncTextureProcessor, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d1d9c61729e72cc4ae5432361e9c1d968551b9c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043158"
---
# <a name="d3dx10createasynctextureprocessor-function"></a><span data-ttu-id="f46c3-103">D3DX10CreateAsyncTextureProcessor fonction)</span><span class="sxs-lookup"><span data-stu-id="f46c3-103">D3DX10CreateAsyncTextureProcessor function</span></span>

<span data-ttu-id="f46c3-104">Créez un processeur de données à utiliser avec une [**pompe de thread**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="f46c3-104">Create a data processor to be used with a [**thread pump**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f46c3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f46c3-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncTextureProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="f46c3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f46c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f46c3-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f46c3-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f46c3-108">Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="f46c3-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="f46c3-109">Pointeur vers la valeur devive (voir [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).</span><span class="sxs-lookup"><span data-stu-id="f46c3-109">A pointer to the devive (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).</span></span>

</dd> <dt>

<span data-ttu-id="f46c3-110">*pLoadInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f46c3-110">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f46c3-111">Type : **[ **\_ \_ \_ informations sur le chargement de l’image d3dx10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="f46c3-111">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="f46c3-112">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="f46c3-112">Optional.</span></span> <span data-ttu-id="f46c3-113">Identifie les caractéristiques d’une texture (voir informations sur le chargement de l' [**\_ image \_ \_ d3dx10**](d3dx10-image-load-info.md)) lorsque le processeur de données est créé ; affectez la valeur **null** pour lire les caractéristiques d’une texture lorsque la texture est chargée.</span><span class="sxs-lookup"><span data-stu-id="f46c3-113">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="f46c3-114">*ppDataProcessor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f46c3-114">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f46c3-115">Type : **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f46c3-115">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="f46c3-116">Adresse d’un pointeur vers une mémoire tampon qui contient le processeur de données créé (voir [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="f46c3-116">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f46c3-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f46c3-117">Return value</span></span>

<span data-ttu-id="f46c3-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f46c3-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f46c3-119">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f46c3-119">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f46c3-120">Notes</span><span class="sxs-lookup"><span data-stu-id="f46c3-120">Remarks</span></span>

<span data-ttu-id="f46c3-121">Cette API crée une interface de processeur de données et charge la texture. [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) crée l’interface du processeur de données.</span><span class="sxs-lookup"><span data-stu-id="f46c3-121">This API does creates a data-processor interface and loads the texture; [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) creates the data-processor interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="f46c3-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f46c3-122">Requirements</span></span>



| <span data-ttu-id="f46c3-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f46c3-123">Requirement</span></span> | <span data-ttu-id="f46c3-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f46c3-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f46c3-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f46c3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f46c3-126"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f46c3-126"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f46c3-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f46c3-127">Library</span></span><br/> | <dl> <span data-ttu-id="f46c3-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f46c3-128"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f46c3-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f46c3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f46c3-130">Fonctions de texture dans D3DX 10</span><span class="sxs-lookup"><span data-stu-id="f46c3-130">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




