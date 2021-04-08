---
description: Obtient le nombre maximal d’influences pour un vertex de la maille.
ms.assetid: 012168e8-30e5-4571-b793-647ab23df068
title: 'ID3DXSkinInfo :: GetMaxVertexInfluences, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxVertexInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2acae5cc119df25989e6bf22692ec1609ffa9408
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953792"
---
# <a name="id3dxskininfogetmaxvertexinfluences-method"></a><span data-ttu-id="fab92-103">ID3DXSkinInfo :: GetMaxVertexInfluences, méthode</span><span class="sxs-lookup"><span data-stu-id="fab92-103">ID3DXSkinInfo::GetMaxVertexInfluences method</span></span>

<span data-ttu-id="fab92-104">Obtient le nombre maximal d’influences pour un vertex de la maille.</span><span class="sxs-lookup"><span data-stu-id="fab92-104">Gets the maximum number of influences for any vertex in the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="fab92-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fab92-105">Syntax</span></span>


```C++
HRESULT GetMaxVertexInfluences(
  [in] DWORD *maxVertexInfluences
);
```



## <a name="parameters"></a><span data-ttu-id="fab92-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fab92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fab92-107">*maxVertexInfluences* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fab92-107">*maxVertexInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fab92-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fab92-108">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fab92-109">Pointeur vers l’influence de vertex maximale.</span><span class="sxs-lookup"><span data-stu-id="fab92-109">Pointer to the maximum vertex influence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fab92-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fab92-110">Return value</span></span>

<span data-ttu-id="fab92-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fab92-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fab92-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fab92-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fab92-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fab92-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fab92-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fab92-114">Requirements</span></span>



| <span data-ttu-id="fab92-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fab92-115">Requirement</span></span> | <span data-ttu-id="fab92-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="fab92-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fab92-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="fab92-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fab92-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fab92-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fab92-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fab92-119">Library</span></span><br/> | <dl> <span data-ttu-id="fab92-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fab92-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fab92-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fab92-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fab92-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="fab92-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
