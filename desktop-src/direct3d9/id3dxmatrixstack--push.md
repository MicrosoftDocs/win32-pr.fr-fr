---
description: ID3DXMATRIXStack ::P méthode par émission (D3dx9math. h)-ajoute une matrice à la pile.
ms.assetid: 99bc636d-f1fd-4ace-a649-6a1a952927e0
title: ID3DXMATRIXStack ::P méthode par émission (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aeaf40d3164d6bd9d892d30f352fd24467b24ddb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093501"
---
# <a name="id3dxmatrixstackpush-method-d3dx9mathh"></a><span data-ttu-id="76f06-103">ID3DXMATRIXStack ::P méthode par émission (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="76f06-103">ID3DXMATRIXStack::Push method (D3dx9math.h)</span></span>

<span data-ttu-id="76f06-104">Ajoute une matrice à la pile.</span><span class="sxs-lookup"><span data-stu-id="76f06-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="76f06-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76f06-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="76f06-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76f06-106">Parameters</span></span>

<span data-ttu-id="76f06-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="76f06-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="76f06-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="76f06-108">Return value</span></span>

<span data-ttu-id="76f06-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="76f06-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="76f06-110">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="76f06-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="76f06-111">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="76f06-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="76f06-112">Notes </span><span class="sxs-lookup"><span data-stu-id="76f06-112">Remarks</span></span>

<span data-ttu-id="76f06-113">Cette méthode incrémente le nombre d’éléments sur la pile de 1, en dupliquant la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="76f06-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="76f06-114">La pile croît de manière dynamique à mesure que d’autres éléments sont ajoutés.</span><span class="sxs-lookup"><span data-stu-id="76f06-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="76f06-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76f06-115">Requirements</span></span>



| <span data-ttu-id="76f06-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76f06-116">Requirement</span></span> | <span data-ttu-id="76f06-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="76f06-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76f06-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="76f06-118">Header</span></span><br/>  | <dl> <span data-ttu-id="76f06-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="76f06-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="76f06-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="76f06-120">Library</span></span><br/> | <dl> <span data-ttu-id="76f06-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76f06-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="76f06-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76f06-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76f06-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="76f06-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="76f06-124">**ID3DXMATRIXStack :: GetTop**</span><span class="sxs-lookup"><span data-stu-id="76f06-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="76f06-125">**ID3DXMATRIXStack ::P op**</span><span class="sxs-lookup"><span data-stu-id="76f06-125">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> </dl>

 

 




