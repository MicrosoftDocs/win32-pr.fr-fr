---
description: Charger les données de niveau supérieur à partir d’un fichier. x.
ms.assetid: 0270b923-d524-46c5-bd1a-44c782722635
title: 'ID3DXLoadUserData :: LoadTopLevelData, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadTopLevelData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f52d6853b12b666ab64602711a42c3698d6d8032
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532480"
---
# <a name="id3dxloaduserdataloadtopleveldata-method"></a><span data-ttu-id="a42f7-103">ID3DXLoadUserData :: LoadTopLevelData, méthode</span><span class="sxs-lookup"><span data-stu-id="a42f7-103">ID3DXLoadUserData::LoadTopLevelData method</span></span>

<span data-ttu-id="a42f7-104">Charger les données de niveau supérieur à partir d’un fichier. x.</span><span class="sxs-lookup"><span data-stu-id="a42f7-104">Load top level data from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a42f7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a42f7-105">Syntax</span></span>


```C++
HRESULT LoadTopLevelData(
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a><span data-ttu-id="a42f7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a42f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a42f7-107">*pXofChildData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a42f7-107">*pXofChildData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a42f7-108">Type : **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="a42f7-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="a42f7-109">Pointeur vers une structure de données de fichier. x.</span><span class="sxs-lookup"><span data-stu-id="a42f7-109">Pointer to a .x file data structure.</span></span> <span data-ttu-id="a42f7-110">Cela est défini dans dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="a42f7-110">This is defined in Dxfile.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a42f7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a42f7-111">Return value</span></span>

<span data-ttu-id="a42f7-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a42f7-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a42f7-113">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="a42f7-113">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="a42f7-114">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a42f7-114">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="a42f7-115">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de D3DERR ou D3DXERR, car cela entraînera l’échec de [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) également et retourne l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a42f7-115">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a42f7-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a42f7-116">Requirements</span></span>



| <span data-ttu-id="a42f7-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a42f7-117">Requirement</span></span> | <span data-ttu-id="a42f7-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a42f7-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a42f7-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="a42f7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a42f7-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a42f7-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a42f7-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a42f7-121">Library</span></span><br/> | <dl> <span data-ttu-id="a42f7-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a42f7-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a42f7-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a42f7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a42f7-124">ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="a42f7-124">ID3DXLoadUserData</span></span>](id3dxloaduserdata.md)
</dt> </dl>

 

 




