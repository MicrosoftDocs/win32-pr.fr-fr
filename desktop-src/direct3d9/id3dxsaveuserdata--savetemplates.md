---
description: Rappel permettant à l’utilisateur d’enregistrer un modèle de fichier. x.
ms.assetid: c2e29495-5eeb-42b8-826e-1a60c1c6bda2
title: 'ID3DXSaveUserData :: SaveTemplates, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.SaveTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 92040629b1b21cbfa1219eee237e357aa056b473
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953998"
---
# <a name="id3dxsaveuserdatasavetemplates-method"></a><span data-ttu-id="5127c-103">ID3DXSaveUserData :: SaveTemplates, méthode</span><span class="sxs-lookup"><span data-stu-id="5127c-103">ID3DXSaveUserData::SaveTemplates method</span></span>

<span data-ttu-id="5127c-104">Rappel permettant à l’utilisateur d’enregistrer un modèle de fichier. x.</span><span class="sxs-lookup"><span data-stu-id="5127c-104">A callback for the user to save a .x file template.</span></span>

## <a name="syntax"></a><span data-ttu-id="5127c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5127c-105">Syntax</span></span>


```C++
HRESULT SaveTemplates(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a><span data-ttu-id="5127c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5127c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5127c-107">*pXofSave* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5127c-107">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5127c-108">Type : **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="5127c-108">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="5127c-109">Pointeur vers un objet Save du fichier. x.</span><span class="sxs-lookup"><span data-stu-id="5127c-109">Pointer to a .x file save object.</span></span> <span data-ttu-id="5127c-110">N’utilisez pas ce paramètre pour ajouter des objets de données.</span><span class="sxs-lookup"><span data-stu-id="5127c-110">Do not use this parameter to add data objects.</span></span> <span data-ttu-id="5127c-111">Consultez [**ID3DXFileSaveObject**](id3dxfilesaveobject.md).</span><span class="sxs-lookup"><span data-stu-id="5127c-111">See [**ID3DXFileSaveObject**](id3dxfilesaveobject.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5127c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5127c-112">Return value</span></span>

<span data-ttu-id="5127c-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5127c-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5127c-114">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="5127c-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="5127c-115">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5127c-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="5127c-116">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md), car cela entraînera l’échec de [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) également et retourne l’erreur.</span><span class="sxs-lookup"><span data-stu-id="5127c-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="5127c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="5127c-117">Remarks</span></span>

<span data-ttu-id="5127c-118">[**ID3DXSaveUserData :: RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) et **ID3DXSaveUserData :: SaveTemplates** fournissent un mécanisme d’ajout d’un modèle à un fichier. x pour l’enregistrement des données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5127c-118">[**ID3DXSaveUserData::RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) and **ID3DXSaveUserData::SaveTemplates** provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="5127c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5127c-119">Requirements</span></span>



| <span data-ttu-id="5127c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5127c-120">Requirement</span></span> | <span data-ttu-id="5127c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5127c-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5127c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5127c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5127c-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="5127c-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5127c-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5127c-124">Library</span></span><br/> | <dl> <span data-ttu-id="5127c-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5127c-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5127c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5127c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5127c-127">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="5127c-127">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
