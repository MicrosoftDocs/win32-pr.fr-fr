---
description: Ajoutez un objet de niveau supérieur après la hiérarchie de frames.
ms.assetid: 43b3cdb3-c6f0-4028-bf86-43d643fba73d
title: 'ID3DXSaveUserData :: AddTopLevelDataObjectsPost, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPost
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3573bae8cbcb6858b04207f936545b7cf93959c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043178"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspost-method"></a><span data-ttu-id="4a15b-103">ID3DXSaveUserData :: AddTopLevelDataObjectsPost, méthode</span><span class="sxs-lookup"><span data-stu-id="4a15b-103">ID3DXSaveUserData::AddTopLevelDataObjectsPost method</span></span>

<span data-ttu-id="4a15b-104">Ajoutez un objet de niveau supérieur après la hiérarchie de frames.</span><span class="sxs-lookup"><span data-stu-id="4a15b-104">Add a top level object after the frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a15b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a15b-105">Syntax</span></span>


```C++
HRESULT AddTopLevelDataObjectsPost(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a><span data-ttu-id="4a15b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a15b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a15b-107">*pXofSave* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a15b-107">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a15b-108">Type : **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="4a15b-108">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="4a15b-109">Pointeur vers un objet Save du fichier. x.</span><span class="sxs-lookup"><span data-stu-id="4a15b-109">Pointer to a .x file save object.</span></span> <span data-ttu-id="4a15b-110">Utilisez ce pointeur pour appeler [**IDirectXFileSaveObject :: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) pour créer l’objet de données à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="4a15b-110">Use this pointer to call [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) to create the data object to be saved.</span></span> <span data-ttu-id="4a15b-111">Appelez ensuite [**IDirectXFileSaveObject :: SaveData**](idirectxfilesaveobject--savedata.md) pour enregistrer les données.</span><span class="sxs-lookup"><span data-stu-id="4a15b-111">Then call [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) to save the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a15b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4a15b-112">Return value</span></span>

<span data-ttu-id="4a15b-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4a15b-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4a15b-114">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="4a15b-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="4a15b-115">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4a15b-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="4a15b-116">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md), car cela entraînera l’échec de [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) également et retourne l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4a15b-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a15b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a15b-117">Requirements</span></span>



| <span data-ttu-id="4a15b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a15b-118">Requirement</span></span> | <span data-ttu-id="4a15b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a15b-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a15b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a15b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="4a15b-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a15b-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4a15b-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4a15b-122">Library</span></span><br/> | <dl> <span data-ttu-id="4a15b-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a15b-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4a15b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a15b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a15b-125">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="4a15b-125">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
