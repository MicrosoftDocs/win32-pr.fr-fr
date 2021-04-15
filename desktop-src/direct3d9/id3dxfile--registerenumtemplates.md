---
description: Inscrit des modèles personnalisés, à partir d’un objet d’énumération ID3DXFileEnumObject.
ms.assetid: 1b0c71db-639b-4836-8a65-7d0a2ed3ba4f
title: 'ID3DXFile :: RegisterEnumTemplates, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterEnumTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 89a8b136bdc0e202fc87ba8fd4d7f013203814eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394179"
---
# <a name="id3dxfileregisterenumtemplates-method"></a><span data-ttu-id="e8af1-103">ID3DXFile :: RegisterEnumTemplates, méthode</span><span class="sxs-lookup"><span data-stu-id="e8af1-103">ID3DXFile::RegisterEnumTemplates method</span></span>

<span data-ttu-id="e8af1-104">Inscrit des modèles personnalisés, à partir d’un objet d’énumération [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="e8af1-104">Registers custom templates, given an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8af1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8af1-105">Syntax</span></span>


```C++
HRESULT RegisterEnumTemplates(
  [in] ID3DXFileEnumObject *pEnum
);
```



## <a name="parameters"></a><span data-ttu-id="e8af1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8af1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8af1-107">*pEnum* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e8af1-107">*pEnum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8af1-108">Type : **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="e8af1-108">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\***</span></span>

<span data-ttu-id="e8af1-109">Pointeur vers un objet d’énumération [**ID3DXFileEnumObject**](id3dxfileenumobject.md) qui contient des modèles.</span><span class="sxs-lookup"><span data-stu-id="e8af1-109">Pointer to an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object that contains templates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8af1-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e8af1-110">Return value</span></span>

<span data-ttu-id="e8af1-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e8af1-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e8af1-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e8af1-112">If the method succeeds, the return value is S\_OK .</span></span>

<span data-ttu-id="e8af1-113">Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="e8af1-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8af1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e8af1-114">Remarks</span></span>

<span data-ttu-id="e8af1-115">Lorsque cette méthode est appelée, elle copie les modèles stockés avec ID3DXFileEnumObject, représentant le fichier, dans le magasin de modèles local de l’objet [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="e8af1-115">When this method is called, it copies templates stored with the ID3DXFileEnumObject, representing the file, to the local template store of the [**ID3DXFile**](id3dxfile.md) object.</span></span>

<span data-ttu-id="e8af1-116">Si un pointeur [**ID3DXFileEnumObject**](id3dxfileenumobject.md) n’est pas disponible, appelez la méthode [**RegisterTemplates**](id3dxfile--registertemplates.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="e8af1-116">If an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) pointer is not available, call the [**RegisterTemplates**](id3dxfile--registertemplates.md) method instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8af1-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8af1-117">Requirements</span></span>



| <span data-ttu-id="e8af1-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8af1-118">Requirement</span></span> | <span data-ttu-id="e8af1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8af1-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8af1-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8af1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e8af1-121"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8af1-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="e8af1-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e8af1-122">Library</span></span><br/> | <dl> <span data-ttu-id="e8af1-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8af1-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e8af1-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8af1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8af1-125">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="e8af1-125">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="e8af1-126">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="e8af1-126">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




