---
description: Crée une instance d’un objet ID3DXFile.
ms.assetid: c086cb66-b1dc-4180-b966-e9a3b1f36f22
title: D3DXFileCreate, fonction (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFileCreate
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 36fd57d15257323e86c0068709c3c73662eb0658
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116226"
---
# <a name="d3dxfilecreate-function"></a><span data-ttu-id="49688-103">D3DXFileCreate fonction)</span><span class="sxs-lookup"><span data-stu-id="49688-103">D3DXFileCreate function</span></span>

<span data-ttu-id="49688-104">Crée une instance d’un objet [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="49688-104">Creates an instance of an [**ID3DXFile**](id3dxfile.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="49688-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49688-105">Syntax</span></span>


```C++
HRESULT STDAPICALLTYPE D3DXFileCreate(
   ID3DXFile **lplpDirectXFile
);
```



## <a name="parameters"></a><span data-ttu-id="49688-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49688-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49688-107">*lplpDirectXFile*</span><span class="sxs-lookup"><span data-stu-id="49688-107">*lplpDirectXFile*</span></span> 
</dt> <dd>

<span data-ttu-id="49688-108">Type : **[ **ID3DXFile**](id3dxfile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="49688-108">Type: **[**ID3DXFile**](id3dxfile.md)\*\***</span></span>

<span data-ttu-id="49688-109">Adresse d’un pointeur vers une interface [**ID3DXFile**](id3dxfile.md) , représentant l’objet fichier. x créé.</span><span class="sxs-lookup"><span data-stu-id="49688-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) interface, representing the created .x file object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49688-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49688-110">Return value</span></span>

<span data-ttu-id="49688-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="49688-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="49688-112">Si la fonction est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="49688-112">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="49688-113">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : \_ pointeur e, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="49688-113">If the function fails, the return value can be one of the following: E\_POINTER, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="49688-114">Notes</span><span class="sxs-lookup"><span data-stu-id="49688-114">Remarks</span></span>

<span data-ttu-id="49688-115">Après l’utilisation de cette fonction, utilisez [**RegisterTemplates**](id3dxfile--registertemplates.md) ou [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) pour inscrire des modèles, [**CreateEnumObject**](id3dxfile--createenumobject.md) pour créer un objet énumérateur ou [**CreateSaveObject**](id3dxfile--createsaveobject.md) pour créer un objet Save.</span><span class="sxs-lookup"><span data-stu-id="49688-115">After using this function, use [**RegisterTemplates**](id3dxfile--registertemplates.md) or [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) to register templates, [**CreateEnumObject**](id3dxfile--createenumobject.md) to create an enumerator object, or [**CreateSaveObject**](id3dxfile--createsaveobject.md) to create a save object.</span></span>

## <a name="requirements"></a><span data-ttu-id="49688-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49688-116">Requirements</span></span>



| <span data-ttu-id="49688-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49688-117">Requirement</span></span> | <span data-ttu-id="49688-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="49688-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49688-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="49688-119">Header</span></span><br/>  | <dl> <span data-ttu-id="49688-120"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="49688-120"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="49688-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="49688-121">Library</span></span><br/> | <dl> <span data-ttu-id="49688-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49688-122"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="49688-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49688-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49688-124">Fonctions de fichier D3DX X</span><span class="sxs-lookup"><span data-stu-id="49688-124">D3DX X File Functions</span></span>](dx9-graphics-reference-d3dx-x-file-functions.md)
</dt> <dt>

[<span data-ttu-id="49688-125">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="49688-125">**CreateEnumObject**</span></span>](id3dxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="49688-126">**CreateSaveObject**</span><span class="sxs-lookup"><span data-stu-id="49688-126">**CreateSaveObject**</span></span>](id3dxfile--createsaveobject.md)
</dt> <dt>

[<span data-ttu-id="49688-127">**RegisterEnumTemplates**</span><span class="sxs-lookup"><span data-stu-id="49688-127">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md)
</dt> <dt>

[<span data-ttu-id="49688-128">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="49688-128">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




