---
description: Récupère l’objet de niveau supérieur suivant dans le fichier DirectX. Action déconseillée.
ms.assetid: 91cd3205-5603-4a62-aab2-7ef4adb9e6d1
title: 'IDirectXFileEnumObject :: GetNextDataObject, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetNextDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: bc50af216eaae1687351d472b7151aaaeae9116f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322669"
---
# <a name="idirectxfileenumobjectgetnextdataobject-method"></a><span data-ttu-id="12fd3-104">IDirectXFileEnumObject :: GetNextDataObject, méthode</span><span class="sxs-lookup"><span data-stu-id="12fd3-104">IDirectXFileEnumObject::GetNextDataObject method</span></span>

<span data-ttu-id="12fd3-105">Récupère l’objet de niveau supérieur suivant dans le fichier DirectX.</span><span class="sxs-lookup"><span data-stu-id="12fd3-105">Retrieves the next top-level object in the DirectX file.</span></span> <span data-ttu-id="12fd3-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="12fd3-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="12fd3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12fd3-107">Syntax</span></span>


```C++
HRESULT GetNextDataObject(
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="12fd3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12fd3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12fd3-109">*ppDataObj* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="12fd3-109">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12fd3-110">Type : **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="12fd3-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="12fd3-111">Adresse d’un pointeur vers une interface [**IDirectXFileData**](idirectxfiledata.md) , représentant l’objet de données de fichier retourné.</span><span class="sxs-lookup"><span data-stu-id="12fd3-111">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12fd3-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12fd3-112">Return value</span></span>

<span data-ttu-id="12fd3-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="12fd3-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="12fd3-114">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="12fd3-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="12fd3-115">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREOBJECTS</span><span class="sxs-lookup"><span data-stu-id="12fd3-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREOBJECTS</span></span>

## <a name="remarks"></a><span data-ttu-id="12fd3-116">Notes</span><span class="sxs-lookup"><span data-stu-id="12fd3-116">Remarks</span></span>

<span data-ttu-id="12fd3-117">Les objets de niveau supérieur sont toujours des objets de données.</span><span class="sxs-lookup"><span data-stu-id="12fd3-117">Top-level objects are always data objects.</span></span> <span data-ttu-id="12fd3-118">Les objets de référence de données et les objets binaires peuvent uniquement être des enfants d’objets de données.</span><span class="sxs-lookup"><span data-stu-id="12fd3-118">Data reference objects and binary objects can only be children of data objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="12fd3-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12fd3-119">Requirements</span></span>



| <span data-ttu-id="12fd3-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12fd3-120">Requirement</span></span> | <span data-ttu-id="12fd3-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="12fd3-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12fd3-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="12fd3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="12fd3-123"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="12fd3-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="12fd3-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="12fd3-124">Library</span></span><br/> | <dl> <span data-ttu-id="12fd3-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12fd3-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12fd3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12fd3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12fd3-127">IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="12fd3-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 




