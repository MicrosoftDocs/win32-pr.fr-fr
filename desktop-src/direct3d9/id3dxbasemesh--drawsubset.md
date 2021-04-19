---
description: Dessine un sous-ensemble d’une maille.
ms.assetid: 99eaa185-b681-47f2-aed8-5ca1697ff73c
title: ID3DXBaseMesh ::D méthode rawSubset (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.DrawSubset
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0da6e9fc57e0fc5e7b4b263ba3d97185333881c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523820"
---
# <a name="id3dxbasemeshdrawsubset-method"></a><span data-ttu-id="e9bad-103">ID3DXBaseMesh ::D méthode rawSubset</span><span class="sxs-lookup"><span data-stu-id="e9bad-103">ID3DXBaseMesh::DrawSubset method</span></span>

<span data-ttu-id="e9bad-104">Dessine un sous-ensemble d’une maille.</span><span class="sxs-lookup"><span data-stu-id="e9bad-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9bad-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9bad-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] DWORD AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="e9bad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9bad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9bad-107">*AttribId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9bad-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9bad-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e9bad-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e9bad-109">Valeur DWORD qui spécifie le sous-ensemble du maillage à dessiner.</span><span class="sxs-lookup"><span data-stu-id="e9bad-109">DWORD that specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="e9bad-110">Cette valeur est utilisée pour différencier les visages d’un maillage comme appartenant à un ou plusieurs groupes d’attributs.</span><span class="sxs-lookup"><span data-stu-id="e9bad-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9bad-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9bad-111">Return value</span></span>

<span data-ttu-id="e9bad-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e9bad-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e9bad-113">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e9bad-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e9bad-114">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e9bad-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9bad-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e9bad-115">Remarks</span></span>

<span data-ttu-id="e9bad-116">Le sous-ensemble spécifié par AttribId sera restitué par la méthode [**IDirect3DDevice9 ::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) , à l’aide du \_ type primitif TRIANGLELIST D3DPT, de sorte qu’une mémoire tampon d’index doit être correctement initialisée.</span><span class="sxs-lookup"><span data-stu-id="e9bad-116">The subset that is specified by AttribId will be rendered by the [**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) method, using the D3DPT\_TRIANGLELIST primitive type, so an index buffer must be properly initialized.</span></span>

<span data-ttu-id="e9bad-117">Une table d’attributs permet d’identifier les zones de la maille qui doivent être dessinées avec différentes textures, États de rendu, matériaux, etc.</span><span class="sxs-lookup"><span data-stu-id="e9bad-117">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="e9bad-118">En outre, l’application peut utiliser la table d’attributs pour masquer des parties d’un maillage en ne dessinant pas un identificateur d’attribut (*AttribId*) donné lors du dessin du frame.</span><span class="sxs-lookup"><span data-stu-id="e9bad-118">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (*AttribId*) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9bad-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9bad-119">Requirements</span></span>



| <span data-ttu-id="e9bad-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9bad-120">Requirement</span></span> | <span data-ttu-id="e9bad-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9bad-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9bad-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9bad-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e9bad-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9bad-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e9bad-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e9bad-124">Library</span></span><br/> | <dl> <span data-ttu-id="e9bad-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9bad-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e9bad-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9bad-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9bad-127">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="e9bad-127">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
