---
description: 'ID3DXMATRIXStack :: LoadMatrix, méthode (D3DX10. h)-charge la matrice donnée dans la matrice actuelle.'
ms.assetid: b898f344-db90-48e0-b457-0eb8d7b31dca
title: 'ID3DXMATRIXStack :: LoadMatrix, méthode (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 20c80f578abd5e35c89f3ecccedd2ab7fd59e812
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107957"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx10h"></a><span data-ttu-id="765ae-103">ID3DXMATRIXStack :: LoadMatrix, méthode (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="765ae-103">ID3DXMATRIXStack::LoadMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="765ae-104">Charge la matrice donnée dans la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="765ae-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="765ae-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="765ae-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="765ae-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="765ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="765ae-107">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="765ae-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="765ae-108">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="765ae-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="765ae-109">Pointeur vers la structure D3DXMATRIX chargée dans la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="765ae-109">Pointer to the D3DXMATRIX structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="765ae-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="765ae-110">Return value</span></span>

<span data-ttu-id="765ae-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="765ae-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="765ae-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="765ae-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="765ae-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="765ae-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="765ae-114">Notes </span><span class="sxs-lookup"><span data-stu-id="765ae-114">Remarks</span></span>

<span data-ttu-id="765ae-115">Notez que cette méthode n’ajoute pas d’élément à la pile ; au lieu de cela, elle remplace la matrice actuelle par la matrice fournie.</span><span class="sxs-lookup"><span data-stu-id="765ae-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="765ae-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="765ae-116">Requirements</span></span>



| <span data-ttu-id="765ae-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="765ae-117">Requirement</span></span> | <span data-ttu-id="765ae-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="765ae-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="765ae-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="765ae-119">Header</span></span><br/>  | <dl> <span data-ttu-id="765ae-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="765ae-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="765ae-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="765ae-121">Library</span></span><br/> | <dl> <span data-ttu-id="765ae-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="765ae-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="765ae-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="765ae-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="765ae-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="765ae-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="765ae-125">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="765ae-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
