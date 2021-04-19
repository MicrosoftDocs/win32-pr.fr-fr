---
description: Définit la partie FOURCC de l’objet FOURCCMap.
ms.assetid: cc821e39-e565-4255-a289-2c9507d43433
title: 'FOURCCMap :: SetFOURCC, méthode (FourCC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.SetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 435eb209e39ffad29f041e2e117a45d735abffed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543233"
---
# <a name="fourccmapsetfourcc-method"></a><span data-ttu-id="a4e08-103">FOURCCMap :: SetFOURCC, méthode</span><span class="sxs-lookup"><span data-stu-id="a4e08-103">FOURCCMap::SetFOURCC method</span></span>

<span data-ttu-id="a4e08-104">Définit la partie **FourCC** de l’objet [**FOURCCMap**](fourccmap.md) .</span><span class="sxs-lookup"><span data-stu-id="a4e08-104">Sets the **FOURCC** portion of the [**FOURCCMap**](fourccmap.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4e08-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4e08-105">Syntax</span></span>


```C++
void SetFOURCC(
   const GUID *pguid
);
```



## <a name="parameters"></a><span data-ttu-id="a4e08-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4e08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4e08-107">*pguid*</span><span class="sxs-lookup"><span data-stu-id="a4e08-107">*pguid*</span></span> 
</dt> <dd>

<span data-ttu-id="a4e08-108">Pointeur vers la partie d’identificateur global unique (**GUID**) retournée de l’objet **FOURCCMap** .</span><span class="sxs-lookup"><span data-stu-id="a4e08-108">Pointer to the returned globally unique identifier (**GUID**) part of the **FOURCCMap** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4e08-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a4e08-109">Return value</span></span>

<span data-ttu-id="a4e08-110">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="a4e08-110">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4e08-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4e08-111">Requirements</span></span>



| <span data-ttu-id="a4e08-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4e08-112">Requirement</span></span> | <span data-ttu-id="a4e08-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4e08-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4e08-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="a4e08-114">Header</span></span><br/>  | <dl> <span data-ttu-id="a4e08-115"><dt>FourCC. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4e08-115"><dt>Fourcc.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a4e08-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a4e08-116">Library</span></span><br/> | <dl> <span data-ttu-id="a4e08-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a4e08-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4e08-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4e08-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4e08-119">**FOURCCMap, classe**</span><span class="sxs-lookup"><span data-stu-id="a4e08-119">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




