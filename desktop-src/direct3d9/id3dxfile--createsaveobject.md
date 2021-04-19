---
description: Crée un objet Save qui sera utilisé pour enregistrer des données dans un fichier. x.
ms.assetid: da064e83-605f-4c86-985d-9a0961c18e01
title: 'ID3DXFile :: CreateSaveObject, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d7c5b3de020ad50abfd8834aabbdc8e6e848d71d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523204"
---
# <a name="id3dxfilecreatesaveobject-method"></a><span data-ttu-id="81bfb-103">ID3DXFile :: CreateSaveObject, méthode</span><span class="sxs-lookup"><span data-stu-id="81bfb-103">ID3DXFile::CreateSaveObject method</span></span>

<span data-ttu-id="81bfb-104">Crée un objet Save qui sera utilisé pour enregistrer des données dans un fichier. x.</span><span class="sxs-lookup"><span data-stu-id="81bfb-104">Creates a save object that will be used to save data to a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="81bfb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81bfb-105">Syntax</span></span>


```C++
HRESULT CreateSaveObject(
  [in]  LPCVOID               pData,
  [in]  D3DXF_FILESAVEOPTIONS flags,
  [in]  D3DXF_FILEFORMAT      dwFileFormat,
  [out] ID3DXFileSaveObject   **ppSaveObj
);
```



## <a name="parameters"></a><span data-ttu-id="81bfb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81bfb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81bfb-107">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81bfb-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81bfb-108">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81bfb-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81bfb-109">Pointeur vers le nom du fichier à utiliser pour enregistrer les données.</span><span class="sxs-lookup"><span data-stu-id="81bfb-109">Pointer to the name of the file to use for saving data.</span></span>

</dd> <dt>

<span data-ttu-id="81bfb-110">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81bfb-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81bfb-111">Type : **[D3DXF \_ FILESAVEOPTIONS](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="81bfb-111">Type: **[D3DXF\_FILESAVEOPTIONS](d3dxf.md)**</span></span>

<span data-ttu-id="81bfb-112">Valeur qui spécifie le nom du fichier dans lequel les données doivent être enregistrées.</span><span class="sxs-lookup"><span data-stu-id="81bfb-112">Value that specifies the name of the file to which data is to be saved.</span></span> <span data-ttu-id="81bfb-113">Cette valeur peut être l’un des indicateurs d' [options d’enregistrement de fichier](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="81bfb-113">This value can be one of the [File Save Options](d3dxf.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="81bfb-114">*dwFileFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81bfb-114">*dwFileFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81bfb-115">Type : **[D3DXF \_ FILEFORMAT](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="81bfb-115">Type: **[D3DXF\_FILEFORMAT](d3dxf.md)**</span></span>

<span data-ttu-id="81bfb-116">Indique le format à utiliser lors de l’enregistrement du fichier. x.</span><span class="sxs-lookup"><span data-stu-id="81bfb-116">Indicates the format to use when saving the .x file.</span></span> <span data-ttu-id="81bfb-117">Cette valeur peut être l’un des indicateurs de [formats de fichier](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="81bfb-117">This value can be one of the [File Formats](d3dxf.md) flags.</span></span> <span data-ttu-id="81bfb-118">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="81bfb-118">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="81bfb-119">*ppSaveObj* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="81bfb-119">*ppSaveObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81bfb-120">Type : **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="81bfb-120">Type: **[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span></span>

<span data-ttu-id="81bfb-121">Adresse d’un pointeur vers une interface [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) , représentant l’objet Save créé.</span><span class="sxs-lookup"><span data-stu-id="81bfb-121">Address of a pointer to an [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface, representing the created save object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81bfb-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81bfb-122">Return value</span></span>

<span data-ttu-id="81bfb-123">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="81bfb-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="81bfb-124">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="81bfb-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="81bfb-125">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.</span><span class="sxs-lookup"><span data-stu-id="81bfb-125">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="81bfb-126">Notes</span><span class="sxs-lookup"><span data-stu-id="81bfb-126">Remarks</span></span>

<span data-ttu-id="81bfb-127">Après l’utilisation de cette méthode, utilisez les méthodes de l’interface [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) pour créer des objets de données et enregistrer des modèles ou des données.</span><span class="sxs-lookup"><span data-stu-id="81bfb-127">After using this method, use methods of the [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface to create data objects and to save templates or data.</span></span>

<span data-ttu-id="81bfb-128">Pour le format de fichier enregistré *dwFileFormat*, l’un des indicateurs binaires, binaires hérités ou de texte dans les [formats de fichier](d3dxf.md) doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="81bfb-128">For the saved file format *dwFileFormat*, one of the binary, legacy binary, or text flags in [File Formats](d3dxf.md) must be specified.</span></span> <span data-ttu-id="81bfb-129">Le fichier peut être compressé à l’aide de l' \_ indicateur de compression D3DXF FILEFORMAT facultatif \_ .</span><span class="sxs-lookup"><span data-stu-id="81bfb-129">The file can be compressed by using the optional D3DXF\_FILEFORMAT\_COMPRESSED flag.</span></span>

<span data-ttu-id="81bfb-130">Les valeurs de format de fichier peuvent être combinées dans un ou logique pour créer du texte compressé ou des fichiers binaires compressés.</span><span class="sxs-lookup"><span data-stu-id="81bfb-130">The file format values can be combined in a logical OR to create compressed text or compressed binary files.</span></span> <span data-ttu-id="81bfb-131">Si vous indiquez que le format de fichier doit être texte et compressé, le fichier est écrit en premier sous forme de texte, puis compressé.</span><span class="sxs-lookup"><span data-stu-id="81bfb-131">If you indicate that the file format should be text and compressed, the file will be written out first as text and then compressed.</span></span> <span data-ttu-id="81bfb-132">Toutefois, les fichiers texte compressés ne sont pas aussi efficaces que les fichiers texte binaires ; dans la plupart des cas, vous souhaiterez donc indiquer binaire et compressé.</span><span class="sxs-lookup"><span data-stu-id="81bfb-132">However, compressed text files are not as efficient as binary text files; in most cases, therefore, you will want to indicate binary and compressed.</span></span>

## <a name="requirements"></a><span data-ttu-id="81bfb-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81bfb-133">Requirements</span></span>



| <span data-ttu-id="81bfb-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81bfb-134">Requirement</span></span> | <span data-ttu-id="81bfb-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="81bfb-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81bfb-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="81bfb-136">Header</span></span><br/>  | <dl> <span data-ttu-id="81bfb-137"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="81bfb-137"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="81bfb-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="81bfb-138">Library</span></span><br/> | <dl> <span data-ttu-id="81bfb-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81bfb-139"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="81bfb-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81bfb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81bfb-141">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="81bfb-141">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="81bfb-142">**ID3DXFileSaveObject**</span><span class="sxs-lookup"><span data-stu-id="81bfb-142">**ID3DXFileSaveObject**</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 
