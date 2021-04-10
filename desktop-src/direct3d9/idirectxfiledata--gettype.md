---
description: Récupère le GUID du modèle de l’objet. Action déconseillée.
ms.assetid: bb4a4a32-a9e7-4caa-869d-24cfb310d8d1
title: 'IDirectXFileData :: GetType, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 463391c661b2d166a6fba773e3b01590daf0ebd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116262"
---
# <a name="idirectxfiledatagettype-method"></a><span data-ttu-id="65499-104">IDirectXFileData :: GetType, méthode</span><span class="sxs-lookup"><span data-stu-id="65499-104">IDirectXFileData::GetType method</span></span>

<span data-ttu-id="65499-105">Récupère le GUID du modèle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="65499-105">Retrieves the GUID of the object's template.</span></span> <span data-ttu-id="65499-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="65499-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="65499-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65499-107">Syntax</span></span>


```C++
HRESULT GetType(
  [out, retval] const GUID **ppguid
);
```



## <a name="parameters"></a><span data-ttu-id="65499-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65499-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65499-109">*ppGUID* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="65499-109">*ppguid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="65499-110">Type : **const [**GUID**](guid.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="65499-110">Type: **const [**GUID**](guid.md)\*\***</span></span>

<span data-ttu-id="65499-111">Adresse d’un pointeur devant recevoir le GUID du modèle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="65499-111">Address of a pointer to receive the GUID of the object's template.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65499-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65499-112">Return value</span></span>

<span data-ttu-id="65499-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="65499-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="65499-114">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="65499-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="65499-115">Si la méthode échoue, la valeur de retour peut être DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="65499-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="65499-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65499-116">Requirements</span></span>



| <span data-ttu-id="65499-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65499-117">Requirement</span></span> | <span data-ttu-id="65499-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="65499-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65499-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="65499-119">Header</span></span><br/>  | <dl> <span data-ttu-id="65499-120"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="65499-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="65499-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="65499-121">Library</span></span><br/> | <dl> <span data-ttu-id="65499-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65499-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65499-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65499-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65499-124">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="65499-124">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> </dl>

 

 




