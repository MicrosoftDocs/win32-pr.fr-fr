---
description: Crée un objet binaire et l’ajoute en tant qu’objet enfant. Action déconseillée.
ms.assetid: 6164951d-dd87-4318-ac08-b97c22f58d45
title: 'IDirectXFileData :: AddBinaryObject, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddBinaryObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 8373b9c4328a8683f32c1fe7ab979cb8d7636f87
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211691"
---
# <a name="idirectxfiledataaddbinaryobject-method"></a><span data-ttu-id="dfb21-104">IDirectXFileData :: AddBinaryObject, méthode</span><span class="sxs-lookup"><span data-stu-id="dfb21-104">IDirectXFileData::AddBinaryObject method</span></span>

<span data-ttu-id="dfb21-105">Crée un objet binaire et l’ajoute en tant qu’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="dfb21-105">Creates a binary object and adds it as a child object.</span></span> <span data-ttu-id="dfb21-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="dfb21-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfb21-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dfb21-107">Syntax</span></span>


```C++
HRESULT AddBinaryObject(
  [in]       LPCSTR szName,
  [in] const GUID   *pguid,
  [in]       LPCSTR szMimeType,
  [in]       LPVOID pvData,
  [in]       DWORD  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="dfb21-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dfb21-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfb21-109">*szName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dfb21-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb21-110">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dfb21-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dfb21-111">Pointeur vers le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dfb21-111">Pointer to the name of the object.</span></span> <span data-ttu-id="dfb21-112">Spécifiez **null** si l’objet n’a pas besoin d’un nom.</span><span class="sxs-lookup"><span data-stu-id="dfb21-112">Specify **NULL** if the object does not need a name.</span></span>

</dd> <dt>

<span data-ttu-id="dfb21-113">*pguid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dfb21-113">*pguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb21-114">Type : **const [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="dfb21-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="dfb21-115">Pointeur vers le GUID représentant l’objet.</span><span class="sxs-lookup"><span data-stu-id="dfb21-115">Pointer to the GUID representing the object.</span></span> <span data-ttu-id="dfb21-116">Spécifiez **null** si l’objet n’a pas besoin d’un GUID.</span><span class="sxs-lookup"><span data-stu-id="dfb21-116">Specify **NULL** if the object does not need a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="dfb21-117">*szMimeType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dfb21-117">*szMimeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb21-118">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dfb21-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dfb21-119">Pointeur vers le type MIME de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dfb21-119">Pointer to the object's MIME type.</span></span>

</dd> <dt>

<span data-ttu-id="dfb21-120">*pvData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dfb21-120">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb21-121">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dfb21-121">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dfb21-122">Pointeur vers les données de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dfb21-122">Pointer to the object's data.</span></span>

</dd> <dt>

<span data-ttu-id="dfb21-123">*cbSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dfb21-123">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb21-124">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dfb21-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dfb21-125">Taille de la mémoire tampon vers laquelle pointe pvData, en octets.</span><span class="sxs-lookup"><span data-stu-id="dfb21-125">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfb21-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dfb21-126">Return value</span></span>

<span data-ttu-id="dfb21-127">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dfb21-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dfb21-128">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dfb21-128">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="dfb21-129">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="dfb21-129">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="dfb21-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dfb21-130">Requirements</span></span>



| <span data-ttu-id="dfb21-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dfb21-131">Requirement</span></span> | <span data-ttu-id="dfb21-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfb21-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb21-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="dfb21-133">Header</span></span><br/>  | <dl> <span data-ttu-id="dfb21-134"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfb21-134"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="dfb21-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dfb21-135">Library</span></span><br/> | <dl> <span data-ttu-id="dfb21-136"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dfb21-136"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfb21-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfb21-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfb21-138">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="dfb21-138">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="dfb21-139">**IDirectXFileBinary::GetMimeType**</span><span class="sxs-lookup"><span data-stu-id="dfb21-139">**IDirectXFileBinary::GetMimeType**</span></span>](idirectxfilebinary--getmimetype.md)
</dt> </dl>

 

 
