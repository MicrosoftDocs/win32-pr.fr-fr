---
description: Crée un objet de mémoire tampon.
ms.assetid: 6f44fe84-3e0b-4fb8-821a-c997944fed37
title: D3DXCreateBuffer, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc54813ea9947d263febcbe843702124c68ba747
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523228"
---
# <a name="d3dxcreatebuffer-function"></a><span data-ttu-id="d00cf-103">D3DXCreateBuffer fonction)</span><span class="sxs-lookup"><span data-stu-id="d00cf-103">D3DXCreateBuffer function</span></span>

<span data-ttu-id="d00cf-104">Crée un objet de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d00cf-104">Creates a buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d00cf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d00cf-105">Syntax</span></span>


```C++
HRESULT D3DXCreateBuffer(
  _In_  DWORD        NumBytes,
  _Out_ LPD3DXBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="d00cf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d00cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d00cf-107">*NumBytes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d00cf-107">*NumBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d00cf-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d00cf-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d00cf-109">Taille de la mémoire tampon à créer, en octets.</span><span class="sxs-lookup"><span data-stu-id="d00cf-109">Size of the buffer to create, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d00cf-110">*ppBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d00cf-110">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d00cf-111">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d00cf-111">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d00cf-112">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) , représentant l’objet de mémoire tampon créé.</span><span class="sxs-lookup"><span data-stu-id="d00cf-112">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, representing the created buffer object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d00cf-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d00cf-113">Return value</span></span>

<span data-ttu-id="d00cf-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d00cf-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d00cf-115">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d00cf-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d00cf-116">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d00cf-116">If the function fails, the return value can be one of the following: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="d00cf-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d00cf-117">Requirements</span></span>



| <span data-ttu-id="d00cf-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d00cf-118">Requirement</span></span> | <span data-ttu-id="d00cf-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d00cf-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d00cf-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d00cf-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d00cf-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d00cf-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d00cf-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d00cf-122">Library</span></span><br/> | <dl> <span data-ttu-id="d00cf-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d00cf-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d00cf-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d00cf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d00cf-125">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="d00cf-125">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
