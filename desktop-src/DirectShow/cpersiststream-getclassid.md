---
description: Récupère l’identificateur de classe pour ce filtre.
ms.assetid: f0559437-5d0d-4522-a3dc-947e3494b576
title: Méthode CPersistStream. GetClassID (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7603541eae4f431327a91777488a740afb7f628b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541151"
---
# <a name="cpersiststreamgetclassid-method"></a><span data-ttu-id="c1914-103">Méthode CPersistStream. GetClassID</span><span class="sxs-lookup"><span data-stu-id="c1914-103">CPersistStream.GetClassID method</span></span>

<span data-ttu-id="c1914-104">Récupère l’identificateur de classe pour ce filtre.</span><span class="sxs-lookup"><span data-stu-id="c1914-104">Retrieves the class identifier for this filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1914-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1914-105">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="c1914-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1914-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1914-107">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="c1914-107">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="c1914-108">Pointeur vers une structure CLSID.</span><span class="sxs-lookup"><span data-stu-id="c1914-108">Pointer to a CLSID structure.</span></span> <span data-ttu-id="c1914-109">Copiez votre ID de classe ici.</span><span class="sxs-lookup"><span data-stu-id="c1914-109">Copy your class ID to here.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1914-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1914-110">Return value</span></span>

<span data-ttu-id="c1914-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c1914-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1914-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1914-112">Requirements</span></span>



| <span data-ttu-id="c1914-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1914-113">Requirement</span></span> | <span data-ttu-id="c1914-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1914-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1914-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1914-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c1914-116"><dt>PStream. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1914-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c1914-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c1914-117">Library</span></span><br/> | <dl> <span data-ttu-id="c1914-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c1914-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1914-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1914-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1914-120">**CPersistStream, classe**</span><span class="sxs-lookup"><span data-stu-id="c1914-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




