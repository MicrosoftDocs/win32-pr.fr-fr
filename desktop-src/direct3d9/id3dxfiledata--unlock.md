---
description: 'Termine la durée de vie du pointeur ppData retourné par ID3DXFileData :: Lock.'
ms.assetid: 6032ea1f-3c73-4157-ba3f-41ce9e73d64c
title: 'ID3DXFileData :: Unlock, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Unlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8371b87152a6184f34a225b24d2de1b0fd21248f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762140"
---
# <a name="id3dxfiledataunlock-method"></a><span data-ttu-id="40750-103">ID3DXFileData :: Unlock, méthode</span><span class="sxs-lookup"><span data-stu-id="40750-103">ID3DXFileData::Unlock method</span></span>

<span data-ttu-id="40750-104">Termine la durée de vie du pointeur *ppData* retourné par [**ID3DXFileData :: Lock**](id3dxfiledata--lock.md).</span><span class="sxs-lookup"><span data-stu-id="40750-104">Ends the lifespan of the *ppData* pointer returned by [**ID3DXFileData::Lock**](id3dxfiledata--lock.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="40750-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40750-105">Syntax</span></span>


```C++
BOOL Unlock();
```



## <a name="parameters"></a><span data-ttu-id="40750-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40750-106">Parameters</span></span>

<span data-ttu-id="40750-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="40750-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="40750-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40750-108">Return value</span></span>

<span data-ttu-id="40750-109">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40750-109">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40750-110">La valeur de retour est \_ OK.</span><span class="sxs-lookup"><span data-stu-id="40750-110">The return value is S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="40750-111">Notes</span><span class="sxs-lookup"><span data-stu-id="40750-111">Remarks</span></span>

<span data-ttu-id="40750-112">Vous devez vous assurer que le nombre d’appels [**ID3DXFileData :: Lock**](id3dxfiledata--lock.md) correspond au nombre d’appels **ID3DXFileData :: Unlock** .</span><span class="sxs-lookup"><span data-stu-id="40750-112">You must ensure that the number of [**ID3DXFileData::Lock**](id3dxfiledata--lock.md) calls matches the number of **ID3DXFileData::Unlock** calls.</span></span> <span data-ttu-id="40750-113">Après l’appel de Unlock, le pointeur ppData retourné par **ID3DXFileData :: Lock** ne doit plus être utilisé.</span><span class="sxs-lookup"><span data-stu-id="40750-113">After calling Unlock, the ppData pointer returned by **ID3DXFileData::Lock** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="40750-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40750-114">Requirements</span></span>



| <span data-ttu-id="40750-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40750-115">Requirement</span></span> | <span data-ttu-id="40750-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="40750-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40750-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="40750-117">Header</span></span><br/>  | <dl> <span data-ttu-id="40750-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="40750-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="40750-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="40750-119">Library</span></span><br/> | <dl> <span data-ttu-id="40750-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40750-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="40750-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40750-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40750-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="40750-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
