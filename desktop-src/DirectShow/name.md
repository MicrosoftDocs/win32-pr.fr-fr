---
description: La macro NAME génère une chaîne de débogage uniquement.
ms.assetid: 5cb9f803-dd2b-4055-bdcc-e754ef5fa505
title: NOM (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAME
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b698551789deb0c3775bd4ac722136e1abc9d38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540463"
---
# <a name="name"></a><span data-ttu-id="30a31-103">NOM</span><span class="sxs-lookup"><span data-stu-id="30a31-103">NAME</span></span>

<span data-ttu-id="30a31-104">La macro **Name** génère une chaîne de débogage uniquement.</span><span class="sxs-lookup"><span data-stu-id="30a31-104">The **NAME** macro generates a debug-only string.</span></span>

``` syntax
NAME(strLiteral);
```

## <a name="parameters"></a><span data-ttu-id="30a31-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30a31-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30a31-106"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="30a31-106"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span></span>
</dt> <dd>

<span data-ttu-id="30a31-107">Chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="30a31-107">Text string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30a31-108">Notes</span><span class="sxs-lookup"><span data-stu-id="30a31-108">Remarks</span></span>

<span data-ttu-id="30a31-109">Dans les versions Debug, cette macro est équivalente à la macro **Text** .</span><span class="sxs-lookup"><span data-stu-id="30a31-109">In debug builds, this macro is equivalent to the **TEXT** macro.</span></span> <span data-ttu-id="30a31-110">Dans les versions commerciales, elle correspond à (TCHAR \* ) **null**.</span><span class="sxs-lookup"><span data-stu-id="30a31-110">In retail builds, it resolves to (TCHAR\*) **NULL**.</span></span> <span data-ttu-id="30a31-111">Cette macro est utile lors de la déclaration du nom d’un objet qui dérive de la classe [**CBaseObject**](cbaseobject.md) .</span><span class="sxs-lookup"><span data-stu-id="30a31-111">This macro is useful when declaring the name of an object that derives from the [**CBaseObject**](cbaseobject.md) class.</span></span>


```C++
pObject = new CBaseObject(NAME("My Object"));
```



## <a name="requirements"></a><span data-ttu-id="30a31-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30a31-112">Requirements</span></span>



| <span data-ttu-id="30a31-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30a31-113">Requirement</span></span> | <span data-ttu-id="30a31-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="30a31-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a31-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="30a31-115">Header</span></span><br/>  | <dl> <span data-ttu-id="30a31-116"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30a31-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="30a31-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="30a31-117">Library</span></span><br/> | <dl> <span data-ttu-id="30a31-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="30a31-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30a31-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30a31-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30a31-120">Fonctions de sortie de débogage</span><span class="sxs-lookup"><span data-stu-id="30a31-120">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




