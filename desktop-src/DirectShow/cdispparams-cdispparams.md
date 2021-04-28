---
description: Méthode constructeur CDispParams. CDispParams.
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: Constructeur CDispParams. CDispParams (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDispParams.CDispParams
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 42f55a57a0f9e06d3001c2638d457fe0b82a914d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095787"
---
# <a name="cdispparamscdispparams-constructor"></a><span data-ttu-id="defce-103">Constructeur CDispParams. CDispParams</span><span class="sxs-lookup"><span data-stu-id="defce-103">CDispParams.CDispParams constructor</span></span>

<span data-ttu-id="defce-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="defce-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="defce-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="defce-105">Syntax</span></span>


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a><span data-ttu-id="defce-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="defce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="defce-107">*nArgs*</span><span class="sxs-lookup"><span data-stu-id="defce-107">*nArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="defce-108">Nombre d’arguments passés à la méthode ou à la propriété.</span><span class="sxs-lookup"><span data-stu-id="defce-108">Number of arguments passed to the method or property.</span></span>

</dd> <dt>

<span data-ttu-id="defce-109">*pArgs*</span><span class="sxs-lookup"><span data-stu-id="defce-109">*pArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="defce-110">Pointeur désignant la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="defce-110">Pointer to the list of arguments.</span></span> <span data-ttu-id="defce-111">Dans la liste, chaque argument est stocké avec son type Variant.</span><span class="sxs-lookup"><span data-stu-id="defce-111">In the list, each argument is stored with its variant type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="defce-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="defce-112">Requirements</span></span>



| <span data-ttu-id="defce-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="defce-113">Requirement</span></span> | <span data-ttu-id="defce-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="defce-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="defce-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="defce-115">Header</span></span><br/>  | <dl> <span data-ttu-id="defce-116"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="defce-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="defce-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="defce-117">Library</span></span><br/> | <dl> <span data-ttu-id="defce-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="defce-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="defce-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="defce-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="defce-120">**CDispParams, classe**</span><span class="sxs-lookup"><span data-stu-id="defce-120">**CDispParams Class**</span></span>](cdispparams.md)
</dt> </dl>

 

 




