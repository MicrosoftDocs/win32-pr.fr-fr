---
description: Crée une instance d’un objet DirectXFile. Action déconseillée.
ms.assetid: c920d480-2557-491d-87ea-7eea1f470498
title: DirectXFileCreate, fonction (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DirectXFileCreate
api_type:
- DllExport
api_location:
- d3dxof.dll
ms.openlocfilehash: 8ee1787941bbb902e6f0f50b082867aaf2f0a8bc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525864"
---
# <a name="directxfilecreate-function"></a><span data-ttu-id="6118a-104">DirectXFileCreate fonction)</span><span class="sxs-lookup"><span data-stu-id="6118a-104">DirectXFileCreate function</span></span>

<span data-ttu-id="6118a-105">Crée une instance d’un objet DirectXFile.</span><span class="sxs-lookup"><span data-stu-id="6118a-105">Creates an instance of a DirectXFile object.</span></span> <span data-ttu-id="6118a-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="6118a-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="6118a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6118a-107">Syntax</span></span>


```C++
HRESULT STDAPICALLTYPE DirectXFileCreate(
   LPDIRECTXFILE *lplpDirectXFile
);
```



## <a name="parameters"></a><span data-ttu-id="6118a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6118a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6118a-109">*lplpDirectXFile*</span><span class="sxs-lookup"><span data-stu-id="6118a-109">*lplpDirectXFile*</span></span> 
</dt> <dd>

<span data-ttu-id="6118a-110">Type : **[ **LPDIRECTXFILE**](idirectxfile.md)\***</span><span class="sxs-lookup"><span data-stu-id="6118a-110">Type: **[**LPDIRECTXFILE**](idirectxfile.md)\***</span></span>

<span data-ttu-id="6118a-111">Adresse d’un pointeur vers une interface [**IDirectXFile**](idirectxfile.md) , représentant l’objet DirectXFile créé.</span><span class="sxs-lookup"><span data-stu-id="6118a-111">Address of a pointer to an [**IDirectXFile**](idirectxfile.md) interface, representing the created DirectXFile object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6118a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6118a-112">Return value</span></span>

<span data-ttu-id="6118a-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6118a-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6118a-114">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6118a-114">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6118a-115">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : DXFILEERR \_ BADALLOC, DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="6118a-115">If the function fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="6118a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="6118a-116">Remarks</span></span>

<span data-ttu-id="6118a-117">Après l’utilisation de cette fonction, utilisez [**RegisterTemplates**](idirectxfile--registertemplates.md) pour inscrire des modèles, [**CreateEnumObject**](idirectxfile--createenumobject.md) pour créer un objet énumérateur ou [**CreateSaveObject**](idirectxfile--createsaveobject.md) pour créer un objet Save.</span><span class="sxs-lookup"><span data-stu-id="6118a-117">After using this function, use [**RegisterTemplates**](idirectxfile--registertemplates.md) to register templates, [**CreateEnumObject**](idirectxfile--createenumobject.md) to create an enumerator object, or [**CreateSaveObject**](idirectxfile--createsaveobject.md) to create a save object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6118a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6118a-118">Requirements</span></span>



| <span data-ttu-id="6118a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6118a-119">Requirement</span></span> | <span data-ttu-id="6118a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6118a-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6118a-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="6118a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6118a-122"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="6118a-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="6118a-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6118a-123">Library</span></span><br/> | <dl> <span data-ttu-id="6118a-124"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6118a-124"><dt>D3dxof.lib</dt></span></span> </dl> |
| <span data-ttu-id="6118a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6118a-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="6118a-126"><dt>D3dxof.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6118a-126"><dt>D3dxof.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6118a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6118a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6118a-128">X, fonctions de fichier</span><span class="sxs-lookup"><span data-stu-id="6118a-128">X File Functions</span></span>](dx9-graphics-reference-x-file-functions.md)
</dt> <dt>

[<span data-ttu-id="6118a-129">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="6118a-129">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="6118a-130">**CreateSaveObject**</span><span class="sxs-lookup"><span data-stu-id="6118a-130">**CreateSaveObject**</span></span>](idirectxfile--createsaveobject.md)
</dt> <dt>

[<span data-ttu-id="6118a-131">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="6118a-131">**RegisterTemplates**</span></span>](idirectxfile--registertemplates.md)
</dt> </dl>

 

 




