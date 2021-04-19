---
description: Dessine une bande en courbes dans l’espace à l’écran. L’entrée se présente sous la forme d’un tableau qui définit les points (of D3DXVECTOR2) sur la bande.
ms.assetid: 10ad5af5-fb57-46ef-a89f-7a05dcf58826
title: ID3DXLine ::D méthode brute (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0a7492fb2128e0d9ec402d5211c20d5569ceb506
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531366"
---
# <a name="id3dxlinedraw-method"></a><span data-ttu-id="52da8-104">ID3DXLine ::D méthode brute</span><span class="sxs-lookup"><span data-stu-id="52da8-104">ID3DXLine::Draw method</span></span>

<span data-ttu-id="52da8-105">Dessine une bande en courbes dans l’espace à l’écran.</span><span class="sxs-lookup"><span data-stu-id="52da8-105">Draws a line strip in screen space.</span></span> <span data-ttu-id="52da8-106">L’entrée se présente sous la forme d’un tableau qui définit les points (of [**D3DXVECTOR2**](d3dxvector2.md)) sur la bande.</span><span class="sxs-lookup"><span data-stu-id="52da8-106">Input is in the form of an array that defines points (of [**D3DXVECTOR2**](d3dxvector2.md)) on the line strip.</span></span>

## <a name="syntax"></a><span data-ttu-id="52da8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52da8-107">Syntax</span></span>


```C++
HRESULT Draw(
  [in] const D3DXVECTOR2 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a><span data-ttu-id="52da8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52da8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52da8-109">*pVertexList* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52da8-109">*pVertexList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52da8-110">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="52da8-110">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="52da8-111">Tableau des vertex qui composent la ligne.</span><span class="sxs-lookup"><span data-stu-id="52da8-111">Array of vertices that make up the line.</span></span> <span data-ttu-id="52da8-112">Consultez [**D3DXVECTOR2**](d3dxvector2.md).</span><span class="sxs-lookup"><span data-stu-id="52da8-112">See [**D3DXVECTOR2**](d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="52da8-113">*dwVertexListCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52da8-113">*dwVertexListCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52da8-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52da8-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52da8-115">Nombre de vertex dans la liste de vertex.</span><span class="sxs-lookup"><span data-stu-id="52da8-115">Number of vertices in the vertex list.</span></span>

</dd> <dt>

<span data-ttu-id="52da8-116">*Couleur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52da8-116">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52da8-117">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="52da8-117">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="52da8-118">Couleur de la ligne.</span><span class="sxs-lookup"><span data-stu-id="52da8-118">Color of the line.</span></span> <span data-ttu-id="52da8-119">Consultez [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="52da8-119">See [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52da8-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="52da8-120">Return value</span></span>

<span data-ttu-id="52da8-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="52da8-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="52da8-122">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="52da8-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="52da8-123">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="52da8-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="52da8-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52da8-124">Requirements</span></span>



| <span data-ttu-id="52da8-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52da8-125">Requirement</span></span> | <span data-ttu-id="52da8-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="52da8-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52da8-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="52da8-127">Header</span></span><br/>  | <dl> <span data-ttu-id="52da8-128"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="52da8-128"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="52da8-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="52da8-129">Library</span></span><br/> | <dl> <span data-ttu-id="52da8-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52da8-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="52da8-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52da8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52da8-132">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="52da8-132">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
