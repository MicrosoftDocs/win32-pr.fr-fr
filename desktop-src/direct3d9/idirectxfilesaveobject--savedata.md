---
description: Enregistre un objet de données et ses enfants dans un fichier DirectX. Action déconseillée.
ms.assetid: 18bd5ef6-9e17-4c21-bc14-373de8df9ffb
title: 'IDirectXFileSaveObject :: SaveData, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: cb901bd984e1fcd923d0ea172fb5f387b3a9302a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538508"
---
# <a name="idirectxfilesaveobjectsavedata-method"></a><span data-ttu-id="e0586-104">IDirectXFileSaveObject :: SaveData, méthode</span><span class="sxs-lookup"><span data-stu-id="e0586-104">IDirectXFileSaveObject::SaveData method</span></span>

<span data-ttu-id="e0586-105">Enregistre un objet de données et ses enfants dans un fichier DirectX.</span><span class="sxs-lookup"><span data-stu-id="e0586-105">Saves a data object and its children to a DirectX file.</span></span> <span data-ttu-id="e0586-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e0586-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0586-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0586-107">Syntax</span></span>


```C++
HRESULT SaveData(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="e0586-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0586-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0586-109">*pDataObj* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e0586-109">*pDataObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0586-110">Type : **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="e0586-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span></span>

<span data-ttu-id="e0586-111">Pointeur vers une interface [**IDirectXFileData**](idirectxfiledata.md) , représentant l’objet de données de fichier à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="e0586-111">Pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the file data object to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0586-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e0586-112">Return value</span></span>

<span data-ttu-id="e0586-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0586-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0586-114">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e0586-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="e0586-115">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : DXFILEERR \_ BADARRAYSIZE, DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="e0586-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADARRAYSIZE, DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0586-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0586-116">Requirements</span></span>



| <span data-ttu-id="e0586-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0586-117">Requirement</span></span> | <span data-ttu-id="e0586-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0586-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0586-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="e0586-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e0586-120"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0586-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0586-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e0586-121">Library</span></span><br/> | <dl> <span data-ttu-id="e0586-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0586-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0586-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0586-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0586-124">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="e0586-124">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> </dl>

 

 




