---
description: Enregistrer une texture dans un fichier.
ms.assetid: c1718903-039a-4132-b128-82e03078ef62
title: D3DX10SaveTextureToFile, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c760876160d8ce1cbc0423639a59218c79716481
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535215"
---
# <a name="d3dx10savetexturetofile-function"></a><span data-ttu-id="3c3c3-103">D3DX10SaveTextureToFile fonction)</span><span class="sxs-lookup"><span data-stu-id="3c3c3-103">D3DX10SaveTextureToFile function</span></span>

<span data-ttu-id="3c3c3-104">Enregistrer une texture dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="3c3c3-104">Save a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c3c3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c3c3-105">Syntax</span></span>


```C++
HRESULT D3DX10SaveTextureToFile(
  _In_ ID3D10Resource           *pSrcTexture,
  _In_ D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a><span data-ttu-id="3c3c3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c3c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c3c3-107">*pSrcTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c3c3-107">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c3c3-108">Type : **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="3c3c3-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="3c3c3-109">Pointeur vers la texture à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="3c3c3-109">Pointer to the texture to be saved.</span></span> <span data-ttu-id="3c3c3-110">Voir [**interface ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="3c3c3-110">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="3c3c3-111">*DestFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c3c3-111">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c3c3-112">Type : **[ **d3dx10 \_ image \_ file \_ format**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="3c3c3-112">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

<span data-ttu-id="3c3c3-113">Format dans lequel la texture sera enregistrée (voir [**format de \_ \_ fichier image \_ d3dx10**](d3dx10-image-file-format.md)).</span><span class="sxs-lookup"><span data-stu-id="3c3c3-113">The format the texture will be saved as (see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)).</span></span> <span data-ttu-id="3c3c3-114">D3DX10 \_ IFF \_ DDS est le format par défaut, car il s’agit de la seule option qui prend en charge tous les formats au [**\_ format dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="3c3c3-114">D3DX10\_IFF\_DDS is the preferred format since it is the only option that supports all the formats in [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="3c3c3-115">*pDestFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c3c3-115">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c3c3-116">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c3c3-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c3c3-117">Nom du fichier de sortie de destination dans lequel la texture sera enregistrée.</span><span class="sxs-lookup"><span data-stu-id="3c3c3-117">Name of the destination output file where the texture will be saved.</span></span> <span data-ttu-id="3c3c3-118">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="3c3c3-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="3c3c3-119">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="3c3c3-119">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c3c3-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c3c3-120">Return value</span></span>

<span data-ttu-id="3c3c3-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c3c3-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c3c3-122">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md). Utilisez la valeur de retour pour voir si le *DestFormat* est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3c3c3-122">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md); use the return value to see if the *DestFormat* is supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c3c3-123">Notes</span><span class="sxs-lookup"><span data-stu-id="3c3c3-123">Remarks</span></span>

<span data-ttu-id="3c3c3-124">**D3DX10SaveTextureToFile** écrit la structure [**\_ \_ DXT10 en-tête DDS**](../direct3ddds/dds-header-dxt10.md) supplémentaire pour la texture d’entrée uniquement si nécessaire (par exemple, parce que la texture d’entrée est au format RVB standard (sRVB)).</span><span class="sxs-lookup"><span data-stu-id="3c3c3-124">**D3DX10SaveTextureToFile** writes out the extra [**DDS\_HEADER\_DXT10**](../direct3ddds/dds-header-dxt10.md) structure for the input texture only if necessary (for example, because the input texture is in standard RGB (sRGB) format).</span></span> <span data-ttu-id="3c3c3-125">Si **D3DX10SaveTextureToFile** écrit la structure **DXT10 de l' \_ en-tête \_ DDS** , il définit le membre **dwFourCC** de la structure [**DDS \_ PIXELFORMAT**](../direct3ddds/dds-pixelformat.md) pour la texture sur **facilement** pour indiquer le Prescense de l’en-tête étendu DXT10 de l' **\_ en-tête \_ DDS** .</span><span class="sxs-lookup"><span data-stu-id="3c3c3-125">If **D3DX10SaveTextureToFile** writes out the **DDS\_HEADER\_DXT10** structure, it sets the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](../direct3ddds/dds-pixelformat.md) structure for the texture to **DX10** to indicate the prescense of the **DDS\_HEADER\_DXT10** extended header.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c3c3-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c3c3-126">Requirements</span></span>



| <span data-ttu-id="3c3c3-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c3c3-127">Requirement</span></span> | <span data-ttu-id="3c3c3-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c3c3-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c3c3-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c3c3-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3c3c3-130"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c3c3-130"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="3c3c3-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3c3c3-131">Library</span></span><br/> | <dl> <span data-ttu-id="3c3c3-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c3c3-132"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3c3c3-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c3c3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c3c3-134">Fonctions de texture dans D3DX 10</span><span class="sxs-lookup"><span data-stu-id="3c3c3-134">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="3c3c3-135">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="3c3c3-135">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
