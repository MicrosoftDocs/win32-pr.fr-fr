---
description: Récupère l’objet de données qui a le GUID spécifié. Action déconseillée.
ms.assetid: dd079b5c-18e1-4252-aabd-498c24910a08
title: 'IDirectXFileEnumObject :: GetDataObjectById, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: a27ac17963d4876a3cb0a26d05b63f4c34bf99fc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531777"
---
# <a name="idirectxfileenumobjectgetdataobjectbyid-method"></a><span data-ttu-id="16a93-104">IDirectXFileEnumObject :: GetDataObjectById, méthode</span><span class="sxs-lookup"><span data-stu-id="16a93-104">IDirectXFileEnumObject::GetDataObjectById method</span></span>

<span data-ttu-id="16a93-105">Récupère l’objet de données qui a le GUID spécifié.</span><span class="sxs-lookup"><span data-stu-id="16a93-105">Retrieves the data object that has the specified GUID.</span></span> <span data-ttu-id="16a93-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="16a93-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="16a93-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16a93-107">Syntax</span></span>


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID           rguid,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="16a93-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16a93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16a93-109">*rguid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16a93-109">*rguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16a93-110">Type : **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="16a93-110">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="16a93-111">Référence au GUID demandé.</span><span class="sxs-lookup"><span data-stu-id="16a93-111">Reference to the requested GUID.</span></span>

</dd> <dt>

<span data-ttu-id="16a93-112">*ppDataObj* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="16a93-112">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16a93-113">Type : **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="16a93-113">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="16a93-114">Adresse d’un pointeur vers une interface [**IDirectXFileData**](idirectxfiledata.md) , représentant l’objet de données de fichier retourné.</span><span class="sxs-lookup"><span data-stu-id="16a93-114">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16a93-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16a93-115">Return value</span></span>

<span data-ttu-id="16a93-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="16a93-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="16a93-117">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="16a93-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="16a93-118">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : DXFILEERR \_ BADVALUE, DXFILEERR \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="16a93-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="16a93-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16a93-119">Requirements</span></span>



| <span data-ttu-id="16a93-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16a93-120">Requirement</span></span> | <span data-ttu-id="16a93-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="16a93-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16a93-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="16a93-122">Header</span></span><br/>  | <dl> <span data-ttu-id="16a93-123"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="16a93-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="16a93-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="16a93-124">Library</span></span><br/> | <dl> <span data-ttu-id="16a93-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16a93-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16a93-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16a93-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16a93-127">IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="16a93-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 
