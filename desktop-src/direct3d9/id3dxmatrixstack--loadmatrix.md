---
description: Charge la matrice donnée dans la matrice actuelle.
ms.assetid: c4c5ac50-238f-4b41-8ea9-7e48ffd03fc5
title: 'ID3DXMATRIXStack :: LoadMatrix, méthode (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 292b4e147dfa99023f0b4d560a4ed41e6b41b3fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530861"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx9mathh"></a><span data-ttu-id="e4fb0-103">ID3DXMATRIXStack :: LoadMatrix, méthode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e4fb0-103">ID3DXMATRIXStack::LoadMatrix method (D3dx9math.h)</span></span>

<span data-ttu-id="e4fb0-104">Charge la matrice donnée dans la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="e4fb0-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4fb0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4fb0-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="e4fb0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4fb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4fb0-107">*pMat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4fb0-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4fb0-108">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4fb0-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e4fb0-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) chargée dans la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="e4fb0-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4fb0-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e4fb0-110">Return value</span></span>

<span data-ttu-id="e4fb0-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e4fb0-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e4fb0-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e4fb0-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e4fb0-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e4fb0-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4fb0-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e4fb0-114">Remarks</span></span>

<span data-ttu-id="e4fb0-115">Notez que cette méthode n’ajoute pas d’élément à la pile ; au lieu de cela, elle remplace la matrice actuelle par la matrice fournie.</span><span class="sxs-lookup"><span data-stu-id="e4fb0-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4fb0-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4fb0-116">Requirements</span></span>



| <span data-ttu-id="e4fb0-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4fb0-117">Requirement</span></span> | <span data-ttu-id="e4fb0-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4fb0-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4fb0-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4fb0-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e4fb0-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4fb0-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e4fb0-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e4fb0-121">Library</span></span><br/> | <dl> <span data-ttu-id="e4fb0-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4fb0-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e4fb0-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4fb0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4fb0-124">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="e4fb0-124">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="e4fb0-125">**ID3DXMATRIXStack::LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="e4fb0-125">**ID3DXMATRIXStack::LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)
</dt> </dl>

 

 




