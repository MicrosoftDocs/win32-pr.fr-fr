---
description: Récupère l’objet de données qui a le GUID spécifié.
ms.assetid: c3d598bd-0646-4f99-8517-4475ef7cd8c9
title: 'ID3DXFileEnumObject :: GetDataObjectById, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 82a74ca4ff472d678ded92aa01f2c2406560955e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525892"
---
# <a name="id3dxfileenumobjectgetdataobjectbyid-method"></a><span data-ttu-id="ef92c-103">ID3DXFileEnumObject :: GetDataObjectById, méthode</span><span class="sxs-lookup"><span data-stu-id="ef92c-103">ID3DXFileEnumObject::GetDataObjectById method</span></span>

<span data-ttu-id="ef92c-104">Récupère l’objet de données qui a le GUID spécifié.</span><span class="sxs-lookup"><span data-stu-id="ef92c-104">Retrieves the data object that has the specified GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef92c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef92c-105">Syntax</span></span>


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID        rguid,
  [out] LPD3DXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="ef92c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef92c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef92c-107">*rguid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef92c-107">*rguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef92c-108">Type : **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="ef92c-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="ef92c-109">Référence au GUID demandé.</span><span class="sxs-lookup"><span data-stu-id="ef92c-109">Reference to the requested GUID.</span></span>

</dd> <dt>

<span data-ttu-id="ef92c-110">*ppDataObj* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ef92c-110">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef92c-111">Type : **[ **LPD3DXFILEDATA**](id3dxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="ef92c-111">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)\***</span></span>

<span data-ttu-id="ef92c-112">Adresse d’un pointeur vers une interface [**ID3DXFileData**](id3dxfiledata.md) , représentant l’objet de données de fichier retourné.</span><span class="sxs-lookup"><span data-stu-id="ef92c-112">Address of a pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef92c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef92c-113">Return value</span></span>

<span data-ttu-id="ef92c-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ef92c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ef92c-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ef92c-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ef92c-116">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : DXFILEERR \_ BADVALUE, DXFILEERR \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="ef92c-116">If the method fails, the return value can be one of the following:DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef92c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ef92c-117">Remarks</span></span>

<span data-ttu-id="ef92c-118">Obtient le GUID rguid de l’objet de données de fichier actuel avec la méthode [**ID3DXFileData :: GetId**](id3dxfiledata--getid.md) .</span><span class="sxs-lookup"><span data-stu-id="ef92c-118">Obtain the GUID rguid of the current file data object with the [**ID3DXFileData::GetId**](id3dxfiledata--getid.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef92c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef92c-119">Requirements</span></span>



| <span data-ttu-id="ef92c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef92c-120">Requirement</span></span> | <span data-ttu-id="ef92c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef92c-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef92c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef92c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ef92c-123"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef92c-123"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="ef92c-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ef92c-124">Library</span></span><br/> | <dl> <span data-ttu-id="ef92c-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef92c-125"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ef92c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef92c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef92c-127">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="ef92c-127">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
