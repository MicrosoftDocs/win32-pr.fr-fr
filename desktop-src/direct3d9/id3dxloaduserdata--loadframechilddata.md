---
description: Charger les données enfants d’un frame à partir d’un fichier. x.
ms.assetid: 79d251f3-c661-42e3-9385-84aabd58fd4f
title: 'ID3DXLoadUserData :: LoadFrameChildData, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 53bde98f0e756fd1baff4c509179f15e8489e74f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531059"
---
# <a name="id3dxloaduserdataloadframechilddata-method"></a><span data-ttu-id="cb018-103">ID3DXLoadUserData :: LoadFrameChildData, méthode</span><span class="sxs-lookup"><span data-stu-id="cb018-103">ID3DXLoadUserData::LoadFrameChildData method</span></span>

<span data-ttu-id="cb018-104">Charger les données enfants d’un frame à partir d’un fichier. x.</span><span class="sxs-lookup"><span data-stu-id="cb018-104">Load frame child data from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb018-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb018-105">Syntax</span></span>


```C++
HRESULT LoadFrameChildData(
  [in] LPD3DXFRAME    pFrame,
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a><span data-ttu-id="cb018-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb018-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb018-107">*pFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cb018-107">*pFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb018-108">Type : **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="cb018-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="cb018-109">Pointeur désignant un conteneur de maillage.</span><span class="sxs-lookup"><span data-stu-id="cb018-109">Pointer to a mesh container.</span></span> <span data-ttu-id="cb018-110">Consultez [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="cb018-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb018-111">*pXofChildData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cb018-111">*pXofChildData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb018-112">Type : **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="cb018-112">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="cb018-113">Pointeur vers une structure de données de fichier. x.</span><span class="sxs-lookup"><span data-stu-id="cb018-113">Pointer to a .x file data structure.</span></span> <span data-ttu-id="cb018-114">Cela est défini dans dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="cb018-114">This is defined in Dxfile.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb018-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb018-115">Return value</span></span>

<span data-ttu-id="cb018-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cb018-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cb018-117">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="cb018-117">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="cb018-118">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cb018-118">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="cb018-119">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de D3DERR ou D3DXERR, car cela entraînera l’échec de [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) également et retourne l’erreur.</span><span class="sxs-lookup"><span data-stu-id="cb018-119">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb018-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb018-120">Requirements</span></span>



| <span data-ttu-id="cb018-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb018-121">Requirement</span></span> | <span data-ttu-id="cb018-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb018-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb018-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb018-123">Header</span></span><br/>  | <dl> <span data-ttu-id="cb018-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb018-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="cb018-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cb018-125">Library</span></span><br/> | <dl> <span data-ttu-id="cb018-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb018-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cb018-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb018-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb018-128">ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="cb018-128">ID3DXLoadUserData</span></span>](id3dxloaduserdata.md)
</dt> </dl>

 

 




