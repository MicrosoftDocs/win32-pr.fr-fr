---
description: Enregistre un objet de données et ses enfants dans un fichier. x sur le disque.
ms.assetid: a48cd1b2-d1e7-446b-8482-485ccdd59353
title: 'ID3DXFileSaveObject :: Save, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.Save
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c97c2ccf6c509aec1d217e3179c927fe2bb5a797
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394124"
---
# <a name="id3dxfilesaveobjectsave-method"></a><span data-ttu-id="e2551-103">ID3DXFileSaveObject :: Save, méthode</span><span class="sxs-lookup"><span data-stu-id="e2551-103">ID3DXFileSaveObject::Save method</span></span>

<span data-ttu-id="e2551-104">Enregistre un objet de données et ses enfants dans un fichier. x sur le disque.</span><span class="sxs-lookup"><span data-stu-id="e2551-104">Saves a data object and its children to a .x file on disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2551-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2551-105">Syntax</span></span>


```C++
HRESULT Save();
```



## <a name="parameters"></a><span data-ttu-id="e2551-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2551-106">Parameters</span></span>

<span data-ttu-id="e2551-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e2551-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e2551-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e2551-108">Return value</span></span>

<span data-ttu-id="e2551-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e2551-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e2551-110">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e2551-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e2551-111">Si la méthode échoue, la valeur de retour peut être la suivante : D3DXFERR \_ BADOBJECT.</span><span class="sxs-lookup"><span data-stu-id="e2551-111">If the method fails, the return value can be the following: D3DXFERR\_BADOBJECT.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2551-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e2551-112">Remarks</span></span>

<span data-ttu-id="e2551-113">Une fois cette méthode réussie, [**ID3DXFileSaveObject :: AddDataObject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData :: AddDataObject**](id3dxfilesavedata--adddataobject.md) et [**ID3DXFileSaveData :: AddDataReference**](id3dxfilesavedata--adddatareference.md) ne peuvent plus être appelés jusqu’à la création d’un nouvel objet [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="e2551-113">After this method succeeds, [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) and [**ID3DXFileSaveData::AddDataReference**](id3dxfilesavedata--adddatareference.md) can no longer be called until a new [**ID3DXFile**](id3dxfile.md) object is created.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2551-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2551-114">Requirements</span></span>



| <span data-ttu-id="e2551-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2551-115">Requirement</span></span> | <span data-ttu-id="e2551-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2551-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2551-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2551-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e2551-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2551-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="e2551-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e2551-119">Library</span></span><br/> | <dl> <span data-ttu-id="e2551-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2551-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e2551-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2551-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2551-122">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="e2551-122">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 




