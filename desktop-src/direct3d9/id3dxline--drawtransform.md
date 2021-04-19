---
description: Dessine une bande de courbes dans l’espace à l’écran avec une matrice de transformation d’entrée spécifiée.
ms.assetid: 869dc705-8162-4cd9-ac6a-c0ce32f430c3
title: ID3DXLine ::D méthode rawTransform (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.DrawTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 52407a8c92e626f8fe4d2df817017f81806cbae9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522764"
---
# <a name="id3dxlinedrawtransform-method"></a><span data-ttu-id="3c2c0-103">ID3DXLine ::D méthode rawTransform</span><span class="sxs-lookup"><span data-stu-id="3c2c0-103">ID3DXLine::DrawTransform method</span></span>

<span data-ttu-id="3c2c0-104">Dessine une bande de courbes dans l’espace à l’écran avec une matrice de transformation d’entrée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-104">Draws a line strip in screen space with a specified input transformation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c2c0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c2c0-105">Syntax</span></span>


```C++
HRESULT DrawTransform(
  [in] const D3DXVECTOR3 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in] const D3DXMATRIX  *pTransform,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a><span data-ttu-id="3c2c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c2c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c2c0-107">*pVertexList* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c2c0-107">*pVertexList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2c0-108">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3c2c0-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3c2c0-109">Tableau des vertex qui composent la ligne.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-109">Array of vertices that make up the line.</span></span> <span data-ttu-id="3c2c0-110">Consultez [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="3c2c0-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c2c0-111">*dwVertexListCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c2c0-111">*dwVertexListCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2c0-112">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c2c0-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c2c0-113">Nombre de vertex dans la liste de vertex.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-113">Number of vertices in the vertex list.</span></span>

</dd> <dt>

<span data-ttu-id="3c2c0-114">*pTransform* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c2c0-114">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2c0-115">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="3c2c0-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3c2c0-116">Matrice de mise à l’échelle, de rotation et de translation (SRT) pour la transformation des points.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-116">A scale, rotate, and translate (SRT) matrix for transforming the points.</span></span> <span data-ttu-id="3c2c0-117">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="3c2c0-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span> <span data-ttu-id="3c2c0-118">Si cette matrice est une matrice de projection, toutes les lignes stippled sont dessinées avec un modèle de stippling de perspective.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-118">If this matrix is a projection matrix, any stippled lines will be drawn with a perspective-correct stippling pattern.</span></span> <span data-ttu-id="3c2c0-119">Ou bien, vous pouvez transformer les vertex et utiliser [**ID3DXLine ::D RAW**](id3dxline--draw.md) pour dessiner la ligne avec un modèle de stipple de type non-perspective-correct.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-119">Or, you can transform the vertices and use [**ID3DXLine::Draw**](id3dxline--draw.md) to draw the line with a nonperspective-correct stipple pattern.</span></span>

</dd> <dt>

<span data-ttu-id="3c2c0-120">*Couleur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c2c0-120">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2c0-121">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="3c2c0-121">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="3c2c0-122">Couleur de la ligne.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-122">Color of the line.</span></span> <span data-ttu-id="3c2c0-123">Consultez [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="3c2c0-123">See [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c2c0-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c2c0-124">Return value</span></span>

<span data-ttu-id="3c2c0-125">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c2c0-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c2c0-126">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-126">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3c2c0-127">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-127">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c2c0-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c2c0-128">Requirements</span></span>



| <span data-ttu-id="3c2c0-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c2c0-129">Requirement</span></span> | <span data-ttu-id="3c2c0-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c2c0-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2c0-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c2c0-131">Header</span></span><br/>  | <dl> <span data-ttu-id="3c2c0-132"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c2c0-132"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="3c2c0-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3c2c0-133">Library</span></span><br/> | <dl> <span data-ttu-id="3c2c0-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c2c0-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3c2c0-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c2c0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c2c0-136">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="3c2c0-136">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
