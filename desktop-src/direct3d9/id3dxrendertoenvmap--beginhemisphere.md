---
description: Lancer le rendu d’un mappage d’environnement hémisphérique.
ms.assetid: 1150aad9-dd8c-4943-afaf-90794faaaf70
title: 'ID3DXRenderToEnvMap :: BeginHemisphere, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginHemisphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 96eb4bbf4cfc6cac952368337456b946f64cf711
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211733"
---
# <a name="id3dxrendertoenvmapbeginhemisphere-method"></a><span data-ttu-id="64300-103">ID3DXRenderToEnvMap :: BeginHemisphere, méthode</span><span class="sxs-lookup"><span data-stu-id="64300-103">ID3DXRenderToEnvMap::BeginHemisphere method</span></span>

<span data-ttu-id="64300-104">Lancer le rendu d’un mappage d’environnement hémisphérique.</span><span class="sxs-lookup"><span data-stu-id="64300-104">Initiate the rendering of a hemispheric environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="64300-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64300-105">Syntax</span></span>


```C++
HRESULT BeginHemisphere(
  [in] LPDIRECT3DTEXTURE9 pTexZPos,
  [in] LPDIRECT3DTEXTURE9 pTexZNeg
);
```



## <a name="parameters"></a><span data-ttu-id="64300-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64300-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64300-107">*pTexZPos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64300-107">*pTexZPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64300-108">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="64300-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="64300-109">Pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) qui représente la surface de rendu de texture positive.</span><span class="sxs-lookup"><span data-stu-id="64300-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the positive texture render surface.</span></span>

</dd> <dt>

<span data-ttu-id="64300-110">*pTexZNeg* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64300-110">*pTexZNeg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64300-111">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="64300-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="64300-112">Pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) qui représente la surface de rendu de texture négative.</span><span class="sxs-lookup"><span data-stu-id="64300-112">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the negative texture render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64300-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64300-113">Return value</span></span>

<span data-ttu-id="64300-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64300-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64300-115">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="64300-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="64300-116">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL. E \_ échec</span><span class="sxs-lookup"><span data-stu-id="64300-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="64300-117">Notes</span><span class="sxs-lookup"><span data-stu-id="64300-117">Remarks</span></span>

<span data-ttu-id="64300-118">Consultez [**ID3DXRenderToEnvMap :: face**](id3dxrendertoenvmap--face.md) pour dessiner le visage.</span><span class="sxs-lookup"><span data-stu-id="64300-118">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the face.</span></span>

## <a name="requirements"></a><span data-ttu-id="64300-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64300-119">Requirements</span></span>



| <span data-ttu-id="64300-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64300-120">Requirement</span></span> | <span data-ttu-id="64300-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="64300-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64300-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="64300-122">Header</span></span><br/>  | <dl> <span data-ttu-id="64300-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="64300-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="64300-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="64300-124">Library</span></span><br/> | <dl> <span data-ttu-id="64300-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64300-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="64300-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64300-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64300-127">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="64300-127">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="64300-128">**ID3DXRenderToEnvMap :: fin**</span><span class="sxs-lookup"><span data-stu-id="64300-128">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
