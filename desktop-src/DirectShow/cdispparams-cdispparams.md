---
description: Méthode de constructeur.
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
ms.openlocfilehash: f3beeb0a6e3a18c3fac6606385d9206938bbc1cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539724"
---
# <a name="cdispparamscdispparams-constructor"></a><span data-ttu-id="c205e-103">Constructeur CDispParams. CDispParams</span><span class="sxs-lookup"><span data-stu-id="c205e-103">CDispParams.CDispParams constructor</span></span>

<span data-ttu-id="c205e-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="c205e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c205e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c205e-105">Syntax</span></span>


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a><span data-ttu-id="c205e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c205e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c205e-107">*nArgs*</span><span class="sxs-lookup"><span data-stu-id="c205e-107">*nArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="c205e-108">Nombre d’arguments passés à la méthode ou à la propriété.</span><span class="sxs-lookup"><span data-stu-id="c205e-108">Number of arguments passed to the method or property.</span></span>

</dd> <dt>

<span data-ttu-id="c205e-109">*pArgs*</span><span class="sxs-lookup"><span data-stu-id="c205e-109">*pArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="c205e-110">Pointeur désignant la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="c205e-110">Pointer to the list of arguments.</span></span> <span data-ttu-id="c205e-111">Dans la liste, chaque argument est stocké avec son type Variant.</span><span class="sxs-lookup"><span data-stu-id="c205e-111">In the list, each argument is stored with its variant type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c205e-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c205e-112">Requirements</span></span>



| <span data-ttu-id="c205e-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c205e-113">Requirement</span></span> | <span data-ttu-id="c205e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c205e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c205e-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="c205e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c205e-116"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c205e-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c205e-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c205e-117">Library</span></span><br/> | <dl> <span data-ttu-id="c205e-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c205e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c205e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c205e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c205e-120">**CDispParams, classe**</span><span class="sxs-lookup"><span data-stu-id="c205e-120">**CDispParams Class**</span></span>](cdispparams.md)
</dt> </dl>

 

 




