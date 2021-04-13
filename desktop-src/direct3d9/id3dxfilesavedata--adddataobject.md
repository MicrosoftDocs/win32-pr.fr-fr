---
description: Ajoute un objet de données en tant qu’enfant du nœud de données du fichier ID3DXFileSaveData.
ms.assetid: 47faad99-3ee8-4ca8-b8d7-413d4cd5b090
title: 'ID3DXFileSaveData :: AddDataObject, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b097e63792b32bc1688ce93c8ce32ffaedeae6ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323065"
---
# <a name="id3dxfilesavedataadddataobject-method"></a><span data-ttu-id="5a4a9-103">ID3DXFileSaveData :: AddDataObject, méthode</span><span class="sxs-lookup"><span data-stu-id="5a4a9-103">ID3DXFileSaveData::AddDataObject method</span></span>

<span data-ttu-id="5a4a9-104">Ajoute un objet de données en tant qu’enfant du nœud de données du fichier [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="5a4a9-104">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a4a9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a4a9-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="5a4a9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a4a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a4a9-107">*rguidTemplate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a4a9-107">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a4a9-108">Type : **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="5a4a9-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="5a4a9-109">GUID représentant le modèle de l’objet de données.</span><span class="sxs-lookup"><span data-stu-id="5a4a9-109">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="5a4a9-110">*szName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a4a9-110">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a4a9-111">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a4a9-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a4a9-112">Pointeur vers le nom de l’objet de données à ajouter.</span><span class="sxs-lookup"><span data-stu-id="5a4a9-112">Pointer to the name of the data object to add.</span></span> <span data-ttu-id="5a4a9-113">Spécifiez **null** si l’objet n’a pas de nom.</span><span class="sxs-lookup"><span data-stu-id="5a4a9-113">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="5a4a9-114">*PID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a4a9-114">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a4a9-115">Type : **const [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="5a4a9-115">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="5a4a9-116">Pointeur vers un GUID représentant l’objet de données.</span><span class="sxs-lookup"><span data-stu-id="5a4a9-116">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="5a4a9-117">L’objet de données doit avoir été enregistré avec [**ID3DXFile :: RegisterTemplates**](id3dxfile--registertemplates.md) ou [**ID3DXFile :: RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md).</span><span class="sxs-lookup"><span data-stu-id="5a4a9-117">The data object must have been registered with [**ID3DXFile::RegisterTemplates**](id3dxfile--registertemplates.md) or [**ID3DXFile::RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md).</span></span> <span data-ttu-id="5a4a9-118">Spécifiez **null** si l’objet n’a pas de GUID.</span><span class="sxs-lookup"><span data-stu-id="5a4a9-118">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="5a4a9-119">*cbSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a4a9-119">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a4a9-120">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a4a9-120">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a4a9-121">Taille de l’objet de données, en octets.</span><span class="sxs-lookup"><span data-stu-id="5a4a9-121">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5a4a9-122">*pvData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a4a9-122">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a4a9-123">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a4a9-123">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a4a9-124">Pointeur vers une mémoire tampon contenant toutes les données requises dans l’objet de données.</span><span class="sxs-lookup"><span data-stu-id="5a4a9-124">Pointer to a buffer containing all required data in the data object.</span></span>

</dd> <dt>

<span data-ttu-id="5a4a9-125">*ppObj* \[ dans, retval\]</span><span class="sxs-lookup"><span data-stu-id="5a4a9-125">*ppObj* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5a4a9-126">Type : **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="5a4a9-126">Type: **[**ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span></span>

<span data-ttu-id="5a4a9-127">Adresse d’un pointeur vers une interface [**ID3DXFileSaveData**](id3dxfilesavedata.md) , représentant le nœud de données de fichier auquel l’objet de données sera ajouté.</span><span class="sxs-lookup"><span data-stu-id="5a4a9-127">Address of a pointer to an [**ID3DXFileSaveData**](id3dxfilesavedata.md) interface, representing the file data node to which the data object will be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a4a9-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a4a9-128">Return value</span></span>

<span data-ttu-id="5a4a9-129">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5a4a9-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5a4a9-130">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5a4a9-130">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5a4a9-131">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5a4a9-131">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a4a9-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a4a9-132">Requirements</span></span>



| <span data-ttu-id="5a4a9-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a4a9-133">Requirement</span></span> | <span data-ttu-id="5a4a9-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a4a9-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a4a9-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a4a9-135">Header</span></span><br/>  | <dl> <span data-ttu-id="5a4a9-136"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a4a9-136"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="5a4a9-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5a4a9-137">Library</span></span><br/> | <dl> <span data-ttu-id="5a4a9-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a4a9-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5a4a9-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a4a9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a4a9-140">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="5a4a9-140">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 
