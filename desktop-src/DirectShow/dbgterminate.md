---
description: La fonction DbgTerminate nettoie la bibliothèque de débogage. Ignoré dans les builds de vente au détail.
ms.assetid: a0e23c57-b4b5-4bcf-8c63-0dee40cc71a7
title: DbgTerminate, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgTerminate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d29e5fde86b9573261e39a0dbe2e9d87018ff23c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539616"
---
# <a name="dbgterminate-function"></a><span data-ttu-id="0ad37-104">DbgTerminate fonction)</span><span class="sxs-lookup"><span data-stu-id="0ad37-104">DbgTerminate function</span></span>

<span data-ttu-id="0ad37-105">La fonction **DbgTerminate** nettoie la bibliothèque de débogage.</span><span class="sxs-lookup"><span data-stu-id="0ad37-105">The **DbgTerminate** function cleans up the debug library.</span></span> <span data-ttu-id="0ad37-106">Ignoré dans les builds de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="0ad37-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ad37-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ad37-107">Syntax</span></span>


```C++
void DbgTerminate(void);
```



## <a name="parameters"></a><span data-ttu-id="0ad37-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ad37-108">Parameters</span></span>

<span data-ttu-id="0ad37-109">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="0ad37-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ad37-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ad37-110">Return value</span></span>

<span data-ttu-id="0ad37-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0ad37-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ad37-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0ad37-112">Remarks</span></span>

<span data-ttu-id="0ad37-113">Appelez cette fonction si vous appelez la fonction [**DbgInitialise**](dbginitialise.md) .</span><span class="sxs-lookup"><span data-stu-id="0ad37-113">Call this function if you call the [**DbgInitialise**](dbginitialise.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ad37-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ad37-114">Requirements</span></span>



| <span data-ttu-id="0ad37-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ad37-115">Requirement</span></span> | <span data-ttu-id="0ad37-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ad37-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ad37-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ad37-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0ad37-118"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ad37-118"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0ad37-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0ad37-119">Library</span></span><br/> | <dl> <span data-ttu-id="0ad37-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0ad37-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ad37-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ad37-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ad37-122">Fonctions de sortie de débogage</span><span class="sxs-lookup"><span data-stu-id="0ad37-122">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




