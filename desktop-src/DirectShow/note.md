---
description: La macro NOTE envoie une chaîne à l’emplacement de sortie de débogage. Ignoré dans les builds de vente au détail.
ms.assetid: 8b85861a-b4d6-4cc6-9ac9-77d06f173869
title: Remarque (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NOTE
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 898d31c48807c3bf0826dc643d89126db36b0f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537663"
---
# <a name="note"></a><span data-ttu-id="122a7-104">REMARQUE</span><span class="sxs-lookup"><span data-stu-id="122a7-104">NOTE</span></span>

<span data-ttu-id="122a7-105">La `NOTE` macro envoie une chaîne à l’emplacement de sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="122a7-105">The `NOTE` macro sends a string to the debug output location.</span></span> <span data-ttu-id="122a7-106">Ignoré dans les builds de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="122a7-106">Ignored in retail builds.</span></span>

``` syntax
NOTE(
    pFormat
);

NOTEn(
    pFormat,
    arg1 ... arg5
);
```

## <a name="parameters"></a><span data-ttu-id="122a7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="122a7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="122a7-108"><span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*pFormat*</span><span class="sxs-lookup"><span data-stu-id="122a7-108"><span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*pFormat*</span></span>
</dt> <dd>

<span data-ttu-id="122a7-109">Chaîne de format printf-style.</span><span class="sxs-lookup"><span data-stu-id="122a7-109">A printf -style format string.</span></span>

</dd> <dt>

<span data-ttu-id="122a7-110"><span id="arg1arg5"></span><span id="ARG1ARG5"></span>*Arg1*–*Arg5*</span><span class="sxs-lookup"><span data-stu-id="122a7-110"><span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*–*arg5*</span></span>
</dt> <dd>

<span data-ttu-id="122a7-111">Arguments supplémentaires pour la chaîne de format.</span><span class="sxs-lookup"><span data-stu-id="122a7-111">Additional arguments for the format string.</span></span> <span data-ttu-id="122a7-112">Le nombre d’arguments doit correspondre au nom de la macro.</span><span class="sxs-lookup"><span data-stu-id="122a7-112">The number of arguments must match the macro name.</span></span> <span data-ttu-id="122a7-113">Par exemple, **Note1** accepte un argument et **Note5** accepte cinq arguments.</span><span class="sxs-lookup"><span data-stu-id="122a7-113">For example, **NOTE1** takes one argument, and **NOTE5** takes five arguments.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="122a7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="122a7-114">Remarks</span></span>

<span data-ttu-id="122a7-115">Ces macros sont des variantes de la macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="122a7-115">These macros are variants of the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="122a7-116">Ils génèrent des messages de suivi de niveau 5 \_ .</span><span class="sxs-lookup"><span data-stu-id="122a7-116">They generate level 5 LOG\_TRACE messages.</span></span>

## <a name="example"></a><span data-ttu-id="122a7-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="122a7-117">Example</span></span>


```C++
NOTE("Warning, failed to created graph.");
NOTE2("Width: %d, Height: %d", width, height);
```



## <a name="requirements"></a><span data-ttu-id="122a7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="122a7-118">Requirements</span></span>



| <span data-ttu-id="122a7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="122a7-119">Requirement</span></span> | <span data-ttu-id="122a7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="122a7-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="122a7-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="122a7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="122a7-122"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="122a7-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="122a7-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="122a7-123">Library</span></span><br/> | <dl> <span data-ttu-id="122a7-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="122a7-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="122a7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="122a7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="122a7-126">Fonctions de sortie de débogage</span><span class="sxs-lookup"><span data-stu-id="122a7-126">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




