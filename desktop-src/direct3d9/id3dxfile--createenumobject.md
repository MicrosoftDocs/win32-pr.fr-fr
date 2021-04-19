---
description: Crée un objet énumérateur qui lira un fichier. x.
ms.assetid: 86d05eab-601c-4beb-9dbe-c23fa524871c
title: 'ID3DXFile :: CreateEnumObject, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a58a3341bacf9b323cc5753f8e9e51c4b703b966
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531785"
---
# <a name="id3dxfilecreateenumobject-method"></a><span data-ttu-id="54b3c-103">ID3DXFile :: CreateEnumObject, méthode</span><span class="sxs-lookup"><span data-stu-id="54b3c-103">ID3DXFile::CreateEnumObject method</span></span>

<span data-ttu-id="54b3c-104">Crée un objet énumérateur qui lira un fichier. x.</span><span class="sxs-lookup"><span data-stu-id="54b3c-104">Creates an enumerator object that will read a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="54b3c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54b3c-105">Syntax</span></span>


```C++
HRESULT CreateEnumObject(
  [out] LPCVOID               pvSource,
  [in]  D3DXF_FILELOADOPTIONS loadflags,
  [out] ID3DXFileEnumObject   **ppEnumObj
);
```



## <a name="parameters"></a><span data-ttu-id="54b3c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54b3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54b3c-107">*pvSource* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="54b3c-107">*pvSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54b3c-108">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54b3c-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54b3c-109">Source de données.</span><span class="sxs-lookup"><span data-stu-id="54b3c-109">The data source.</span></span> <span data-ttu-id="54b3c-110">Un des deux éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="54b3c-110">Either:</span></span>

-   <span data-ttu-id="54b3c-111">Un nom de fichier</span><span class="sxs-lookup"><span data-stu-id="54b3c-111">A file name</span></span>
-   <span data-ttu-id="54b3c-112">Une structure [**D3DXF \_ FILELOADMEMORY**](d3dxf-fileloadmemory.md)</span><span class="sxs-lookup"><span data-stu-id="54b3c-112">A [**D3DXF\_FILELOADMEMORY**](d3dxf-fileloadmemory.md) structure</span></span>
-   <span data-ttu-id="54b3c-113">Une structure [**D3DXF \_ FILELOADRESOURCE**](d3dxf-fileloadresource.md)</span><span class="sxs-lookup"><span data-stu-id="54b3c-113">A [**D3DXF\_FILELOADRESOURCE**](d3dxf-fileloadresource.md) structure</span></span>

<span data-ttu-id="54b3c-114">En fonction de la valeur de loadflags.</span><span class="sxs-lookup"><span data-stu-id="54b3c-114">Depending on the value of loadflags.</span></span>

</dd> <dt>

<span data-ttu-id="54b3c-115">*loadflags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54b3c-115">*loadflags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54b3c-116">Type : **[D3DXF \_ FILELOADOPTIONS](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="54b3c-116">Type: **[D3DXF\_FILELOADOPTIONS](d3dxf.md)**</span></span>

<span data-ttu-id="54b3c-117">Valeur qui spécifie la source des données.</span><span class="sxs-lookup"><span data-stu-id="54b3c-117">Value that specifies the source of the data.</span></span> <span data-ttu-id="54b3c-118">Cette valeur peut être l’un des indicateurs [D3DXF \_ FILELOADOPTIONS](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="54b3c-118">This value can be one of the [D3DXF\_FILELOADOPTIONS](d3dxf.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="54b3c-119">*ppEnumObj* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="54b3c-119">*ppEnumObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54b3c-120">Type : **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="54b3c-120">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span></span>

<span data-ttu-id="54b3c-121">Adresse d’un pointeur vers une interface [**ID3DXFileEnumObject**](id3dxfileenumobject.md) , représentant l’objet énumérateur créé.</span><span class="sxs-lookup"><span data-stu-id="54b3c-121">Address of a pointer to an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) interface, representing the created enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54b3c-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54b3c-122">Return value</span></span>

<span data-ttu-id="54b3c-123">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54b3c-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54b3c-124">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="54b3c-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="54b3c-125">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.</span><span class="sxs-lookup"><span data-stu-id="54b3c-125">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="54b3c-126">Notes</span><span class="sxs-lookup"><span data-stu-id="54b3c-126">Remarks</span></span>

<span data-ttu-id="54b3c-127">Après l’utilisation de cette méthode, utilisez l’une des méthodes [**ID3DXFileEnumObject**](id3dxfileenumobject.md) pour récupérer un objet de données.</span><span class="sxs-lookup"><span data-stu-id="54b3c-127">After using this method, use one of the [**ID3DXFileEnumObject**](id3dxfileenumobject.md) methods to retrieve a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="54b3c-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54b3c-128">Requirements</span></span>



| <span data-ttu-id="54b3c-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54b3c-129">Requirement</span></span> | <span data-ttu-id="54b3c-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="54b3c-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54b3c-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="54b3c-131">Header</span></span><br/>  | <dl> <span data-ttu-id="54b3c-132"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="54b3c-132"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="54b3c-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="54b3c-133">Library</span></span><br/> | <dl> <span data-ttu-id="54b3c-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54b3c-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="54b3c-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54b3c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54b3c-136">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="54b3c-136">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="54b3c-137">**ID3DXFileEnumObject**</span><span class="sxs-lookup"><span data-stu-id="54b3c-137">**ID3DXFileEnumObject**</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
