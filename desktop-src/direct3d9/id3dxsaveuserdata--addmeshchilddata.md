---
description: Ajoutez des données enfants à la maille.
ms.assetid: cf3e2015-c4b0-4d98-8346-c74fbdd37310
title: 'ID3DXSaveUserData :: AddMeshChildData, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8a9d6b69e64e0e1eca5d4350125e0955254b6127
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211933"
---
# <a name="id3dxsaveuserdataaddmeshchilddata-method"></a><span data-ttu-id="773d2-103">ID3DXSaveUserData :: AddMeshChildData, méthode</span><span class="sxs-lookup"><span data-stu-id="773d2-103">ID3DXSaveUserData::AddMeshChildData method</span></span>

<span data-ttu-id="773d2-104">Ajoutez des données enfants à la maille.</span><span class="sxs-lookup"><span data-stu-id="773d2-104">Add child data to the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="773d2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="773d2-105">Syntax</span></span>


```C++
HRESULT AddMeshChildData(
  [in] const D3DXMESHCONTAINER    *pMeshContainer,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofMeshData
);
```



## <a name="parameters"></a><span data-ttu-id="773d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="773d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="773d2-107">*pMeshContainer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="773d2-107">*pMeshContainer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="773d2-108">Type : **const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md) \***</span><span class="sxs-lookup"><span data-stu-id="773d2-108">Type: **const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span></span>

<span data-ttu-id="773d2-109">Pointeur désignant un conteneur de maillage.</span><span class="sxs-lookup"><span data-stu-id="773d2-109">Pointer to a mesh container.</span></span> <span data-ttu-id="773d2-110">Consultez [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span><span class="sxs-lookup"><span data-stu-id="773d2-110">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> <dt>

<span data-ttu-id="773d2-111">*pXofSave* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="773d2-111">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="773d2-112">Type : **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="773d2-112">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="773d2-113">Pointeur vers un objet Save du fichier. x.</span><span class="sxs-lookup"><span data-stu-id="773d2-113">Pointer to a .x file save object.</span></span> <span data-ttu-id="773d2-114">Utilisez le pointeur pour appeler [**ID3DXFileSaveObject :: AddDataObject**](id3dxfilesaveobject--adddataobject.md) pour ajouter un objet de données enfant.</span><span class="sxs-lookup"><span data-stu-id="773d2-114">Use the pointer to call [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md) to add a child data object.</span></span> <span data-ttu-id="773d2-115">N’enregistrez pas les données avec [**ID3DXFileSaveObject :: Save**](id3dxfilesaveobject--save.md).</span><span class="sxs-lookup"><span data-stu-id="773d2-115">Do not save the data with [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md).</span></span>

</dd> <dt>

<span data-ttu-id="773d2-116">*pXofMeshData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="773d2-116">*pXofMeshData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="773d2-117">Type : **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span><span class="sxs-lookup"><span data-stu-id="773d2-117">Type: **[**LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span></span>

<span data-ttu-id="773d2-118">Pointeur vers un nœud de données de fichier. x.</span><span class="sxs-lookup"><span data-stu-id="773d2-118">Pointer to a .x file data node.</span></span> <span data-ttu-id="773d2-119">Utilisez le pointeur pour appeler [**ID3DXFileSaveData :: AddDataObject**](id3dxfilesavedata--adddataobject.md) pour ajouter un objet de données enfant.</span><span class="sxs-lookup"><span data-stu-id="773d2-119">Use the pointer to call [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) to add a child data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="773d2-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="773d2-120">Return value</span></span>

<span data-ttu-id="773d2-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="773d2-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="773d2-122">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="773d2-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="773d2-123">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="773d2-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="773d2-124">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md), car cela entraînera l’échec de [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) également et retourne l’erreur.</span><span class="sxs-lookup"><span data-stu-id="773d2-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="773d2-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="773d2-125">Requirements</span></span>



| <span data-ttu-id="773d2-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="773d2-126">Requirement</span></span> | <span data-ttu-id="773d2-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="773d2-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="773d2-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="773d2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="773d2-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="773d2-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="773d2-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="773d2-130">Library</span></span><br/> | <dl> <span data-ttu-id="773d2-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="773d2-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="773d2-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="773d2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="773d2-133">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="773d2-133">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
