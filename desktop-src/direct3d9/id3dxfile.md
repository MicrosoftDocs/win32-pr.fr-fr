---
description: Les applications utilisent les méthodes de l’interface ID3DXFile pour créer des instances des interfaces ID3DXFileEnumObject et ID3DXFileSaveObject, et pour inscrire des modèles.
ms.assetid: 472d45b1-5c03-4417-a005-91f802667919
title: Interface ID3DXFile (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 45af79c4fb01c95b25803788f79588a3880fe264
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539894"
---
# <a name="id3dxfile-interface"></a><span data-ttu-id="db06f-103">Interface ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="db06f-103">ID3DXFile interface</span></span>

<span data-ttu-id="db06f-104">Les applications utilisent les méthodes de l’interface ID3DXFile pour créer des instances des interfaces [**ID3DXFileEnumObject**](id3dxfileenumobject.md) et [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) , et pour inscrire des modèles.</span><span class="sxs-lookup"><span data-stu-id="db06f-104">Applications use the methods of the ID3DXFile interface to create instances of the [**ID3DXFileEnumObject**](id3dxfileenumobject.md) and [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interfaces, and to register templates.</span></span>

## <a name="members"></a><span data-ttu-id="db06f-105">Membres</span><span class="sxs-lookup"><span data-stu-id="db06f-105">Members</span></span>

<span data-ttu-id="db06f-106">L’interface **ID3DXFile** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="db06f-106">The **ID3DXFile** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="db06f-107">**ID3DXFile** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="db06f-107">**ID3DXFile** also has these types of members:</span></span>

-   [<span data-ttu-id="db06f-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="db06f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="db06f-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="db06f-109">Methods</span></span>

<span data-ttu-id="db06f-110">L’interface **ID3DXFile** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="db06f-110">The **ID3DXFile** interface has these methods.</span></span>



| <span data-ttu-id="db06f-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="db06f-111">Method</span></span>                                                            | <span data-ttu-id="db06f-112">Description</span><span class="sxs-lookup"><span data-stu-id="db06f-112">Description</span></span>                                                                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db06f-113">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="db06f-113">**CreateEnumObject**</span></span>](id3dxfile--createenumobject.md)           | <span data-ttu-id="db06f-114">Crée un objet énumérateur qui lira un fichier. x.</span><span class="sxs-lookup"><span data-stu-id="db06f-114">Creates an enumerator object that will read a .x file.</span></span><br/>                                                      |
| [<span data-ttu-id="db06f-115">**CreateSaveObject**</span><span class="sxs-lookup"><span data-stu-id="db06f-115">**CreateSaveObject**</span></span>](id3dxfile--createsaveobject.md)           | <span data-ttu-id="db06f-116">Crée un objet Save qui sera utilisé pour enregistrer des données dans un fichier. x.</span><span class="sxs-lookup"><span data-stu-id="db06f-116">Creates a save object that will be used to save data to a .x file.</span></span><br/>                                          |
| [<span data-ttu-id="db06f-117">**RegisterEnumTemplates**</span><span class="sxs-lookup"><span data-stu-id="db06f-117">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md) | <span data-ttu-id="db06f-118">Inscrit des modèles personnalisés, à partir d’un objet d’énumération [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="db06f-118">Registers custom templates, given an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object.</span></span><br/> |
| [<span data-ttu-id="db06f-119">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="db06f-119">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)         | <span data-ttu-id="db06f-120">Inscrit des modèles personnalisés.</span><span class="sxs-lookup"><span data-stu-id="db06f-120">Registers custom templates.</span></span><br/>                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="db06f-121">Notes</span><span class="sxs-lookup"><span data-stu-id="db06f-121">Remarks</span></span>

<span data-ttu-id="db06f-122">Un objet ID3DXFile contient également un magasin de modèles local.</span><span class="sxs-lookup"><span data-stu-id="db06f-122">An ID3DXFile object also contains a local template store.</span></span> <span data-ttu-id="db06f-123">Ce stockage local peut être ajouté à uniquement avec les méthodes [**ID3DXFile :: RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) et [**ID3DXFile :: RegisterTemplates**](id3dxfile--registertemplates.md) .</span><span class="sxs-lookup"><span data-stu-id="db06f-123">This local storage may be added to only with the [**ID3DXFile::RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) and [**ID3DXFile::RegisterTemplates**](id3dxfile--registertemplates.md) methods.</span></span>

<span data-ttu-id="db06f-124">Les objets [**ID3DXFileEnumObject**](id3dxfileenumobject.md) et [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) créés avec [**ID3DXFile :: CreateEnumObject**](id3dxfile--createenumobject.md) et [**ID3DXFile :: CreateSaveObject**](id3dxfile--createsaveobject.md) utilisent également le magasin de modèles de l’objet ID3DXFile parent.</span><span class="sxs-lookup"><span data-stu-id="db06f-124">[**ID3DXFileEnumObject**](id3dxfileenumobject.md) and [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) objects created with [**ID3DXFile::CreateEnumObject**](id3dxfile--createenumobject.md) and [**ID3DXFile::CreateSaveObject**](id3dxfile--createsaveobject.md) also utilize the template store of the parent ID3DXFile object.</span></span>

<span data-ttu-id="db06f-125">L’interface ID3DXFile est obtenue en appelant la fonction [**D3DXFileCreate**](d3dxfilecreate.md) .</span><span class="sxs-lookup"><span data-stu-id="db06f-125">The ID3DXFile interface is obtained by calling the [**D3DXFileCreate**](d3dxfilecreate.md) function.</span></span>

<span data-ttu-id="db06f-126">L’identificateur global unique (GUID) de l’interface ID3DXFile est IID \_ ID3DXFile.</span><span class="sxs-lookup"><span data-stu-id="db06f-126">The globally unique identifier (GUID) for the ID3DXFile interface is IID\_ID3DXFile.</span></span>

<span data-ttu-id="db06f-127">Le type LPD3DXFILE est défini comme un pointeur vers l’interface ID3DXFile.</span><span class="sxs-lookup"><span data-stu-id="db06f-127">The LPD3DXFILE type is defined as a pointer to the ID3DXFile interface.</span></span>


```
typedef interface ID3DXFile *LPD3DXFILE;
```



## <a name="requirements"></a><span data-ttu-id="db06f-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db06f-128">Requirements</span></span>



| <span data-ttu-id="db06f-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db06f-129">Requirement</span></span> | <span data-ttu-id="db06f-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="db06f-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db06f-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="db06f-131">Header</span></span><br/>  | <dl> <span data-ttu-id="db06f-132"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="db06f-132"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="db06f-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="db06f-133">Library</span></span><br/> | <dl> <span data-ttu-id="db06f-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db06f-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="db06f-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db06f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db06f-136">Interfaces de fichiers D3DX X</span><span class="sxs-lookup"><span data-stu-id="db06f-136">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
