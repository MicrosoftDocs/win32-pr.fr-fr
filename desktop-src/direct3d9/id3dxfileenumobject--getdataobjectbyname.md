---
description: Récupère l’objet de données qui porte le nom spécifié.
ms.assetid: ed53d871-24e8-4c51-8897-1055ef8a9af1
title: 'ID3DXFileEnumObject :: GetDataObjectByName, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 41850615726ac15e890162c6e28df9b638c582a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531784"
---
# <a name="id3dxfileenumobjectgetdataobjectbyname-method"></a><span data-ttu-id="acf36-103">ID3DXFileEnumObject :: GetDataObjectByName, méthode</span><span class="sxs-lookup"><span data-stu-id="acf36-103">ID3DXFileEnumObject::GetDataObjectByName method</span></span>

<span data-ttu-id="acf36-104">Récupère l’objet de données qui porte le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="acf36-104">Retrieves the data object that has the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="acf36-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="acf36-105">Syntax</span></span>


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR        szName,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="acf36-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="acf36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acf36-107">*szName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="acf36-107">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acf36-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="acf36-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="acf36-109">Pointeur vers le nom demandé.</span><span class="sxs-lookup"><span data-stu-id="acf36-109">Pointer to the requested name.</span></span>

</dd> <dt>

<span data-ttu-id="acf36-110">*ppObj* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="acf36-110">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acf36-111">Type : **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="acf36-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="acf36-112">Adresse d’un pointeur vers une interface [**ID3DXFileData**](id3dxfiledata.md) , représentant l’objet de données de fichier retourné.</span><span class="sxs-lookup"><span data-stu-id="acf36-112">Address of a pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acf36-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="acf36-113">Return value</span></span>

<span data-ttu-id="acf36-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="acf36-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="acf36-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="acf36-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="acf36-116">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : DXFILEERR \_ BADVALUE, DXFILEERR \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="acf36-116">If the method fails, the return value can be one of the following:DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="acf36-117">Notes</span><span class="sxs-lookup"><span data-stu-id="acf36-117">Remarks</span></span>

<span data-ttu-id="acf36-118">Obtenez le nom szName de l’objet de données de fichier actuel à l’aide de la méthode [**ID3DXFileData :: GetName**](id3dxfiledata--getname.md) .</span><span class="sxs-lookup"><span data-stu-id="acf36-118">Obtain the name szName of the current file data object with the [**ID3DXFileData::GetName**](id3dxfiledata--getname.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="acf36-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acf36-119">Requirements</span></span>



| <span data-ttu-id="acf36-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acf36-120">Requirement</span></span> | <span data-ttu-id="acf36-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="acf36-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="acf36-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="acf36-122">Header</span></span><br/>  | <dl> <span data-ttu-id="acf36-123"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="acf36-123"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="acf36-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="acf36-124">Library</span></span><br/> | <dl> <span data-ttu-id="acf36-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="acf36-125"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="acf36-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acf36-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acf36-127">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="acf36-127">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
