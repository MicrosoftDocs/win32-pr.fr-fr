---
description: Charge l’identité dans la matrice actuelle.
ms.assetid: e314a51f-4016-4819-a95d-d91864a54b2e
title: 'ID3DXMATRIXStack :: LoadIdentity, méthode (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e7ebc7b61679dc3938c2a57aa2346a45b136e5a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539432"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx9mathh"></a><span data-ttu-id="dd8dc-103">ID3DXMATRIXStack :: LoadIdentity, méthode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="dd8dc-103">ID3DXMATRIXStack::LoadIdentity method (D3dx9math.h)</span></span>

<span data-ttu-id="dd8dc-104">Charge l’identité dans la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd8dc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd8dc-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="dd8dc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd8dc-106">Parameters</span></span>

<span data-ttu-id="dd8dc-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dd8dc-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd8dc-108">Return value</span></span>

<span data-ttu-id="dd8dc-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dd8dc-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dd8dc-110">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dd8dc-111">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd8dc-112">Notes</span><span class="sxs-lookup"><span data-stu-id="dd8dc-112">Remarks</span></span>

<span data-ttu-id="dd8dc-113">La matrice d’identité est une matrice dans laquelle tous les coefficients sont 0,0, à l’exception des \[ coefficients 1, 1, 2 \] \[ \] \[ 3, 3 \] \[ 4, 4 \] , qui sont définis sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="dd8dc-114">La matrice d’identité est spéciale dans le cas où elle est appliquée aux sommets, mais elle n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="dd8dc-115">La matrice d’identité est utilisée comme point de départ pour les matrices qui modifient les valeurs de vertex pour créer des rotations, des translations et d’autres transformations qui peuvent être représentées par une matrice 4x4.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd8dc-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd8dc-116">Requirements</span></span>



| <span data-ttu-id="dd8dc-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd8dc-117">Requirement</span></span> | <span data-ttu-id="dd8dc-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd8dc-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd8dc-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd8dc-119">Header</span></span><br/>  | <dl> <span data-ttu-id="dd8dc-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd8dc-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="dd8dc-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dd8dc-121">Library</span></span><br/> | <dl> <span data-ttu-id="dd8dc-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd8dc-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dd8dc-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd8dc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd8dc-124">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="dd8dc-124">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="dd8dc-125">**ID3DXMATRIXStack::LoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="dd8dc-125">**ID3DXMATRIXStack::LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)
</dt> </dl>

 

 




