---
description: Ajoute un objet de données en tant qu’objet enfant. Action déconseillée.
ms.assetid: 43771dd6-c17f-4376-9b0a-459ba61ff4c5
title: 'IDirectXFileData :: AddDataObject, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 393526bb249b0337964bee0af5be1b55b8dd513e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323137"
---
# <a name="idirectxfiledataadddataobject-method"></a><span data-ttu-id="75b0f-104">IDirectXFileData :: AddDataObject, méthode</span><span class="sxs-lookup"><span data-stu-id="75b0f-104">IDirectXFileData::AddDataObject method</span></span>

<span data-ttu-id="75b0f-105">Ajoute un objet de données en tant qu’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="75b0f-105">Adds a data object as a child object.</span></span> <span data-ttu-id="75b0f-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="75b0f-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="75b0f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75b0f-107">Syntax</span></span>


```C++
HRESULT AddDataObject(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="75b0f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75b0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75b0f-109">*pDataObj* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75b0f-109">*pDataObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b0f-110">Type : **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="75b0f-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span></span>

<span data-ttu-id="75b0f-111">Pointeur vers une interface [**IDirectXFileData**](idirectxfiledata.md) , représentant l’objet de données de fichier à ajouter en tant qu’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="75b0f-111">Pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the file data object to add as a child object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75b0f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75b0f-112">Return value</span></span>

<span data-ttu-id="75b0f-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="75b0f-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="75b0f-114">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="75b0f-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="75b0f-115">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="75b0f-115">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="75b0f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="75b0f-116">Remarks</span></span>

<span data-ttu-id="75b0f-117">Utilisez la méthode [**IDirectXFileSaveObject :: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) pour créer l’objet [**IDirectXFileData**](idirectxfiledata.md) avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="75b0f-117">Use the [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) method to create the [**IDirectXFileData**](idirectxfiledata.md) object before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="75b0f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75b0f-118">Requirements</span></span>



| <span data-ttu-id="75b0f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75b0f-119">Requirement</span></span> | <span data-ttu-id="75b0f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="75b0f-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75b0f-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="75b0f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="75b0f-122"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="75b0f-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="75b0f-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="75b0f-123">Library</span></span><br/> | <dl> <span data-ttu-id="75b0f-124"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75b0f-124"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75b0f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75b0f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75b0f-126">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="75b0f-126">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="75b0f-127">**IDirectXFileSaveObject::CreateDataObject**</span><span class="sxs-lookup"><span data-stu-id="75b0f-127">**IDirectXFileSaveObject::CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 




