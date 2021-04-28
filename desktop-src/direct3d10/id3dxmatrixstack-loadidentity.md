---
description: 'ID3DXMATRIXStack :: LoadIdentity, méthode (D3DX10. h)-charge l’identité dans la matrice actuelle.'
ms.assetid: 324b49c2-3aca-4bbb-90f3-62f3ffb2fa45
title: 'ID3DXMATRIXStack :: LoadIdentity, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadIdentity
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f056a911b19c0ea18f5f728a6ce8c4403dd14587
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107987"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx10h"></a><span data-ttu-id="af26b-103">ID3DXMATRIXStack :: LoadIdentity, méthode (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="af26b-103">ID3DXMATRIXStack::LoadIdentity method (D3DX10.h)</span></span>

<span data-ttu-id="af26b-104">Charge l’identité dans la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="af26b-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="af26b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af26b-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="af26b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af26b-106">Parameters</span></span>

<span data-ttu-id="af26b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="af26b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="af26b-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="af26b-108">Return value</span></span>

<span data-ttu-id="af26b-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="af26b-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="af26b-110">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="af26b-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="af26b-111">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="af26b-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="af26b-112">Notes </span><span class="sxs-lookup"><span data-stu-id="af26b-112">Remarks</span></span>

<span data-ttu-id="af26b-113">La matrice d’identité est une matrice dans laquelle tous les coefficients sont 0,0, à l’exception des \[ coefficients 1, 1, 2 \] \[ \] \[ 3, 3 \] \[ 4, 4 \] , qui sont définis sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="af26b-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="af26b-114">La matrice d’identité est spéciale dans le cas où elle est appliquée aux sommets, mais elle n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="af26b-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="af26b-115">La matrice d’identité est utilisée comme point de départ pour les matrices qui modifient les valeurs de vertex pour créer des rotations, des translations et d’autres transformations qui peuvent être représentées par une matrice 4x4.</span><span class="sxs-lookup"><span data-stu-id="af26b-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="af26b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af26b-116">Requirements</span></span>



| <span data-ttu-id="af26b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af26b-117">Requirement</span></span> | <span data-ttu-id="af26b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="af26b-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af26b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="af26b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="af26b-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="af26b-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="af26b-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="af26b-121">Library</span></span><br/> | <dl> <span data-ttu-id="af26b-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af26b-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af26b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af26b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af26b-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="af26b-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="af26b-125">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="af26b-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




