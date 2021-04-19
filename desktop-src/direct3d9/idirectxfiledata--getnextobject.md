---
description: Récupère l’objet de données enfants, l’objet de référence de données ou l’objet binaire suivant dans le fichier DirectX. Action déconseillée.
ms.assetid: 8232e911-6552-4b2b-a9c2-59e6a13a0d9b
title: 'IDirectXFileData :: GetNextObject, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetNextObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e03351068cdc4f8fca28c612b7bb4c546125a4cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531563"
---
# <a name="idirectxfiledatagetnextobject-method"></a><span data-ttu-id="020ce-104">IDirectXFileData :: GetNextObject, méthode</span><span class="sxs-lookup"><span data-stu-id="020ce-104">IDirectXFileData::GetNextObject method</span></span>

<span data-ttu-id="020ce-105">Récupère l’objet de données enfants, l’objet de référence de données ou l’objet binaire suivant dans le fichier DirectX.</span><span class="sxs-lookup"><span data-stu-id="020ce-105">Retrieves the next child data object, data reference object, or binary object in the DirectX file.</span></span> <span data-ttu-id="020ce-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="020ce-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="020ce-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="020ce-107">Syntax</span></span>


```C++
HRESULT GetNextObject(
  [out, retval] LPDIRECTXFILEOBJECT *ppChildObj
);
```



## <a name="parameters"></a><span data-ttu-id="020ce-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="020ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="020ce-109">*ppChildObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="020ce-109">*ppChildObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="020ce-110">Type : **[ **LPDIRECTXFILEOBJECT**](idirectxfileobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="020ce-110">Type: **[**LPDIRECTXFILEOBJECT**](idirectxfileobject.md)\***</span></span>

<span data-ttu-id="020ce-111">Adresse d’un pointeur vers une interface [**IDirectXFileObject**](idirectxfileobject.md) , représentant l’interface d’objet fichier de l’objet enfant retourné.</span><span class="sxs-lookup"><span data-stu-id="020ce-111">Address of a pointer to an [**IDirectXFileObject**](idirectxfileobject.md) interface, representing the returned child object's file object interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="020ce-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="020ce-112">Return value</span></span>

<span data-ttu-id="020ce-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="020ce-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="020ce-114">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="020ce-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="020ce-115">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="020ce-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREOBJECTS.</span></span>

## <a name="remarks"></a><span data-ttu-id="020ce-116">Notes</span><span class="sxs-lookup"><span data-stu-id="020ce-116">Remarks</span></span>

<span data-ttu-id="020ce-117">Pour déterminer le type d’objet récupéré, utilisez QueryInterface pour interroger l’objet récupéré pour la prise en charge des interfaces [**IDirectXFileData**](idirectxfiledata.md), [**IDirectXFileDataReference**](idirectxfiledatareference.md)ou [**IDirectXFileBinary**](idirectxfilebinary.md) .</span><span class="sxs-lookup"><span data-stu-id="020ce-117">To determine the type of object retrieved, use QueryInterface to query the retrieved object for support of [**IDirectXFileData**](idirectxfiledata.md), [**IDirectXFileDataReference**](idirectxfiledatareference.md), or [**IDirectXFileBinary**](idirectxfilebinary.md) interfaces.</span></span> <span data-ttu-id="020ce-118">L’interface prise en charge indique le type d’objet (données, référence de données ou binaire).</span><span class="sxs-lookup"><span data-stu-id="020ce-118">The interface supported indicates the type of object (data, data reference, or binary).</span></span>

## <a name="requirements"></a><span data-ttu-id="020ce-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="020ce-119">Requirements</span></span>



| <span data-ttu-id="020ce-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="020ce-120">Requirement</span></span> | <span data-ttu-id="020ce-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="020ce-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="020ce-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="020ce-122">Header</span></span><br/>  | <dl> <span data-ttu-id="020ce-123"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="020ce-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="020ce-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="020ce-124">Library</span></span><br/> | <dl> <span data-ttu-id="020ce-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="020ce-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="020ce-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="020ce-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="020ce-127">**IDirectXFileBinary**</span><span class="sxs-lookup"><span data-stu-id="020ce-127">**IDirectXFileBinary**</span></span>](idirectxfilebinary.md)
</dt> <dt>

[<span data-ttu-id="020ce-128">**IDirectXFileData**</span><span class="sxs-lookup"><span data-stu-id="020ce-128">**IDirectXFileData**</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="020ce-129">**IDirectXFileDataReference**</span><span class="sxs-lookup"><span data-stu-id="020ce-129">**IDirectXFileDataReference**</span></span>](idirectxfiledatareference.md)
</dt> </dl>

 

 




