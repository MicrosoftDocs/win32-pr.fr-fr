---
description: Crée un objet de données. Action déconseillée.
ms.assetid: bb0ef2cf-db76-40f6-968f-3599c58459a7
title: 'IDirectXFileSaveObject :: CreateDataObject, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.CreateDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 7c5a67a72f6ff5a63730167d2fe2d12213a9ab72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322846"
---
# <a name="idirectxfilesaveobjectcreatedataobject-method"></a><span data-ttu-id="783c5-104">IDirectXFileSaveObject :: CreateDataObject, méthode</span><span class="sxs-lookup"><span data-stu-id="783c5-104">IDirectXFileSaveObject::CreateDataObject method</span></span>

<span data-ttu-id="783c5-105">Crée un objet de données.</span><span class="sxs-lookup"><span data-stu-id="783c5-105">Creates a data object.</span></span> <span data-ttu-id="783c5-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="783c5-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="783c5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="783c5-107">Syntax</span></span>


```C++
HRESULT CreateDataObject(
  [in]                REFGUID           rguidTemplate,
  [in]                LPCSTR            szName,
  [in]          const GUID              *pguid,
  [in]                DWORD             cbSize,
  [in]                LPVOID            pvData,
  [out, retval]       LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="783c5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="783c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="783c5-109">*rguidTemplate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="783c5-109">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="783c5-110">Type : **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="783c5-110">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="783c5-111">GUID représentant le modèle de l’objet de données.</span><span class="sxs-lookup"><span data-stu-id="783c5-111">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="783c5-112">*szName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="783c5-112">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="783c5-113">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="783c5-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="783c5-114">Pointeur vers le nom de l’objet de données.</span><span class="sxs-lookup"><span data-stu-id="783c5-114">Pointer to the name of the data object.</span></span> <span data-ttu-id="783c5-115">Spécifiez **null** si l’objet n’a pas de nom.</span><span class="sxs-lookup"><span data-stu-id="783c5-115">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="783c5-116">*pguid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="783c5-116">*pguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="783c5-117">Type : **const [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="783c5-117">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="783c5-118">Pointeur vers un GUID représentant l’objet de données.</span><span class="sxs-lookup"><span data-stu-id="783c5-118">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="783c5-119">Spécifiez **null** si l’objet n’a pas de GUID.</span><span class="sxs-lookup"><span data-stu-id="783c5-119">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="783c5-120">*cbSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="783c5-120">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="783c5-121">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="783c5-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="783c5-122">Taille de l’objet de données, en octets.</span><span class="sxs-lookup"><span data-stu-id="783c5-122">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="783c5-123">*pvData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="783c5-123">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="783c5-124">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="783c5-124">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="783c5-125">Pointeur vers une mémoire tampon contenant toutes les données du membre requis.</span><span class="sxs-lookup"><span data-stu-id="783c5-125">Pointer to a buffer containing all required member's data.</span></span>

</dd> <dt>

<span data-ttu-id="783c5-126">*ppDataObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="783c5-126">*ppDataObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="783c5-127">Type : **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="783c5-127">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="783c5-128">Adresse d’un pointeur vers une interface [**IDirectXFileData**](idirectxfiledata.md) , représentant l’objet de données de fichier créé.</span><span class="sxs-lookup"><span data-stu-id="783c5-128">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the created file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="783c5-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="783c5-129">Return value</span></span>

<span data-ttu-id="783c5-130">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="783c5-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="783c5-131">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="783c5-131">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="783c5-132">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="783c5-132">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="783c5-133">Notes</span><span class="sxs-lookup"><span data-stu-id="783c5-133">Remarks</span></span>

<span data-ttu-id="783c5-134">Si un objet de référence de données fait référence à l’objet de données, le paramètre szName ou pguid doit avoir une **valeur non null**.</span><span class="sxs-lookup"><span data-stu-id="783c5-134">If a data reference object will reference the data object, either the szName or pguid parameter must be non-**NULL**.</span></span>

<span data-ttu-id="783c5-135">Enregistrez les modèles à l’aide de la méthode [**IDirectXFileSaveObject :: SaveTemplates**](idirectxfilesaveobject--savetemplates.md) avant d’enregistrer les données créées par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="783c5-135">Save any templates by using the [**IDirectXFileSaveObject::SaveTemplates**](idirectxfilesaveobject--savetemplates.md) method before saving the data created by this method.</span></span> <span data-ttu-id="783c5-136">Enregistrez les données créées à l’aide de la méthode [**IDirectXFileSaveObject :: SaveData**](idirectxfilesaveobject--savedata.md) .</span><span class="sxs-lookup"><span data-stu-id="783c5-136">Save the created data by using the [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) method.</span></span>

<span data-ttu-id="783c5-137">Si vous devez enregistrer des données facultatives, utilisez la méthode [**IDirectXFileData :: AddDataObject**](idirectxfiledata--adddataobject.md) après avoir utilisé cette méthode et avant d’utiliser [**IDirectXFileSaveObject :: SaveData**](idirectxfilesaveobject--savedata.md).</span><span class="sxs-lookup"><span data-stu-id="783c5-137">If you need to save optional data, use the [**IDirectXFileData::AddDataObject**](idirectxfiledata--adddataobject.md) method after using this method and before using [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md).</span></span> <span data-ttu-id="783c5-138">Si l’objet a des objets enfants, ajoutez-les avant d’appeler **IDirectXFileSaveObject :: SaveData**.</span><span class="sxs-lookup"><span data-stu-id="783c5-138">If the object has child objects, add them before calling **IDirectXFileSaveObject::SaveData**.</span></span>

## <a name="requirements"></a><span data-ttu-id="783c5-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="783c5-139">Requirements</span></span>



| <span data-ttu-id="783c5-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="783c5-140">Requirement</span></span> | <span data-ttu-id="783c5-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="783c5-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="783c5-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="783c5-142">Header</span></span><br/>  | <dl> <span data-ttu-id="783c5-143"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="783c5-143"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="783c5-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="783c5-144">Library</span></span><br/> | <dl> <span data-ttu-id="783c5-145"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="783c5-145"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="783c5-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="783c5-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="783c5-147">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="783c5-147">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> <dt>

[<span data-ttu-id="783c5-148">**IDirectXFileData::AddDataObject**</span><span class="sxs-lookup"><span data-stu-id="783c5-148">**IDirectXFileData::AddDataObject**</span></span>](idirectxfiledata--adddataobject.md)
</dt> <dt>

[<span data-ttu-id="783c5-149">**IDirectXFileSaveObject :: SaveData**</span><span class="sxs-lookup"><span data-stu-id="783c5-149">**IDirectXFileSaveObject::SaveData**</span></span>](idirectxfilesaveobject--savedata.md)
</dt> <dt>

[<span data-ttu-id="783c5-150">**IDirectXFileSaveObject::SaveTemplates**</span><span class="sxs-lookup"><span data-stu-id="783c5-150">**IDirectXFileSaveObject::SaveTemplates**</span></span>](idirectxfilesaveobject--savetemplates.md)
</dt> </dl>

 

 
