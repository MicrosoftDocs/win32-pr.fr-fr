---
description: Ajoutez un objet de niveau supérieur avant la hiérarchie des frames.
ms.assetid: ab4bfc3e-58eb-4de6-b080-8b3392b801bf
title: 'ID3DXSaveUserData :: AddTopLevelDataObjectsPre, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPre
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0194c8c9c6806f96cbe75394e6650ca3e7dc74b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539476"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspre-method"></a><span data-ttu-id="7eb34-103">ID3DXSaveUserData :: AddTopLevelDataObjectsPre, méthode</span><span class="sxs-lookup"><span data-stu-id="7eb34-103">ID3DXSaveUserData::AddTopLevelDataObjectsPre method</span></span>

<span data-ttu-id="7eb34-104">Ajoutez un objet de niveau supérieur avant la hiérarchie des frames.</span><span class="sxs-lookup"><span data-stu-id="7eb34-104">Add a top level object before the frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eb34-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7eb34-105">Syntax</span></span>


```C++
HRESULT AddTopLevelDataObjectsPre(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a><span data-ttu-id="7eb34-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7eb34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7eb34-107">*pXofSave* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7eb34-107">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb34-108">Type : **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="7eb34-108">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="7eb34-109">Pointeur vers un objet Save du fichier. x.</span><span class="sxs-lookup"><span data-stu-id="7eb34-109">Pointer to a .x file save object.</span></span> <span data-ttu-id="7eb34-110">Utilisez ce pointeur pour appeler [**IDirectXFileSaveObject :: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) pour créer l’objet de données à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="7eb34-110">Use this pointer to call [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) to create the data object to be saved.</span></span> <span data-ttu-id="7eb34-111">Appelez ensuite [**IDirectXFileSaveObject :: SaveData**](idirectxfilesaveobject--savedata.md) pour enregistrer les données.</span><span class="sxs-lookup"><span data-stu-id="7eb34-111">Then call [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) to save the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7eb34-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7eb34-112">Return value</span></span>

<span data-ttu-id="7eb34-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7eb34-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7eb34-114">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="7eb34-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="7eb34-115">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7eb34-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="7eb34-116">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md), car cela entraînera l’échec de [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) également et retourne l’erreur.</span><span class="sxs-lookup"><span data-stu-id="7eb34-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7eb34-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7eb34-117">Requirements</span></span>



| <span data-ttu-id="7eb34-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7eb34-118">Requirement</span></span> | <span data-ttu-id="7eb34-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7eb34-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7eb34-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7eb34-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7eb34-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="7eb34-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="7eb34-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7eb34-122">Library</span></span><br/> | <dl> <span data-ttu-id="7eb34-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7eb34-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7eb34-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7eb34-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eb34-125">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="7eb34-125">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
