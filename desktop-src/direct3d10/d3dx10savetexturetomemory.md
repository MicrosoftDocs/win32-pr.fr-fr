---
description: Enregistrer une texture dans la mémoire.
ms.assetid: be541b99-6d07-480e-8f28-b7fc44566e7d
title: D3DX10SaveTextureToMemory, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f20278f9fc590e72f93051d5fdd4cfbd918098df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531339"
---
# <a name="d3dx10savetexturetomemory-function"></a><span data-ttu-id="d531a-103">D3DX10SaveTextureToMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="d531a-103">D3DX10SaveTextureToMemory function</span></span>

<span data-ttu-id="d531a-104">Enregistrer une texture dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d531a-104">Save a texture to memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="d531a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d531a-105">Syntax</span></span>


```C++
HRESULT D3DX10SaveTextureToMemory(
  _In_  ID3D10Resource           *pSrcTexture,
  _In_  D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="d531a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d531a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d531a-107">*pSrcTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d531a-107">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d531a-108">Type : **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="d531a-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="d531a-109">Pointeur vers la texture à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="d531a-109">Pointer to the texture to be saved.</span></span> <span data-ttu-id="d531a-110">Voir [**interface ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="d531a-110">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="d531a-111">*DestFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d531a-111">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d531a-112">Type : **[ **d3dx10 \_ image \_ file \_ format**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="d531a-112">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

<span data-ttu-id="d531a-113">Format dans lequel la texture sera enregistrée.</span><span class="sxs-lookup"><span data-stu-id="d531a-113">The format the texture will be saved as.</span></span> <span data-ttu-id="d531a-114">Consultez [**\_ format de \_ fichier \_ image d3dx10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="d531a-114">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

</dd> <dt>

<span data-ttu-id="d531a-115">*ppDestBuf* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d531a-115">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d531a-116">Type : **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="d531a-116">Type: **[**LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="d531a-117">Adresse d’un pointeur vers la mémoire contenant la texture enregistrée.</span><span class="sxs-lookup"><span data-stu-id="d531a-117">Address of a pointer to the memory containing the saved texture.</span></span> <span data-ttu-id="d531a-118">Voir [**interface ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob).</span><span class="sxs-lookup"><span data-stu-id="d531a-118">See [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob).</span></span>

</dd> <dt>

<span data-ttu-id="d531a-119">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="d531a-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d531a-120">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d531a-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d531a-121">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d531a-121">Optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d531a-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d531a-122">Return value</span></span>

<span data-ttu-id="d531a-123">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d531a-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d531a-124">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d531a-124">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d531a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d531a-125">Requirements</span></span>



| <span data-ttu-id="d531a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d531a-126">Requirement</span></span> | <span data-ttu-id="d531a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="d531a-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d531a-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="d531a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="d531a-129"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="d531a-129"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="d531a-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d531a-130">Library</span></span><br/> | <dl> <span data-ttu-id="d531a-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d531a-131"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d531a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d531a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d531a-133">Fonctions de texture dans D3DX 10</span><span class="sxs-lookup"><span data-stu-id="d531a-133">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="d531a-134">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="d531a-134">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
