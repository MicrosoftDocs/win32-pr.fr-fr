---
description: Dessine un sous-ensemble d’une maille.
ms.assetid: e785949e-fcda-4ef9-b50a-193cd954e97d
title: ID3DX10Mesh ::D méthode rawSubset (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 80beceebeead84a782cc7852ac0d2fe15ad61ff3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522962"
---
# <a name="id3dx10meshdrawsubset-method"></a><span data-ttu-id="0b0f8-103">ID3DX10Mesh ::D méthode rawSubset</span><span class="sxs-lookup"><span data-stu-id="0b0f8-103">ID3DX10Mesh::DrawSubset method</span></span>

<span data-ttu-id="0b0f8-104">Dessine un sous-ensemble d’une maille.</span><span class="sxs-lookup"><span data-stu-id="0b0f8-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b0f8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b0f8-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] UINT AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="0b0f8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b0f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b0f8-107">*AttribId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b0f8-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b0f8-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b0f8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b0f8-109">Spécifie le sous-ensemble du maillage à dessiner.</span><span class="sxs-lookup"><span data-stu-id="0b0f8-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="0b0f8-110">Cette valeur est utilisée pour différencier les visages d’un maillage comme appartenant à un ou plusieurs groupes d’attributs.</span><span class="sxs-lookup"><span data-stu-id="0b0f8-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b0f8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b0f8-111">Return value</span></span>

<span data-ttu-id="0b0f8-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0b0f8-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0b0f8-113">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0b0f8-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0b0f8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0b0f8-114">Remarks</span></span>

<span data-ttu-id="0b0f8-115">Une table d’attributs permet d’identifier les zones de la maille qui doivent être dessinées avec différentes textures, États de rendu, matériaux, etc.</span><span class="sxs-lookup"><span data-stu-id="0b0f8-115">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="0b0f8-116">En outre, l’application peut utiliser la table d’attributs pour masquer des parties d’un maillage en ne dessinant pas un identificateur d’attribut (AttribId) donné lors du dessin du frame.</span><span class="sxs-lookup"><span data-stu-id="0b0f8-116">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b0f8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b0f8-117">Requirements</span></span>



| <span data-ttu-id="0b0f8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b0f8-118">Requirement</span></span> | <span data-ttu-id="0b0f8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b0f8-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b0f8-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b0f8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0b0f8-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b0f8-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b0f8-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0b0f8-122">Library</span></span><br/> | <dl> <span data-ttu-id="0b0f8-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b0f8-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b0f8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b0f8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b0f8-125">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="0b0f8-125">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="0b0f8-126">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="0b0f8-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
