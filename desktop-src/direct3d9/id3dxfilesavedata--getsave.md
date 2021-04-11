---
description: Récupère un pointeur vers ce nœud de données de fichier ID3DXFileSaveObject.
ms.assetid: 092d1c6f-0a53-4b8e-84ec-bc76f3f647ac
title: 'ID3DXFileSaveData :: GetSave, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetSave
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4e23296ad0a866a0ad289a9a587c433411ef9bb8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211939"
---
# <a name="id3dxfilesavedatagetsave-method"></a><span data-ttu-id="79791-103">ID3DXFileSaveData :: GetSave, méthode</span><span class="sxs-lookup"><span data-stu-id="79791-103">ID3DXFileSaveData::GetSave method</span></span>

<span data-ttu-id="79791-104">Récupère un pointeur vers ce nœud de données de fichier [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="79791-104">Retrieves a pointer to this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="79791-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79791-105">Syntax</span></span>


```C++
HRESULT GetSave(
  [out] ID3DXFileSaveObject **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="79791-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79791-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79791-107">*ppObj* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="79791-107">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79791-108">Type : **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="79791-108">Type: **[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span></span>

<span data-ttu-id="79791-109">Adresse d’un pointeur vers une interface [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) représentant ce nœud de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="79791-109">Address of a pointer to an [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface representing this file data node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79791-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="79791-110">Return value</span></span>

<span data-ttu-id="79791-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79791-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79791-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="79791-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="79791-113">Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="79791-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="79791-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79791-114">Requirements</span></span>



| <span data-ttu-id="79791-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79791-115">Requirement</span></span> | <span data-ttu-id="79791-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="79791-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79791-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="79791-117">Header</span></span><br/>  | <dl> <span data-ttu-id="79791-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="79791-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="79791-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="79791-119">Library</span></span><br/> | <dl> <span data-ttu-id="79791-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79791-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="79791-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79791-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79791-122">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="79791-122">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




