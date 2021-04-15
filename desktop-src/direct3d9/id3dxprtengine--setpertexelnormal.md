---
description: Définit un vecteur normal pour chaque Texel dans un objet texture. Cette méthode est utilisée pour stocker des vecteurs normaux de vertex à partir d’une maille (ou des normales de vertex interpolées si le transfert de luminance précalculé basé sur les pixels (PRT) est calculé).
ms.assetid: 165a3ef6-c142-4988-b4fb-5aafd8ff11fe
title: 'ID3DXPRTEngine :: SetPerTexelNormal, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelNormal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5220ad500312792cd158967e9502381f49b0e3e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394164"
---
# <a name="id3dxprtenginesetpertexelnormal-method"></a><span data-ttu-id="bf26e-104">ID3DXPRTEngine :: SetPerTexelNormal, méthode</span><span class="sxs-lookup"><span data-stu-id="bf26e-104">ID3DXPRTEngine::SetPerTexelNormal method</span></span>

<span data-ttu-id="bf26e-105">Définit un vecteur normal pour chaque Texel dans un objet texture.</span><span class="sxs-lookup"><span data-stu-id="bf26e-105">Sets a normal vector for each texel in a texture object.</span></span> <span data-ttu-id="bf26e-106">Cette méthode est utilisée pour stocker des vecteurs normaux de vertex à partir d’une maille (ou des normales de vertex interpolées si le transfert de luminance précalculé basé sur les pixels (PRT) est calculé).</span><span class="sxs-lookup"><span data-stu-id="bf26e-106">This method is used to store vertex normal vectors from a mesh (or interpolated vertex normals if pixel-based precomputed radiance transfer (PRT) is being computed).</span></span>

## <a name="syntax"></a><span data-ttu-id="bf26e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf26e-107">Syntax</span></span>


```C++
HRESULT SetPerTexelNormal(
  [in] LPDIRECT3DTEXTURE9 pNormalTexture
);
```



## <a name="parameters"></a><span data-ttu-id="bf26e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf26e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf26e-109">*pNormalTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf26e-109">*pNormalTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf26e-110">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="bf26e-110">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="bf26e-111">Pointeur vers un objet de texture [**IDirect3DTexture9**](/windows/desktop/api) qui sert de carte d’espace d’objet normale dans laquelle stocker les vecteurs normaux.</span><span class="sxs-lookup"><span data-stu-id="bf26e-111">Pointer to an [**IDirect3DTexture9**](/windows/desktop/api) texture object that serves as an object space normal map in which to store normal vectors.</span></span> <span data-ttu-id="bf26e-112">La texture doit avoir les mêmes dimensions que [**ID3DXPRTBuffer**](id3dxprtbuffer.md) et doit être en mesure de stocker des formats de texture signés.</span><span class="sxs-lookup"><span data-stu-id="bf26e-112">The texture must have the same dimensions as [**ID3DXPRTBuffer**](id3dxprtbuffer.md) and must be able to store signed texture formats.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf26e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf26e-113">Return value</span></span>

<span data-ttu-id="bf26e-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bf26e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bf26e-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bf26e-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bf26e-116">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bf26e-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf26e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf26e-117">Requirements</span></span>



| <span data-ttu-id="bf26e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf26e-118">Requirement</span></span> | <span data-ttu-id="bf26e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf26e-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf26e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf26e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bf26e-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf26e-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bf26e-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bf26e-122">Library</span></span><br/> | <dl> <span data-ttu-id="bf26e-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf26e-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bf26e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf26e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf26e-125">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="bf26e-125">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
