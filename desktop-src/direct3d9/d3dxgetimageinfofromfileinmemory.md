---
description: Récupère des informations sur un fichier image donné en mémoire.
ms.assetid: 6363aaf1-abfc-49df-9b99-be8a1c3540e1
title: D3DXGetImageInfoFromFileInMemory, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2bad56cb2aa769be80a6b031b1783d8717bc485
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538512"
---
# <a name="d3dxgetimageinfofromfileinmemory-function"></a><span data-ttu-id="f4af7-103">D3DXGetImageInfoFromFileInMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="f4af7-103">D3DXGetImageInfoFromFileInMemory function</span></span>

<span data-ttu-id="f4af7-104">Récupère des informations sur un fichier image donné en mémoire.</span><span class="sxs-lookup"><span data-stu-id="f4af7-104">Retrieves information about a given image file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4af7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4af7-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromFileInMemory(
  _In_ LPCVOID        pSrcData,
  _In_ UINT           SrcDataSize,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="f4af7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4af7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4af7-107">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f4af7-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4af7-108">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4af7-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4af7-109">Pointeur VOID vers le fichier source en mémoire.</span><span class="sxs-lookup"><span data-stu-id="f4af7-109">VOID pointer to the source file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="f4af7-110">*SrcDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f4af7-110">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4af7-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4af7-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4af7-112">Taille du fichier en mémoire, en octets.</span><span class="sxs-lookup"><span data-stu-id="f4af7-112">Size of file in memory, in bytes.</span></span> <span data-ttu-id="f4af7-113">.</span><span class="sxs-lookup"><span data-stu-id="f4af7-113">.</span></span>

</dd> <dt>

<span data-ttu-id="f4af7-114">*pSrcInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f4af7-114">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4af7-115">Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="f4af7-115">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="f4af7-116">Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec la description des données dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="f4af7-116">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4af7-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f4af7-117">Return value</span></span>

<span data-ttu-id="f4af7-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f4af7-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f4af7-119">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f4af7-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f4af7-120">Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="f4af7-120">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="f4af7-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4af7-121">Requirements</span></span>



| <span data-ttu-id="f4af7-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4af7-122">Requirement</span></span> | <span data-ttu-id="f4af7-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4af7-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4af7-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4af7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f4af7-125"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4af7-125"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f4af7-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f4af7-126">Library</span></span><br/> | <dl> <span data-ttu-id="f4af7-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4af7-127"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f4af7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4af7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4af7-129">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="f4af7-129">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="f4af7-130">**D3DXGetImageInfoFromFile**</span><span class="sxs-lookup"><span data-stu-id="f4af7-130">**D3DXGetImageInfoFromFile**</span></span>](d3dxgetimageinfofromfile.md)
</dt> <dt>

[<span data-ttu-id="f4af7-131">**D3DXGetImageInfoFromResource**</span><span class="sxs-lookup"><span data-stu-id="f4af7-131">**D3DXGetImageInfoFromResource**</span></span>](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
