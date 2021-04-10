---
description: Récupère l’objet ID3DXFile.
ms.assetid: 832878c6-73a4-400a-af30-57112b172977
title: 'ID3DXFileEnumObject :: GetFile, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d3b5d672ca9b462e08c75a6f3352b01b07ead43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953906"
---
# <a name="id3dxfileenumobjectgetfile-method"></a><span data-ttu-id="80a6d-103">ID3DXFileEnumObject :: GetFile, méthode</span><span class="sxs-lookup"><span data-stu-id="80a6d-103">ID3DXFileEnumObject::GetFile method</span></span>

<span data-ttu-id="80a6d-104">Récupère l’objet [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="80a6d-104">Retrieves the [**ID3DXFile**](id3dxfile.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="80a6d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80a6d-105">Syntax</span></span>


```C++
HRESULT GetFile(
  [out] ID3DXFile **ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="80a6d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80a6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80a6d-107">*ppFile* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="80a6d-107">*ppFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80a6d-108">Type : **[ **ID3DXFile**](id3dxfile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="80a6d-108">Type: **[**ID3DXFile**](id3dxfile.md)\*\***</span></span>

<span data-ttu-id="80a6d-109">Adresse d’un pointeur vers une interface [**ID3DXFile**](id3dxfile.md) représentant l’objet retourné.</span><span class="sxs-lookup"><span data-stu-id="80a6d-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) interface, representing the returned object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80a6d-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="80a6d-110">Return value</span></span>

<span data-ttu-id="80a6d-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80a6d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80a6d-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="80a6d-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="80a6d-113">Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="80a6d-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="80a6d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80a6d-114">Requirements</span></span>



| <span data-ttu-id="80a6d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80a6d-115">Requirement</span></span> | <span data-ttu-id="80a6d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="80a6d-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80a6d-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="80a6d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="80a6d-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="80a6d-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="80a6d-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="80a6d-119">Library</span></span><br/> | <dl> <span data-ttu-id="80a6d-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80a6d-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="80a6d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80a6d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80a6d-122">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="80a6d-122">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 




