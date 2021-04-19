---
description: Rappel permettant à l’utilisateur d’inscrire un modèle de fichier. x.
ms.assetid: 60568556-704c-4be3-bbde-04887583cf70
title: 'ID3DXSaveUserData :: RegisterTemplates, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.RegisterTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1465b76b758f6a5ed9e7dff4c7126935fb7c5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539919"
---
# <a name="id3dxsaveuserdataregistertemplates-method"></a><span data-ttu-id="b641d-103">ID3DXSaveUserData :: RegisterTemplates, méthode</span><span class="sxs-lookup"><span data-stu-id="b641d-103">ID3DXSaveUserData::RegisterTemplates method</span></span>

<span data-ttu-id="b641d-104">Rappel permettant à l’utilisateur d’inscrire un modèle de fichier. x.</span><span class="sxs-lookup"><span data-stu-id="b641d-104">A callback for the user to register a .x file template.</span></span>

## <a name="syntax"></a><span data-ttu-id="b641d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b641d-105">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPD3DXFILE pXFileApi
);
```



## <a name="parameters"></a><span data-ttu-id="b641d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b641d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b641d-107">*pXFileApi* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b641d-107">*pXFileApi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b641d-108">Type : **[ **LPD3DXFILE**](id3dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="b641d-108">Type: **[**LPD3DXFILE**](id3dxfile.md)**</span></span>

<span data-ttu-id="b641d-109">Utilisez ce pointeur pour inscrire des modèles de fichier. x définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b641d-109">Use this pointer to register user-defined .x file templates.</span></span> <span data-ttu-id="b641d-110">Consultez [**ID3DXFile**](id3dxfile.md).</span><span class="sxs-lookup"><span data-stu-id="b641d-110">See [**ID3DXFile**](id3dxfile.md).</span></span> <span data-ttu-id="b641d-111">N’utilisez pas ce paramètre pour ajouter des objets de données.</span><span class="sxs-lookup"><span data-stu-id="b641d-111">Do not use this parameter to add data objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b641d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b641d-112">Return value</span></span>

<span data-ttu-id="b641d-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b641d-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b641d-114">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="b641d-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="b641d-115">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b641d-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="b641d-116">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md), car cela entraînera l’échec de [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) également et retourne l’erreur.</span><span class="sxs-lookup"><span data-stu-id="b641d-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="b641d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b641d-117">Remarks</span></span>

<span data-ttu-id="b641d-118">**ID3DXSaveUserData :: RegisterTemplates** et [**ID3DXSaveUserData :: SaveTemplates**](id3dxsaveuserdata--savetemplates.md) fournissent un mécanisme d’ajout d’un modèle à un fichier. x pour l’enregistrement des données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b641d-118">**ID3DXSaveUserData::RegisterTemplates** and [**ID3DXSaveUserData::SaveTemplates**](id3dxsaveuserdata--savetemplates.md) provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="b641d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b641d-119">Requirements</span></span>



| <span data-ttu-id="b641d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b641d-120">Requirement</span></span> | <span data-ttu-id="b641d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b641d-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b641d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b641d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b641d-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="b641d-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b641d-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b641d-124">Library</span></span><br/> | <dl> <span data-ttu-id="b641d-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b641d-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b641d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b641d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b641d-127">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="b641d-127">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
