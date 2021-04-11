---
description: Ajoutez des données enfants au frame.
ms.assetid: b1e02b2a-628f-49c3-a81c-0e96ba0d5f4a
title: 'ID3DXSaveUserData :: AddFrameChildData, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e3017ec2dafa9d4188da4f50d14257a09ffe72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211934"
---
# <a name="id3dxsaveuserdataaddframechilddata-method"></a><span data-ttu-id="49b19-103">ID3DXSaveUserData :: AddFrameChildData, méthode</span><span class="sxs-lookup"><span data-stu-id="49b19-103">ID3DXSaveUserData::AddFrameChildData method</span></span>

<span data-ttu-id="49b19-104">Ajoutez des données enfants au frame.</span><span class="sxs-lookup"><span data-stu-id="49b19-104">Add child data to the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="49b19-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49b19-105">Syntax</span></span>


```C++
HRESULT AddFrameChildData(
  [in] const D3DXFRAME            *pFrame,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="49b19-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49b19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49b19-107">*pFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49b19-107">*pFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49b19-108">Type : **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="49b19-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="49b19-109">Pointeur désignant un conteneur de maillage.</span><span class="sxs-lookup"><span data-stu-id="49b19-109">Pointer to a mesh container.</span></span> <span data-ttu-id="49b19-110">Consultez [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="49b19-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="49b19-111">*pXofSave* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49b19-111">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49b19-112">Type : **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="49b19-112">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="49b19-113">Pointeur vers un objet Save du fichier. x.</span><span class="sxs-lookup"><span data-stu-id="49b19-113">Pointer to a .x file save object.</span></span> <span data-ttu-id="49b19-114">Utilisez le pointeur pour appeler [**ID3DXFileSaveObject :: AddDataObject**](id3dxfilesaveobject--adddataobject.md) pour ajouter un objet de données enfant.</span><span class="sxs-lookup"><span data-stu-id="49b19-114">Use the pointer to call [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md) to add a child data object.</span></span> <span data-ttu-id="49b19-115">N’enregistrez pas les données avec [**ID3DXFileSaveObject :: Save**](id3dxfilesaveobject--save.md).</span><span class="sxs-lookup"><span data-stu-id="49b19-115">Do not save the data with [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md).</span></span>

</dd> <dt>

<span data-ttu-id="49b19-116">*pXofFrameData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49b19-116">*pXofFrameData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49b19-117">Type : **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span><span class="sxs-lookup"><span data-stu-id="49b19-117">Type: **[**LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span></span>

<span data-ttu-id="49b19-118">Pointeur vers un nœud de données de fichier. x.</span><span class="sxs-lookup"><span data-stu-id="49b19-118">Pointer to a .x file data node.</span></span> <span data-ttu-id="49b19-119">Utilisez le pointeur pour appeler [**ID3DXFileSaveData :: AddDataObject**](id3dxfilesavedata--adddataobject.md) pour ajouter un objet de données enfant.</span><span class="sxs-lookup"><span data-stu-id="49b19-119">Use the pointer to call [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) to add a child data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49b19-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49b19-120">Return value</span></span>

<span data-ttu-id="49b19-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="49b19-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="49b19-122">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="49b19-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="49b19-123">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="49b19-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="49b19-124">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md), car cela entraînera l’échec de [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) également et retourne l’erreur.</span><span class="sxs-lookup"><span data-stu-id="49b19-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="49b19-125">Notes</span><span class="sxs-lookup"><span data-stu-id="49b19-125">Remarks</span></span>

<span data-ttu-id="49b19-126">[**ID3DXSaveUserData :: RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) et [**ID3DXSaveUserData :: SaveTemplates**](id3dxsaveuserdata--savetemplates.md) fournissent un mécanisme d’ajout d’un modèle à un fichier. x pour l’enregistrement des données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="49b19-126">[**ID3DXSaveUserData::RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) and [**ID3DXSaveUserData::SaveTemplates**](id3dxsaveuserdata--savetemplates.md) provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="49b19-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49b19-127">Requirements</span></span>



| <span data-ttu-id="49b19-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49b19-128">Requirement</span></span> | <span data-ttu-id="49b19-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="49b19-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49b19-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="49b19-130">Header</span></span><br/>  | <dl> <span data-ttu-id="49b19-131"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="49b19-131"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="49b19-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="49b19-132">Library</span></span><br/> | <dl> <span data-ttu-id="49b19-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49b19-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="49b19-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49b19-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49b19-135">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="49b19-135">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
