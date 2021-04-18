---
description: Charger les données enfants de maillage à partir d’un fichier. x.
ms.assetid: 5ed338f9-48a6-44e6-95da-1bed9ecd6ebf
title: 'ID3DXLoadUserData :: LoadMeshChildData, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9960f47ac21dad2521f6272c9176e3d895bbd109
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522578"
---
# <a name="id3dxloaduserdataloadmeshchilddata-method"></a><span data-ttu-id="58bd3-103">ID3DXLoadUserData :: LoadMeshChildData, méthode</span><span class="sxs-lookup"><span data-stu-id="58bd3-103">ID3DXLoadUserData::LoadMeshChildData method</span></span>

<span data-ttu-id="58bd3-104">Charger les données enfants de maillage à partir d’un fichier. x.</span><span class="sxs-lookup"><span data-stu-id="58bd3-104">Load mesh child data from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="58bd3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58bd3-105">Syntax</span></span>


```C++
HRESULT LoadMeshChildData(
  [in] LPD3DXMESHCONTAINER pMeshContainer,
  [in] LPD3DXFILEDATA      pXofChildData
);
```



## <a name="parameters"></a><span data-ttu-id="58bd3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58bd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58bd3-107">*pMeshContainer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58bd3-107">*pMeshContainer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58bd3-108">Type : **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="58bd3-108">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

<span data-ttu-id="58bd3-109">Pointeur désignant un conteneur de maillage.</span><span class="sxs-lookup"><span data-stu-id="58bd3-109">Pointer to a mesh container.</span></span> <span data-ttu-id="58bd3-110">Consultez [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span><span class="sxs-lookup"><span data-stu-id="58bd3-110">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> <dt>

<span data-ttu-id="58bd3-111">*pXofChildData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58bd3-111">*pXofChildData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58bd3-112">Type : **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="58bd3-112">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="58bd3-113">Pointeur vers une structure de données de fichier. x.</span><span class="sxs-lookup"><span data-stu-id="58bd3-113">Pointer to a .x file data structure.</span></span> <span data-ttu-id="58bd3-114">Cela est défini dans dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="58bd3-114">This is defined in Dxfile.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58bd3-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="58bd3-115">Return value</span></span>

<span data-ttu-id="58bd3-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="58bd3-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="58bd3-117">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="58bd3-117">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="58bd3-118">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="58bd3-118">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="58bd3-119">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de D3DERR ou D3DXERR, car cela entraînera l’échec de [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) également et retourne l’erreur.</span><span class="sxs-lookup"><span data-stu-id="58bd3-119">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="58bd3-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58bd3-120">Requirements</span></span>



| <span data-ttu-id="58bd3-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58bd3-121">Requirement</span></span> | <span data-ttu-id="58bd3-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="58bd3-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58bd3-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="58bd3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="58bd3-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="58bd3-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="58bd3-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="58bd3-125">Library</span></span><br/> | <dl> <span data-ttu-id="58bd3-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58bd3-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="58bd3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58bd3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58bd3-128">ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="58bd3-128">ID3DXLoadUserData</span></span>](id3dxloaduserdata.md)
</dt> </dl>

 

 




