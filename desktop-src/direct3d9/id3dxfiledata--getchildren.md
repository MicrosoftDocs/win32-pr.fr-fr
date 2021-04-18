---
description: Récupère le nombre d’enfants dans cet objet de données de fichier.
ms.assetid: ebc6905b-a453-4a15-adae-956ce7034084
title: 'ID3DXFileData :: GetChildren, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChildren
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: dd6932801f3d4b079efa6f1ed2688505dbd7828b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520330"
---
# <a name="id3dxfiledatagetchildren-method"></a><span data-ttu-id="e173f-103">ID3DXFileData :: GetChildren, méthode</span><span class="sxs-lookup"><span data-stu-id="e173f-103">ID3DXFileData::GetChildren method</span></span>

<span data-ttu-id="e173f-104">Récupère le nombre d’enfants dans cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="e173f-104">Retrieves the number of children in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e173f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e173f-105">Syntax</span></span>


```C++
HRESULT GetChildren(
  [in] SIZE_T *puiChildren
);
```



## <a name="parameters"></a><span data-ttu-id="e173f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e173f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e173f-107">*puiChildren* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e173f-107">*puiChildren* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e173f-108">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e173f-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e173f-109">Adresse d’un pointeur recevant le nombre d’enfants dans cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="e173f-109">Address of a pointer to receive the number of children in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e173f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e173f-110">Return value</span></span>

<span data-ttu-id="e173f-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e173f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e173f-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e173f-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e173f-113">Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="e173f-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="e173f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e173f-114">Requirements</span></span>



| <span data-ttu-id="e173f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e173f-115">Requirement</span></span> | <span data-ttu-id="e173f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e173f-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e173f-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="e173f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e173f-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="e173f-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="e173f-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e173f-119">Library</span></span><br/> | <dl> <span data-ttu-id="e173f-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e173f-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e173f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e173f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e173f-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="e173f-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
