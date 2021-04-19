---
description: Crée un objet Save. Action déconseillée.
ms.assetid: 50a7dbde-1dd4-4aae-a9ab-97d6f99618c0
title: 'IDirectXFile :: CreateSaveObject, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 848010a1f701b39f5cc77a126272bc019ed01f4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523222"
---
# <a name="idirectxfilecreatesaveobject-method"></a><span data-ttu-id="0945c-104">IDirectXFile :: CreateSaveObject, méthode</span><span class="sxs-lookup"><span data-stu-id="0945c-104">IDirectXFile::CreateSaveObject method</span></span>

<span data-ttu-id="0945c-105">Crée un objet Save.</span><span class="sxs-lookup"><span data-stu-id="0945c-105">Creates a save object.</span></span> <span data-ttu-id="0945c-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0945c-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="0945c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0945c-107">Syntax</span></span>


```C++
HRESULT CreateSaveObject(
  [in]          LPCSTR                  szFileName,
  [in]          DXFILEFORMAT            dwFileFormat,
  [out, retval] LPDIRECTXFILESAVEOBJECT *ppSaveObj
);
```



## <a name="parameters"></a><span data-ttu-id="0945c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0945c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0945c-109">*szFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0945c-109">*szFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0945c-110">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0945c-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0945c-111">Pointeur vers le nom du fichier à utiliser pour enregistrer les données.</span><span class="sxs-lookup"><span data-stu-id="0945c-111">Pointer to the name of the file to use for saving data.</span></span>

</dd> <dt>

<span data-ttu-id="0945c-112">*dwFileFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0945c-112">*dwFileFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0945c-113">Type : **[ **DXFILEFORMAT**](dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="0945c-113">Type: **[**DXFILEFORMAT**](dxfile.md)**</span></span>

<span data-ttu-id="0945c-114">Indique le format à utiliser lors de l’enregistrement du fichier DirectX.</span><span class="sxs-lookup"><span data-stu-id="0945c-114">Indicates the format to use when saving the DirectX file.</span></span> <span data-ttu-id="0945c-115">Cette valeur peut être l’un des \_ indicateurs DXFILEFORMAT xxx dans les [constantes DXFILE](dxfile.md).</span><span class="sxs-lookup"><span data-stu-id="0945c-115">This value can be one of the DXFILEFORMAT\_xxx flags in [DXFILE Constants](dxfile.md).</span></span> <span data-ttu-id="0945c-116">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="0945c-116">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0945c-117">*ppSaveObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0945c-117">*ppSaveObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0945c-118">Type : **[ **LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="0945c-118">Type: **[**LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***</span></span>

<span data-ttu-id="0945c-119">Adresse d’un pointeur vers une interface [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) , représentant l’objet Save créé.</span><span class="sxs-lookup"><span data-stu-id="0945c-119">Address of a pointer to an [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interface, representing the created save object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0945c-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0945c-120">Return value</span></span>

<span data-ttu-id="0945c-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0945c-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0945c-122">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0945c-122">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="0945c-123">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : DXFILEERR \_ BADALLOC, DXFILEERR \_ BadFile, DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="0945c-123">If the method fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADFILE, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="0945c-124">Notes</span><span class="sxs-lookup"><span data-stu-id="0945c-124">Remarks</span></span>

<span data-ttu-id="0945c-125">Après l’utilisation de cette méthode, utilisez les méthodes de l’interface [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) pour créer des objets de données et enregistrer des modèles ou des données.</span><span class="sxs-lookup"><span data-stu-id="0945c-125">After using this method, use methods of the [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interface to create data objects and to save templates or data.</span></span>

<span data-ttu-id="0945c-126">La valeur par défaut pour le format de fichier est DXFILEFORMAT \_ binaire.</span><span class="sxs-lookup"><span data-stu-id="0945c-126">The default value for the file format is DXFILEFORMAT\_BINARY.</span></span> <span data-ttu-id="0945c-127">Les valeurs de format de fichier peuvent être combinées dans un ou logique pour créer du texte compressé ou des fichiers binaires compressés.</span><span class="sxs-lookup"><span data-stu-id="0945c-127">The file format values can be combined in a logical OR to create compressed text or compressed binary files.</span></span> <span data-ttu-id="0945c-128">Si un fichier est spécifié à la fois comme binaire (0) et texte (1), il est enregistré en tant que fichier texte, car la valeur ne peut pas être différenciée de la valeur de format de fichier texte (0 + 1 = 1).</span><span class="sxs-lookup"><span data-stu-id="0945c-128">If a file is specified as both binary (0) and text (1), it will be saved as a text file because the value will be indistinguishable from the text file format value (0 + 1 = 1).</span></span> <span data-ttu-id="0945c-129">Si vous indiquez que le format de fichier doit être texte et compressé, le fichier est d’abord écrit sous forme de texte, puis compressé.</span><span class="sxs-lookup"><span data-stu-id="0945c-129">If you indicate that the file format should be text and compressed, the file will first be written out as text and then compressed.</span></span> <span data-ttu-id="0945c-130">Toutefois, les fichiers texte compressés ne sont pas aussi efficaces que les fichiers texte binaires. par conséquent, dans la plupart des cas, vous devez indiquer binary et Compressed.</span><span class="sxs-lookup"><span data-stu-id="0945c-130">However, compressed text files are not as efficient as binary text files, so in most cases you will want to indicate binary and compressed.</span></span> <span data-ttu-id="0945c-131">La définition d’un fichier à compresser sans spécifier de format entraînera un fichier binaire et compressé.</span><span class="sxs-lookup"><span data-stu-id="0945c-131">Setting a file to be compressed without specifying a format will result in a binary, compressed file.</span></span>

## <a name="requirements"></a><span data-ttu-id="0945c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0945c-132">Requirements</span></span>



| <span data-ttu-id="0945c-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0945c-133">Requirement</span></span> | <span data-ttu-id="0945c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="0945c-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0945c-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="0945c-135">Header</span></span><br/>  | <dl> <span data-ttu-id="0945c-136"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="0945c-136"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="0945c-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0945c-137">Library</span></span><br/> | <dl> <span data-ttu-id="0945c-138"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0945c-138"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0945c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0945c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0945c-140">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="0945c-140">IDirectXFile</span></span>](idirectxfile.md)
</dt> <dt>

[<span data-ttu-id="0945c-141">**IDirectXFileSaveObject**</span><span class="sxs-lookup"><span data-stu-id="0945c-141">**IDirectXFileSaveObject**</span></span>](idirectxfilesaveobject.md)
</dt> </dl>

 

 
