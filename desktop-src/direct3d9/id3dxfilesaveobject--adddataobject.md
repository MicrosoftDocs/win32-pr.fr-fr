---
description: Ajoute un objet de données en tant qu’enfant de l’objet ID3DXFileSaveData.
ms.assetid: 710a1588-d766-4555-97a3-4b5a517ce805
title: 'ID3DXFileSaveObject :: AddDataObject, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d1586035a0d8a81c2210009bad903aac5197bcf7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542157"
---
# <a name="id3dxfilesaveobjectadddataobject-method"></a><span data-ttu-id="95254-103">ID3DXFileSaveObject :: AddDataObject, méthode</span><span class="sxs-lookup"><span data-stu-id="95254-103">ID3DXFileSaveObject::AddDataObject method</span></span>

<span data-ttu-id="95254-104">Ajoute un objet de données en tant qu’enfant de l’objet [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="95254-104">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="95254-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95254-105">Syntax</span></span>


```C++
HRESULT AddDataObject(
  [in]               REFGUID           rguidTemplate,
  [in]               LPCSTR            szName,
  [in]         const GUID              *pId,
  [in]               SIZE_T            cbSize,
  [in]               LPCVOID           pvData,
  [in, retval]       ID3DXFileSaveData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="95254-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95254-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95254-107">*rguidTemplate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="95254-107">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95254-108">Type : **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="95254-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="95254-109">GUID représentant le modèle de l’objet de données.</span><span class="sxs-lookup"><span data-stu-id="95254-109">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="95254-110">*szName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="95254-110">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95254-111">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95254-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95254-112">Pointeur vers le nom de l’objet de données.</span><span class="sxs-lookup"><span data-stu-id="95254-112">Pointer to the name of the data object.</span></span> <span data-ttu-id="95254-113">Spécifiez **null** si l’objet n’a pas de nom.</span><span class="sxs-lookup"><span data-stu-id="95254-113">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="95254-114">*PID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="95254-114">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95254-115">Type : **const [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="95254-115">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="95254-116">Pointeur vers un GUID représentant l’objet de données.</span><span class="sxs-lookup"><span data-stu-id="95254-116">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="95254-117">Spécifiez **null** si l’objet n’a pas de GUID.</span><span class="sxs-lookup"><span data-stu-id="95254-117">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="95254-118">*cbSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="95254-118">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95254-119">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95254-119">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95254-120">Taille de l’objet de données, en octets.</span><span class="sxs-lookup"><span data-stu-id="95254-120">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="95254-121">*pvData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="95254-121">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95254-122">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95254-122">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95254-123">Pointeur vers une mémoire tampon contenant toutes les données requises dans l’objet de données.</span><span class="sxs-lookup"><span data-stu-id="95254-123">Pointer to a buffer containing all required data in the data object.</span></span>

</dd> <dt>

<span data-ttu-id="95254-124">*ppObj* \[ dans, retval\]</span><span class="sxs-lookup"><span data-stu-id="95254-124">*ppObj* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="95254-125">Type : **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="95254-125">Type: **[**ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span></span>

<span data-ttu-id="95254-126">Adresse d’un pointeur vers une interface [**ID3DXFileSaveData**](id3dxfilesavedata.md) , représentant le nœud de données de fichier auquel l’objet de données sera ajouté.</span><span class="sxs-lookup"><span data-stu-id="95254-126">Address of a pointer to an [**ID3DXFileSaveData**](id3dxfilesavedata.md) interface, representing the file data node to which the data object will be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95254-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95254-127">Return value</span></span>

<span data-ttu-id="95254-128">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95254-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95254-129">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="95254-129">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="95254-130">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DXFERR \_ BADOBJECT, DXFILEERR \_ BADVALUE, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="95254-130">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, DXFILEERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="95254-131">Notes</span><span class="sxs-lookup"><span data-stu-id="95254-131">Remarks</span></span>

<span data-ttu-id="95254-132">Si un objet de référence de données fait référence à l’objet de données, le paramètre szName ou pId doit avoir une **valeur non null**.</span><span class="sxs-lookup"><span data-stu-id="95254-132">If a data reference object will reference the data object, either the szName or pId parameter must be non-**NULL**.</span></span>

<span data-ttu-id="95254-133">Enregistrez les données créées sur le disque à l’aide de la méthode [**ID3DXFileSaveObject :: Save**](id3dxfilesaveobject--save.md) .</span><span class="sxs-lookup"><span data-stu-id="95254-133">Save the created data to disk by using the [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="95254-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95254-134">Requirements</span></span>



| <span data-ttu-id="95254-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95254-135">Requirement</span></span> | <span data-ttu-id="95254-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="95254-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95254-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="95254-137">Header</span></span><br/>  | <dl> <span data-ttu-id="95254-138"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="95254-138"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="95254-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="95254-139">Library</span></span><br/> | <dl> <span data-ttu-id="95254-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95254-140"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="95254-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95254-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95254-142">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="95254-142">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 
