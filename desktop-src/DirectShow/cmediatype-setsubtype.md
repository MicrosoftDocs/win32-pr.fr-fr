---
description: La méthode SetSubtype spécifie le sous-type.
ms.assetid: cf52e0dc-d75b-408e-a63c-481d55151d4a
title: Méthode CMediaType. SetSubtype (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSubtype
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6474777b1b2e91ce0b676fdc7dbd572d7c622f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525219"
---
# <a name="cmediatypesetsubtype-method"></a><span data-ttu-id="038f7-103">Méthode CMediaType. SetSubtype</span><span class="sxs-lookup"><span data-stu-id="038f7-103">CMediaType.SetSubtype method</span></span>

<span data-ttu-id="038f7-104">La `SetSubtype` méthode spécifie le sous-type.</span><span class="sxs-lookup"><span data-stu-id="038f7-104">The `SetSubtype` method specifies the subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="038f7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="038f7-105">Syntax</span></span>


```C++
void SetSubtype(
   const GUID *psubtype
);
```



## <a name="parameters"></a><span data-ttu-id="038f7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="038f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="038f7-107">*psubtype*</span><span class="sxs-lookup"><span data-stu-id="038f7-107">*psubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="038f7-108">Pointeur vers un **GUID** qui spécifie le sous-type.</span><span class="sxs-lookup"><span data-stu-id="038f7-108">Pointer to a **GUID** that specifies the subtype.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="038f7-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="038f7-109">Return value</span></span>

<span data-ttu-id="038f7-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="038f7-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="038f7-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="038f7-111">Requirements</span></span>



| <span data-ttu-id="038f7-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="038f7-112">Requirement</span></span> | <span data-ttu-id="038f7-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="038f7-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="038f7-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="038f7-114">Header</span></span><br/>  | <dl> <span data-ttu-id="038f7-115"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="038f7-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="038f7-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="038f7-116">Library</span></span><br/> | <dl> <span data-ttu-id="038f7-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="038f7-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="038f7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="038f7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="038f7-119">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="038f7-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




