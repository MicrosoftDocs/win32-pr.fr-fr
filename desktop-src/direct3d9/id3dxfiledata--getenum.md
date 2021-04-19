---
description: Récupère l’objet d’énumération dans cet objet de données de fichier.
ms.assetid: 383560e2-1888-4e37-9883-2ddbcb101cf6
title: 'ID3DXFileData :: GetEnum, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetEnum
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7dd565f6f76d42159d77d8b83c638c75648f293b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542177"
---
# <a name="id3dxfiledatagetenum-method"></a><span data-ttu-id="97279-103">ID3DXFileData :: GetEnum, méthode</span><span class="sxs-lookup"><span data-stu-id="97279-103">ID3DXFileData::GetEnum method</span></span>

<span data-ttu-id="97279-104">Récupère l’objet d’énumération dans cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="97279-104">Retrieves the enumeration object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="97279-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97279-105">Syntax</span></span>


```C++
HRESULT GetEnum(
  [in] ID3DXFileEnumObject **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="97279-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97279-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97279-107">*ppObj* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97279-107">*ppObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97279-108">Type : **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="97279-108">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span></span>

<span data-ttu-id="97279-109">Adresse d’un pointeur devant recevoir l’objet d’énumération dans cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="97279-109">Address of a pointer to receive the enumeration object in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97279-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97279-110">Return value</span></span>

<span data-ttu-id="97279-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="97279-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="97279-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="97279-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="97279-113">Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="97279-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="97279-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97279-114">Requirements</span></span>



| <span data-ttu-id="97279-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97279-115">Requirement</span></span> | <span data-ttu-id="97279-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="97279-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97279-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="97279-117">Header</span></span><br/>  | <dl> <span data-ttu-id="97279-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="97279-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="97279-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="97279-119">Library</span></span><br/> | <dl> <span data-ttu-id="97279-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97279-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="97279-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97279-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97279-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="97279-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




