---
description: 'ID3DXFileEnumObject :: GetChild, méthode-récupère un objet enfant dans cet objet de données de fichier.'
ms.assetid: d8f367dd-8858-48ae-9de5-17de1538aadf
title: 'ID3DXFileEnumObject :: GetChild, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b26cf058b31d1016c68cccf3dde6ade9f84cde1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090357"
---
# <a name="id3dxfileenumobjectgetchild-method"></a><span data-ttu-id="c67eb-103">ID3DXFileEnumObject :: GetChild, méthode</span><span class="sxs-lookup"><span data-stu-id="c67eb-103">ID3DXFileEnumObject::GetChild method</span></span>

<span data-ttu-id="c67eb-104">Récupère un objet enfant dans cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="c67eb-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c67eb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c67eb-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in]  SIZE_T        id,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="c67eb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c67eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c67eb-107">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c67eb-107">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c67eb-108">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c67eb-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c67eb-109">ID de l’objet enfant à récupérer.</span><span class="sxs-lookup"><span data-stu-id="c67eb-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="c67eb-110">*ppObj* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c67eb-110">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c67eb-111">Type : **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c67eb-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="c67eb-112">Adresse d’un pointeur pour recevoir le pointeur d’interface de l’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="c67eb-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c67eb-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c67eb-113">Return value</span></span>

<span data-ttu-id="c67eb-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c67eb-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c67eb-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c67eb-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c67eb-116">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="c67eb-116">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="c67eb-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c67eb-117">Requirements</span></span>



| <span data-ttu-id="c67eb-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c67eb-118">Requirement</span></span> | <span data-ttu-id="c67eb-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c67eb-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c67eb-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c67eb-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c67eb-121"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="c67eb-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="c67eb-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c67eb-122">Library</span></span><br/> | <dl> <span data-ttu-id="c67eb-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c67eb-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c67eb-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c67eb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c67eb-125">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="c67eb-125">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
