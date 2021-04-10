---
description: Ajoute une référence de données en tant qu’enfant de ce nœud de données de fichier ID3DXFileSaveData. La référence de données pointe vers un objet de données de fichier.
ms.assetid: 75bfe91e-15ea-41f3-b1f7-071fb7f0093f
title: 'ID3DXFileSaveData :: AddDataReference, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataReference
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f4aabf5601ef73f4e1062b1db1a28c1f0deae5fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953904"
---
# <a name="id3dxfilesavedataadddatareference-method"></a><span data-ttu-id="826d7-104">ID3DXFileSaveData :: AddDataReference, méthode</span><span class="sxs-lookup"><span data-stu-id="826d7-104">ID3DXFileSaveData::AddDataReference method</span></span>

<span data-ttu-id="826d7-105">Ajoute une référence de données en tant qu’enfant de ce nœud de données de fichier [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="826d7-105">Adds a data reference as a child of this [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span> <span data-ttu-id="826d7-106">La référence de données pointe vers un objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="826d7-106">The data reference points to a file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="826d7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="826d7-107">Syntax</span></span>


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szName,
  [in] const GUID   *pId
);
```



## <a name="parameters"></a><span data-ttu-id="826d7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="826d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="826d7-109">*szName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="826d7-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="826d7-110">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="826d7-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="826d7-111">Pointeur vers le nom de l’objet de données à ajouter par référence.</span><span class="sxs-lookup"><span data-stu-id="826d7-111">Pointer to the name of the data object to add by reference.</span></span> <span data-ttu-id="826d7-112">Spécifiez **null** si l’objet de données n’a pas de nom.</span><span class="sxs-lookup"><span data-stu-id="826d7-112">Specify **NULL** if the data object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="826d7-113">*PID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="826d7-113">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="826d7-114">Type : **const [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="826d7-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="826d7-115">Pointeur vers un GUID représentant l’objet de données à ajouter par référence.</span><span class="sxs-lookup"><span data-stu-id="826d7-115">Pointer to a GUID representing the data object to add by reference.</span></span> <span data-ttu-id="826d7-116">Si la **valeur est null**, une référence qui pointe vers l’objet de données avec le nom donné par szName est ajoutée.</span><span class="sxs-lookup"><span data-stu-id="826d7-116">If **NULL**, a reference will be added that points to the data object with the name given by szName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="826d7-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="826d7-117">Return value</span></span>

<span data-ttu-id="826d7-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="826d7-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="826d7-119">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="826d7-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="826d7-120">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="826d7-120">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="826d7-121">Notes</span><span class="sxs-lookup"><span data-stu-id="826d7-121">Remarks</span></span>

<span data-ttu-id="826d7-122">L’objet de données de fichier référencé doit avoir un nom ou un GUID.</span><span class="sxs-lookup"><span data-stu-id="826d7-122">The file data object being referenced must have either a name or a GUID.</span></span> <span data-ttu-id="826d7-123">L’objet de données de fichier doit également dériver d’un objet [**ID3DXFileSaveData**](id3dxfilesavedata.md) parent différent.</span><span class="sxs-lookup"><span data-stu-id="826d7-123">The file data object must also derive from a different parent [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="826d7-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="826d7-124">Requirements</span></span>



| <span data-ttu-id="826d7-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="826d7-125">Requirement</span></span> | <span data-ttu-id="826d7-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="826d7-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="826d7-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="826d7-127">Header</span></span><br/>  | <dl> <span data-ttu-id="826d7-128"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="826d7-128"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="826d7-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="826d7-129">Library</span></span><br/> | <dl> <span data-ttu-id="826d7-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="826d7-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="826d7-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="826d7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="826d7-132">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="826d7-132">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 
