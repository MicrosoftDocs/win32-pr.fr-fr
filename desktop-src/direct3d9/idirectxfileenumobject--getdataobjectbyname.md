---
description: Récupère l’objet de données qui porte le nom spécifié. Action déconseillée.
ms.assetid: d04d5a45-72d9-4256-8700-378e8139ed36
title: 'IDirectXFileEnumObject :: GetDataObjectByName, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 858097139702770d148765c4c9a57f6522d9633b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535204"
---
# <a name="idirectxfileenumobjectgetdataobjectbyname-method"></a><span data-ttu-id="9590d-104">IDirectXFileEnumObject :: GetDataObjectByName, méthode</span><span class="sxs-lookup"><span data-stu-id="9590d-104">IDirectXFileEnumObject::GetDataObjectByName method</span></span>

<span data-ttu-id="9590d-105">Récupère l’objet de données qui porte le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="9590d-105">Retrieves the data object that has the specified name.</span></span> <span data-ttu-id="9590d-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="9590d-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="9590d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9590d-107">Syntax</span></span>


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR            szName,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="9590d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9590d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9590d-109">*szName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9590d-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9590d-110">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9590d-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9590d-111">Pointeur vers le nom demandé.</span><span class="sxs-lookup"><span data-stu-id="9590d-111">Pointer to the requested name.</span></span>

</dd> <dt>

<span data-ttu-id="9590d-112">*ppDataObj* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9590d-112">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9590d-113">Type : **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="9590d-113">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="9590d-114">Adresse d’un pointeur vers une interface [**IDirectXFileData**](idirectxfiledata.md) , représentant l’objet de données de fichier retourné.</span><span class="sxs-lookup"><span data-stu-id="9590d-114">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9590d-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9590d-115">Return value</span></span>

<span data-ttu-id="9590d-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9590d-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9590d-117">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9590d-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="9590d-118">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : DXFILEERR \_ BADVALUE, DXFILEERR \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="9590d-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="9590d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9590d-119">Requirements</span></span>



| <span data-ttu-id="9590d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9590d-120">Requirement</span></span> | <span data-ttu-id="9590d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9590d-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9590d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9590d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9590d-123"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="9590d-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="9590d-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9590d-124">Library</span></span><br/> | <dl> <span data-ttu-id="9590d-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9590d-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9590d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9590d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9590d-127">IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="9590d-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 
