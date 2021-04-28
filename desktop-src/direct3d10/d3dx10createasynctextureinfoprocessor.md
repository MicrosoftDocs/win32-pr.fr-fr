---
description: 'Fonction D3DX10CreateAsyncTextureInfoProcessor : créez un processeur de données à utiliser avec une pompe de thread.'
ms.assetid: e97b6aca-1839-48ea-8dab-b96a52ec2a68
title: D3DX10CreateAsyncTextureInfoProcessor, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureInfoProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a23c2062c5f17e00d03161483d3ab1cf2ff225d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102797"
---
# <a name="d3dx10createasynctextureinfoprocessor-function"></a><span data-ttu-id="9ef87-103">D3DX10CreateAsyncTextureInfoProcessor fonction)</span><span class="sxs-lookup"><span data-stu-id="9ef87-103">D3DX10CreateAsyncTextureInfoProcessor function</span></span>

<span data-ttu-id="9ef87-104">Créez un processeur de données à utiliser avec une [**pompe de thread**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="9ef87-104">Create a data processor to be used with a [**thread pump**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ef87-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ef87-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncTextureInfoProcessor(
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="9ef87-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ef87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ef87-107">*pLoadInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9ef87-107">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ef87-108">Type : **[ **\_ \_ \_ informations sur le chargement de l’image d3dx10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="9ef87-108">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="9ef87-109">facultatif.</span><span class="sxs-lookup"><span data-stu-id="9ef87-109">Optional.</span></span> <span data-ttu-id="9ef87-110">Identifie les caractéristiques d’une texture (voir informations sur le chargement de l' [**\_ image \_ \_ d3dx10**](d3dx10-image-load-info.md)) lorsque le processeur de données est créé ; affectez la valeur **null** pour lire les caractéristiques d’une texture lorsque la texture est chargée.</span><span class="sxs-lookup"><span data-stu-id="9ef87-110">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="9ef87-111">*ppDataProcessor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9ef87-111">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ef87-112">Type : **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9ef87-112">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="9ef87-113">Adresse d’un pointeur vers une mémoire tampon qui contient le processeur de données créé (voir [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="9ef87-113">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ef87-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9ef87-114">Return value</span></span>

<span data-ttu-id="9ef87-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9ef87-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9ef87-116">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9ef87-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9ef87-117">Notes </span><span class="sxs-lookup"><span data-stu-id="9ef87-117">Remarks</span></span>

<span data-ttu-id="9ef87-118">Cette API crée une interface de processeur de données. [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md) crée l’interface du processeur de données et charge la texture.</span><span class="sxs-lookup"><span data-stu-id="9ef87-118">This API does creates a data-processor interface; [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md) creates the data-processor interface and loads the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ef87-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ef87-119">Requirements</span></span>



| <span data-ttu-id="9ef87-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ef87-120">Requirement</span></span> | <span data-ttu-id="9ef87-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ef87-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ef87-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ef87-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9ef87-123"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ef87-123"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="9ef87-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9ef87-124">Library</span></span><br/> | <dl> <span data-ttu-id="9ef87-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ef87-125"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9ef87-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ef87-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ef87-127">Fonctions de texture dans D3DX 10</span><span class="sxs-lookup"><span data-stu-id="9ef87-127">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




