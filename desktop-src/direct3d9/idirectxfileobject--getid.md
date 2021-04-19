---
description: Récupère un pointeur vers le GUID qui identifie un objet fichier DirectX. Action déconseillée.
ms.assetid: 74c7a1d9-85e4-43eb-bcd8-1f3ddd713e9f
title: 'IDirectXFileObject :: GetId, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetId
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 336dbde487ecd1b3af7b32d3743f037c235952f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535808"
---
# <a name="idirectxfileobjectgetid-method"></a><span data-ttu-id="91d6f-104">IDirectXFileObject :: GetId, méthode</span><span class="sxs-lookup"><span data-stu-id="91d6f-104">IDirectXFileObject::GetId method</span></span>

<span data-ttu-id="91d6f-105">Récupère un pointeur vers le GUID qui identifie un objet fichier DirectX.</span><span class="sxs-lookup"><span data-stu-id="91d6f-105">Retrieves a pointer to the GUID that identifies a DirectX file object.</span></span> <span data-ttu-id="91d6f-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="91d6f-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="91d6f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91d6f-107">Syntax</span></span>


```C++
HRESULT GetId(
  [out, retval] 
            LPGUID pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="91d6f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91d6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91d6f-109">*pguid* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="91d6f-109">*pGuid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="91d6f-110">Type : **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="91d6f-110">Type: **LPGUID**</span></span>

<span data-ttu-id="91d6f-111">Pointeur vers un GUID pour recevoir l’ID de l’objet.</span><span class="sxs-lookup"><span data-stu-id="91d6f-111">Pointer to a GUID to receive the object's ID.</span></span> <span data-ttu-id="91d6f-112">La fonction définit le GUID sur un GUID **null** si l’objet n’a pas d’ID.</span><span class="sxs-lookup"><span data-stu-id="91d6f-112">The function will set the GUID to a **NULL** GUID if the object does not have an ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91d6f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91d6f-113">Return value</span></span>

<span data-ttu-id="91d6f-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="91d6f-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="91d6f-115">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="91d6f-115">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="91d6f-116">Si la méthode échoue, la valeur de retour peut être DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="91d6f-116">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="91d6f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91d6f-117">Requirements</span></span>



| <span data-ttu-id="91d6f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91d6f-118">Requirement</span></span> | <span data-ttu-id="91d6f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="91d6f-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91d6f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="91d6f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="91d6f-121"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="91d6f-121"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="91d6f-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="91d6f-122">Library</span></span><br/> | <dl> <span data-ttu-id="91d6f-123"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91d6f-123"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91d6f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91d6f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91d6f-125">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="91d6f-125">IDirectXFileObject</span></span>](idirectxfileobject.md)
</dt> </dl>

 

 




