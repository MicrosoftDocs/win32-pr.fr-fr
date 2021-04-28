---
description: 'ID3DXMATRIXStack :: ScaleLocal, méthode (D3dx9math. h)-mettez à l’échelle la matrice actuelle à propos de l’origine de l’objet.'
ms.assetid: fe71da67-c8c9-4c78-9055-9bc3cadc0780
title: 'ID3DXMATRIXStack :: ScaleLocal, méthode (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.ScaleLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5bd9f47b6c38b5ec72bcd25ecb5981859a87038b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093327"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx9mathh"></a><span data-ttu-id="6f101-103">ID3DXMATRIXStack :: ScaleLocal, méthode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="6f101-103">ID3DXMATRIXStack::ScaleLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="6f101-104">Mettre à l’échelle la matrice actuelle sur l’origine de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6f101-104">Scale the current matrix about the object origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f101-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f101-105">Syntax</span></span>


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="6f101-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f101-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f101-107">*x* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f101-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f101-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f101-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f101-109">Composant de mise à l’échelle sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="6f101-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="6f101-110">*y* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f101-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f101-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f101-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f101-112">Composant de mise à l’échelle sur l’axe y.</span><span class="sxs-lookup"><span data-stu-id="6f101-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="6f101-113">*z* \[\]</span><span class="sxs-lookup"><span data-stu-id="6f101-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f101-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f101-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f101-115">Composant de mise à l’échelle dans l’axe z.</span><span class="sxs-lookup"><span data-stu-id="6f101-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f101-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6f101-116">Return value</span></span>

<span data-ttu-id="6f101-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6f101-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6f101-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6f101-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f101-119">Notes </span><span class="sxs-lookup"><span data-stu-id="6f101-119">Remarks</span></span>

<span data-ttu-id="6f101-120">Cette méthode multiplie la matrice actuelle par la matrice de mise à l’échelle calculée.</span><span class="sxs-lookup"><span data-stu-id="6f101-120">This method left-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="6f101-121">La transformation concerne l’origine locale de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6f101-121">The transformation is about the local origin of the object.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="6f101-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f101-122">Requirements</span></span>



| <span data-ttu-id="6f101-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f101-123">Requirement</span></span> | <span data-ttu-id="6f101-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f101-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f101-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f101-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6f101-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f101-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6f101-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6f101-127">Library</span></span><br/> | <dl> <span data-ttu-id="6f101-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f101-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6f101-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f101-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f101-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="6f101-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="6f101-131">**ID3DXMATRIXStack :: Scale**</span><span class="sxs-lookup"><span data-stu-id="6f101-131">**ID3DXMATRIXStack::Scale**</span></span>](id3dxmatrixstack--scale.md)
</dt> </dl>

 

 
