---
description: Résout les références de données. Action déconseillée.
ms.assetid: e8cf6e5d-c9b2-4a47-b058-24282dc65e74
title: 'IDirectXFileDataReference :: Resolve, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference.Resolve
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1b047245e3f89a618cde83e5c18a323f9364f3ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520339"
---
# <a name="idirectxfiledatareferenceresolve-method"></a><span data-ttu-id="3da5d-104">IDirectXFileDataReference :: Resolve, méthode</span><span class="sxs-lookup"><span data-stu-id="3da5d-104">IDirectXFileDataReference::Resolve method</span></span>

<span data-ttu-id="3da5d-105">Résout les références de données.</span><span class="sxs-lookup"><span data-stu-id="3da5d-105">Resolves data references.</span></span> <span data-ttu-id="3da5d-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="3da5d-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="3da5d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3da5d-107">Syntax</span></span>


```C++
HRESULT Resolve(
  [out, retval] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="3da5d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3da5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3da5d-109">*ppDataObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3da5d-109">*ppDataObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3da5d-110">Type : **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="3da5d-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="3da5d-111">Adresse d’un pointeur vers une interface [**IDirectXFileData**](idirectxfiledata.md) , représentant l’objet de données de fichier retourné.</span><span class="sxs-lookup"><span data-stu-id="3da5d-111">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3da5d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3da5d-112">Return value</span></span>

<span data-ttu-id="3da5d-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3da5d-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3da5d-114">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3da5d-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="3da5d-115">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : DXFILEERR \_ BADVALUE, DXFILEERR \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="3da5d-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="3da5d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3da5d-116">Requirements</span></span>



| <span data-ttu-id="3da5d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3da5d-117">Requirement</span></span> | <span data-ttu-id="3da5d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3da5d-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3da5d-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="3da5d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3da5d-120"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="3da5d-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="3da5d-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3da5d-121">Library</span></span><br/> | <dl> <span data-ttu-id="3da5d-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3da5d-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3da5d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3da5d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da5d-124">IDirectXFileDataReference</span><span class="sxs-lookup"><span data-stu-id="3da5d-124">IDirectXFileDataReference</span></span>](idirectxfiledatareference.md)
</dt> </dl>

 

 




