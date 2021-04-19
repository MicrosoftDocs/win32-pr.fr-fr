---
description: Récupère des informations sur un fichier image donné.
ms.assetid: 2e9d7073-4136-4fb7-8749-810aee000433
title: D3DXGetImageInfoFromFile, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ff5d540871482b2628fd48deb382121591a9594f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531335"
---
# <a name="d3dxgetimageinfofromfile-function"></a><span data-ttu-id="46da6-103">D3DXGetImageInfoFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="46da6-103">D3DXGetImageInfoFromFile function</span></span>

<span data-ttu-id="46da6-104">Récupère des informations sur un fichier image donné.</span><span class="sxs-lookup"><span data-stu-id="46da6-104">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="46da6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46da6-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromFile(
  _In_ LPCSTR         pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="46da6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46da6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46da6-107">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46da6-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46da6-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46da6-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46da6-109">Nom de fichier de l’image sur laquelle récupérer des informations.</span><span class="sxs-lookup"><span data-stu-id="46da6-109">File name of image to retrieve information about.</span></span> <span data-ttu-id="46da6-110">Si UNICODE ou \_ Unicode sont définis, ce type de paramètre est LPCWSTR, sinon, le type est LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="46da6-110">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="46da6-111">*pSrcInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46da6-111">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46da6-112">Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="46da6-112">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="46da6-113">Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec la description des données dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="46da6-113">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46da6-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46da6-114">Return value</span></span>

<span data-ttu-id="46da6-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46da6-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46da6-116">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="46da6-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="46da6-117">Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="46da6-117">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="46da6-118">Notes</span><span class="sxs-lookup"><span data-stu-id="46da6-118">Remarks</span></span>

<span data-ttu-id="46da6-119">Cette fonction prend en charge les chaînes Unicode et ANSI.</span><span class="sxs-lookup"><span data-stu-id="46da6-119">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="46da6-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46da6-120">Requirements</span></span>



| <span data-ttu-id="46da6-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46da6-121">Requirement</span></span> | <span data-ttu-id="46da6-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="46da6-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46da6-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="46da6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="46da6-124"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="46da6-124"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="46da6-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="46da6-125">Library</span></span><br/> | <dl> <span data-ttu-id="46da6-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46da6-126"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="46da6-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46da6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46da6-128">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="46da6-128">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="46da6-129">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="46da6-129">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="46da6-130">**D3DXGetImageInfoFromResource**</span><span class="sxs-lookup"><span data-stu-id="46da6-130">**D3DXGetImageInfoFromResource**</span></span>](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
