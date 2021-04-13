---
description: Définit les propriétés de matériau de maillage dans la scène 3D. Utilisez cette méthode pour spécifier les paramètres de diffusion de sous-surface.
ms.assetid: 830d73be-bba6-454d-8476-341d291a5b2e
title: 'ID3DXPRTEngine :: SetMeshMaterials, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMeshMaterials
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c90ae72cab5d7a20c2c65b940d28a9b57902d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323250"
---
# <a name="id3dxprtenginesetmeshmaterials-method"></a><span data-ttu-id="df9e5-104">ID3DXPRTEngine :: SetMeshMaterials, méthode</span><span class="sxs-lookup"><span data-stu-id="df9e5-104">ID3DXPRTEngine::SetMeshMaterials method</span></span>

<span data-ttu-id="df9e5-105">Définit les propriétés de matériau de maillage dans la scène 3D.</span><span class="sxs-lookup"><span data-stu-id="df9e5-105">Sets mesh material properties in the 3D scene.</span></span> <span data-ttu-id="df9e5-106">Utilisez cette méthode pour spécifier les paramètres de diffusion de sous-surface.</span><span class="sxs-lookup"><span data-stu-id="df9e5-106">Use this method to specify subsurface scattering parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="df9e5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df9e5-107">Syntax</span></span>


```C++
HRESULT SetMeshMaterials(
  [in] const D3DXSHMATERIAL **ppMaterials,
  [in]       UINT           NumMeshes,
  [in]       UINT           NumChannels,
  [in]       BOOL           bSetAlbedo,
  [in]       FLOAT          fLengthScale
);
```



## <a name="parameters"></a><span data-ttu-id="df9e5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df9e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df9e5-109">*ppMaterials* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df9e5-109">*ppMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df9e5-110">Type : **const [**D3DXSHMATERIAL**](d3dxshmaterial.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="df9e5-110">Type: **const [**D3DXSHMATERIAL**](d3dxshmaterial.md)\*\***</span></span>

<span data-ttu-id="df9e5-111">Adresse d’un pointeur vers les propriétés du matériau de maillage souhaité.</span><span class="sxs-lookup"><span data-stu-id="df9e5-111">Address of a pointer to desired mesh material properties.</span></span> <span data-ttu-id="df9e5-112">Consultez [**D3DXSHMATERIAL**](d3dxshmaterial.md).</span><span class="sxs-lookup"><span data-stu-id="df9e5-112">See [**D3DXSHMATERIAL**](d3dxshmaterial.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9e5-113">*NumMeshes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df9e5-113">*NumMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df9e5-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df9e5-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df9e5-115">Index du maillage sur lequel définir les propriétés du matériau.</span><span class="sxs-lookup"><span data-stu-id="df9e5-115">Index of the mesh on which to set material properties.</span></span>

</dd> <dt>

<span data-ttu-id="df9e5-116">*NumChannels* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df9e5-116">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df9e5-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df9e5-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df9e5-118">Nombre de canaux de couleur à définir dans le maillage.</span><span class="sxs-lookup"><span data-stu-id="df9e5-118">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="df9e5-119">Définissez la valeur 1 pour spécifier les matières grises (R = G = B), ou 3 pour activer les effets de dépassement des couleurs.</span><span class="sxs-lookup"><span data-stu-id="df9e5-119">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span> <span data-ttu-id="df9e5-120">Si vous envisagez de modifier ce paramètre, commencez par définir le Albedo à l’aide d’une autre méthode telle que [**ID3DXPRTEngine :: SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) ou [**ID3DXPRTEngine :: SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md).</span><span class="sxs-lookup"><span data-stu-id="df9e5-120">If you intend to change this parameter, first set the albedo using another method such as [**ID3DXPRTEngine::SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) or [**ID3DXPRTEngine::SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9e5-121">*bSetAlbedo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df9e5-121">*bSetAlbedo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df9e5-122">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df9e5-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df9e5-123">Si la **valeur est true**, définit le Albedo du maillage sur ppMaterials, en remplaçant toutes les valeurs de Texel et de vertex Albedo existantes.</span><span class="sxs-lookup"><span data-stu-id="df9e5-123">If **TRUE**, sets the albedo of the mesh to ppMaterials, overwriting all existing texel and vertex albedo values.</span></span> <span data-ttu-id="df9e5-124">Si la **valeur est false**, conserve toutes les valeurs de Texel et vertex Albedo existantes définies par d’autres méthodes. NumChannels doit correspondre au paramètre NumChannels utilisé pour créer la mémoire tampon dans [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) ou [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md).</span><span class="sxs-lookup"><span data-stu-id="df9e5-124">If **FALSE**, preserves all existing texel and vertex albedo values set by other methods; NumChannels must match the NumChannels parameter used to create the buffer in [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) or [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9e5-125">*fLengthScale* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df9e5-125">*fLengthScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df9e5-126">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df9e5-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df9e5-127">Échelle de la scène 3D par rapport à un cube de 1 mm.</span><span class="sxs-lookup"><span data-stu-id="df9e5-127">Scale of the 3D scene relative to a 1-mm cube.</span></span> <span data-ttu-id="df9e5-128">Utilisé pour les calculs de diffusion de sous-surface.</span><span class="sxs-lookup"><span data-stu-id="df9e5-128">Used for subsurface scattering computations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df9e5-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="df9e5-129">Return value</span></span>

<span data-ttu-id="df9e5-130">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="df9e5-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="df9e5-131">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="df9e5-131">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="df9e5-132">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="df9e5-132">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="df9e5-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df9e5-133">Requirements</span></span>



| <span data-ttu-id="df9e5-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df9e5-134">Requirement</span></span> | <span data-ttu-id="df9e5-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="df9e5-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df9e5-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="df9e5-136">Header</span></span><br/>  | <dl> <span data-ttu-id="df9e5-137"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="df9e5-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="df9e5-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="df9e5-138">Library</span></span><br/> | <dl> <span data-ttu-id="df9e5-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df9e5-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="df9e5-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df9e5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df9e5-141">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="df9e5-141">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
