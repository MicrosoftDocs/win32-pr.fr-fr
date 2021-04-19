---
description: Créez un processeur de données qui chargera une ressource, puis créez une vue de ressource de nuanceur pour celle-ci. Les processeurs de données sont un composant de la fonctionnalité de chargement de données asynchrone dans D3DX10 qui utilise des pompes de thread.
ms.assetid: 6e5a6138-c218-4200-a24e-d906d34933b8
title: D3DX10CreateAsyncShaderResourceViewProcessor, fonction (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderResourceViewProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: bd55e4191382c5abde52ce05d0a16b5533d79eac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535200"
---
# <a name="d3dx10createasyncshaderresourceviewprocessor-function"></a><span data-ttu-id="e3510-104">D3DX10CreateAsyncShaderResourceViewProcessor fonction)</span><span class="sxs-lookup"><span data-stu-id="e3510-104">D3DX10CreateAsyncShaderResourceViewProcessor function</span></span>

<span data-ttu-id="e3510-105">Créez un processeur de données qui chargera une ressource, puis créez une vue de ressource de nuanceur pour celle-ci.</span><span class="sxs-lookup"><span data-stu-id="e3510-105">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="e3510-106">Les processeurs de données sont un composant de la fonctionnalité de chargement de données asynchrone dans D3DX10 qui utilise des [**pompes de thread**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="e3510-106">Data processors are a component of the asynchronous data loading feature in D3DX10 that uses [**thread pumps**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e3510-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3510-107">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="e3510-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3510-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3510-109">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e3510-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3510-110">Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="e3510-110">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="e3510-111">Pointeur vers le périphérique Direct3D (voir [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) qui sera utilisé pour créer une ressource et un affichage des ressources de nuanceur pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="e3510-111">Pointer to the Direct3D device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will be used to create a resource and a shader-resource view for that resource.</span></span>

</dd> <dt>

<span data-ttu-id="e3510-112">*pLoadInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e3510-112">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3510-113">Type : **[ **\_ \_ \_ informations sur le chargement de l’image d3dx10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3510-113">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="e3510-114">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="e3510-114">Optional.</span></span> <span data-ttu-id="e3510-115">Identifie les caractéristiques d’une texture (voir informations sur le chargement de l' [**\_ image \_ \_ d3dx10**](d3dx10-image-load-info.md)) lorsque le processeur de données est créé ; affectez la valeur **null** pour lire les caractéristiques d’une texture lorsque la texture est chargée.</span><span class="sxs-lookup"><span data-stu-id="e3510-115">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="e3510-116">*ppDataProcessor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e3510-116">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3510-117">Type : **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e3510-117">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="e3510-118">Adresse d’un pointeur vers une mémoire tampon qui contient le processeur de données créé (voir [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="e3510-118">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3510-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e3510-119">Return value</span></span>

<span data-ttu-id="e3510-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e3510-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e3510-121">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e3510-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3510-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3510-122">Requirements</span></span>



| <span data-ttu-id="e3510-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3510-123">Requirement</span></span> | <span data-ttu-id="e3510-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3510-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3510-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3510-125">Header</span></span><br/> | <dl> <span data-ttu-id="e3510-126"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3510-126"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3510-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3510-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3510-128">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="e3510-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




