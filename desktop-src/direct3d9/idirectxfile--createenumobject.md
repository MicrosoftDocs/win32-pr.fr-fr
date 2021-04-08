---
description: Crée un objet énumérateur. Action déconseillée.
ms.assetid: 9e72bb2f-143e-4690-baef-ccded21572ec
title: 'IDirectXFile :: CreateEnumObject, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3d15738b78299441fe08333a41f0652f1b4224d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762248"
---
# <a name="idirectxfilecreateenumobject-method"></a><span data-ttu-id="4cdd4-104">IDirectXFile :: CreateEnumObject, méthode</span><span class="sxs-lookup"><span data-stu-id="4cdd4-104">IDirectXFile::CreateEnumObject method</span></span>

<span data-ttu-id="4cdd4-105">Crée un objet énumérateur.</span><span class="sxs-lookup"><span data-stu-id="4cdd4-105">Creates an enumerator object.</span></span> <span data-ttu-id="4cdd4-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="4cdd4-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cdd4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cdd4-107">Syntax</span></span>


```C++
HRESULT CreateEnumObject(
  [in]          LPVOID                  pvSource,
  [in]          DXFILELOADOPTIONS       dwLoadOptions,
  [out, retval] LPDIRECTXFILEENUMOBJECT *ppEnumObj
);
```



## <a name="parameters"></a><span data-ttu-id="4cdd4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4cdd4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cdd4-109">*pvSource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4cdd4-109">*pvSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cdd4-110">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4cdd4-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4cdd4-111">Pointeur vers des données dont le contenu dépend de la valeur de dwLoadOptions</span><span class="sxs-lookup"><span data-stu-id="4cdd4-111">Pointer to data whose contents depend on the value of dwLoadOptions</span></span>

</dd> <dt>

<span data-ttu-id="4cdd4-112">*dwLoadOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4cdd4-112">*dwLoadOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cdd4-113">Type : **[ **DXFILELOADOPTIONS**](dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="4cdd4-113">Type: **[**DXFILELOADOPTIONS**](dxfile.md)**</span></span>

<span data-ttu-id="4cdd4-114">Valeur qui spécifie la source des données.</span><span class="sxs-lookup"><span data-stu-id="4cdd4-114">Value that specifies the source of the data.</span></span> <span data-ttu-id="4cdd4-115">Cette valeur peut être l’un des \_ indicateurs DXFILELOAD xxx dans les [constantes DXFILE](dxfile.md).</span><span class="sxs-lookup"><span data-stu-id="4cdd4-115">This value can be one of the DXFILELOAD\_xxx flags in [DXFILE Constants](dxfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="4cdd4-116">*ppEnumObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4cdd4-116">*ppEnumObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4cdd4-117">Type : **[ **LPDIRECTXFILEENUMOBJECT**](idirectxfileenumobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="4cdd4-117">Type: **[**LPDIRECTXFILEENUMOBJECT**](idirectxfileenumobject.md)\***</span></span>

<span data-ttu-id="4cdd4-118">Adresse d’un pointeur vers une interface [**IDirectXFileEnumObject**](idirectxfileenumobject.md) , représentant l’objet énumérateur créé.</span><span class="sxs-lookup"><span data-stu-id="4cdd4-118">Address of a pointer to an [**IDirectXFileEnumObject**](idirectxfileenumobject.md) interface, representing the created enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cdd4-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4cdd4-119">Return value</span></span>

<span data-ttu-id="4cdd4-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4cdd4-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4cdd4-121">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4cdd4-121">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="4cdd4-122">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : DXFILEERR \_ BADALLOC, DXFILEERR \_ BADFILEFLOATSIZE, DXFILEERR \_ BADFILETYPE, DXFILEERR \_ BADFILEVERSION, DXFILEERR \_ BADRESOURCE, DXFILEERR \_ BADVALUE, DXFILEERR \_ FILENOTFOUND, DXFILEERR \_ RESOURCENOTFOUND, DXFILEERR \_ URLNOTFOUND.</span><span class="sxs-lookup"><span data-stu-id="4cdd4-122">If the method fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADFILEFLOATSIZE, DXFILEERR\_BADFILETYPE, DXFILEERR\_BADFILEVERSION, DXFILEERR\_BADRESOURCE, DXFILEERR\_BADVALUE, DXFILEERR\_FILENOTFOUND, DXFILEERR\_RESOURCENOTFOUND, DXFILEERR\_URLNOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cdd4-123">Notes</span><span class="sxs-lookup"><span data-stu-id="4cdd4-123">Remarks</span></span>

<span data-ttu-id="4cdd4-124">Après l’utilisation de cette méthode, utilisez l’une des méthodes IDirectXFileEnumObject pour récupérer un objet de données.</span><span class="sxs-lookup"><span data-stu-id="4cdd4-124">After using this method, use one of the IDirectXFileEnumObject methods to retrieve a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cdd4-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4cdd4-125">Requirements</span></span>



| <span data-ttu-id="4cdd4-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4cdd4-126">Requirement</span></span> | <span data-ttu-id="4cdd4-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cdd4-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cdd4-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="4cdd4-128">Header</span></span><br/>  | <dl> <span data-ttu-id="4cdd4-129"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cdd4-129"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="4cdd4-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4cdd4-130">Library</span></span><br/> | <dl> <span data-ttu-id="4cdd4-131"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cdd4-131"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cdd4-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cdd4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cdd4-133">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="4cdd4-133">IDirectXFile</span></span>](idirectxfile.md)
</dt> </dl>

 

 
