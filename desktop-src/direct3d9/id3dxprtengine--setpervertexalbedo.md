---
description: Définit une valeur Albedo pour chaque vertex de maillage, en remplaçant les valeurs Albedo précédentes.
ms.assetid: 5220dfe3-8d41-480c-a850-b9aad3d2bb2f
title: 'ID3DXPRTEngine :: SetPerVertexAlbedo, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da7a33a79cc50963e87d0eff15baf22ee8d79ce3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529620"
---
# <a name="id3dxprtenginesetpervertexalbedo-method"></a><span data-ttu-id="4febd-103">ID3DXPRTEngine :: SetPerVertexAlbedo, méthode</span><span class="sxs-lookup"><span data-stu-id="4febd-103">ID3DXPRTEngine::SetPerVertexAlbedo method</span></span>

<span data-ttu-id="4febd-104">Définit une valeur Albedo pour chaque vertex de maillage, en remplaçant les valeurs Albedo précédentes.</span><span class="sxs-lookup"><span data-stu-id="4febd-104">Sets an albedo value for each mesh vertex, overwriting previous albedo values.</span></span>

## <a name="syntax"></a><span data-ttu-id="4febd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4febd-105">Syntax</span></span>


```C++
HRESULT SetPerVertexAlbedo(
  [in] const VOID *pDataIn,
  [in]       UINT NumChannels,
  [in]       UINT Stride
);
```



## <a name="parameters"></a><span data-ttu-id="4febd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4febd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4febd-107">*pDataIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4febd-107">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4febd-108">Type : **const void \***</span><span class="sxs-lookup"><span data-stu-id="4febd-108">Type: **const VOID\***</span></span>

<span data-ttu-id="4febd-109">Pointeur vers les données FLOAT Albedo du premier échantillon.</span><span class="sxs-lookup"><span data-stu-id="4febd-109">Pointer to FLOAT albedo data of the first sample.</span></span>

</dd> <dt>

<span data-ttu-id="4febd-110">*NumChannels* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4febd-110">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4febd-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4febd-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4febd-112">Nombre de canaux de couleur à définir.</span><span class="sxs-lookup"><span data-stu-id="4febd-112">Number of color channels to set.</span></span> <span data-ttu-id="4febd-113">Définissez la valeur 1 pour spécifier les matières grises (R = G = B), ou 3 pour activer les effets de dépassement des couleurs.</span><span class="sxs-lookup"><span data-stu-id="4febd-113">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="4febd-114">*Stride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4febd-114">*Stride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4febd-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4febd-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4febd-116">STRIDE en octets requis pour accéder à la valeur albedo de l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="4febd-116">Stride in bytes needed to get to next sample's albedo value.</span></span> <span data-ttu-id="4febd-117">Voir [largeur et tangage (Direct3D 9)](width-vs--pitch.md).</span><span class="sxs-lookup"><span data-stu-id="4febd-117">See [Width vs. Pitch (Direct3D 9)](width-vs--pitch.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4febd-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4febd-118">Return value</span></span>

<span data-ttu-id="4febd-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4febd-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4febd-120">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4febd-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4febd-121">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4febd-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="4febd-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4febd-122">Requirements</span></span>



| <span data-ttu-id="4febd-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4febd-123">Requirement</span></span> | <span data-ttu-id="4febd-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="4febd-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4febd-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="4febd-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4febd-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4febd-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4febd-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4febd-127">Library</span></span><br/> | <dl> <span data-ttu-id="4febd-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4febd-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4febd-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4febd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4febd-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="4febd-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
