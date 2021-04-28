---
description: ID3DXMATRIXStack ::P méthode par émission (D3DX10. h)-ajoute une matrice à la pile.
ms.assetid: 8660047f-64bc-4b34-8270-3087412db942
title: ID3DXMATRIXStack ::P méthode par émission (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Push
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9c248fdaed8235c383388a52172021921e2c78d8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107915"
---
# <a name="id3dxmatrixstackpush-method-d3dx10h"></a><span data-ttu-id="d07bd-103">ID3DXMATRIXStack ::P méthode par émission (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="d07bd-103">ID3DXMATRIXStack::Push method (D3DX10.h)</span></span>

<span data-ttu-id="d07bd-104">Ajoute une matrice à la pile.</span><span class="sxs-lookup"><span data-stu-id="d07bd-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="d07bd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d07bd-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="d07bd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d07bd-106">Parameters</span></span>

<span data-ttu-id="d07bd-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d07bd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d07bd-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d07bd-108">Return value</span></span>

<span data-ttu-id="d07bd-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d07bd-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d07bd-110">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d07bd-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d07bd-111">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d07bd-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d07bd-112">Notes </span><span class="sxs-lookup"><span data-stu-id="d07bd-112">Remarks</span></span>

<span data-ttu-id="d07bd-113">Cette méthode incrémente le nombre d’éléments sur la pile de 1, en dupliquant la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="d07bd-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="d07bd-114">La pile croît de manière dynamique à mesure que d’autres éléments sont ajoutés.</span><span class="sxs-lookup"><span data-stu-id="d07bd-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="d07bd-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d07bd-115">Requirements</span></span>



| <span data-ttu-id="d07bd-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d07bd-116">Requirement</span></span> | <span data-ttu-id="d07bd-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d07bd-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d07bd-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="d07bd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d07bd-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d07bd-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d07bd-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d07bd-120">Library</span></span><br/> | <dl> <span data-ttu-id="d07bd-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d07bd-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d07bd-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d07bd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d07bd-123">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="d07bd-123">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="d07bd-124">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="d07bd-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




