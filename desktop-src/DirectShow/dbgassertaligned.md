---
description: Teste si un pointeur est aligné sur une limite spécifiée. Si ce n’est pas le cas, cette macro appelle la macro Assert. Ignoré dans les builds de vente au détail.
ms.assetid: 4d9ec3a9-7107-45a3-a7aa-28d6e38fa92a
title: DbgAssertAligned macro (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgAssertAligned
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 22b357f7f28e9df04ce36636e3972dbadc3036a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521739"
---
# <a name="dbgassertaligned-macro"></a><span data-ttu-id="03748-105">DbgAssertAligned macro)</span><span class="sxs-lookup"><span data-stu-id="03748-105">DbgAssertAligned macro</span></span>

<span data-ttu-id="03748-106">Teste si un pointeur est aligné sur une limite spécifiée.</span><span class="sxs-lookup"><span data-stu-id="03748-106">Tests whether a pointer is aligned to a specified boundary.</span></span> <span data-ttu-id="03748-107">Si ce n’est pas le cas, cette macro appelle la macro [**Assert**](assert.md) .</span><span class="sxs-lookup"><span data-stu-id="03748-107">If not, this macro invokes the [**ASSERT**](assert.md) macro.</span></span> <span data-ttu-id="03748-108">Ignoré dans les builds de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="03748-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="03748-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03748-109">Syntax</span></span>


```C++
void DbgAssertAligned(
    ptr,
    alignment
);
```



## <a name="parameters"></a><span data-ttu-id="03748-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03748-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03748-111">*ptr*</span><span class="sxs-lookup"><span data-stu-id="03748-111">*ptr*</span></span> 
</dt> <dd>

<span data-ttu-id="03748-112">Variable pointeur.</span><span class="sxs-lookup"><span data-stu-id="03748-112">Pointer variable.</span></span>

</dd> <dt>

<span data-ttu-id="03748-113">*repère*</span><span class="sxs-lookup"><span data-stu-id="03748-113">*alignment*</span></span> 
</dt> <dd>

<span data-ttu-id="03748-114">Alignement requis.</span><span class="sxs-lookup"><span data-stu-id="03748-114">Required alignment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03748-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03748-115">Return value</span></span>

<span data-ttu-id="03748-116">Cette macro ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="03748-116">This macro does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="03748-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03748-117">Requirements</span></span>



| <span data-ttu-id="03748-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03748-118">Requirement</span></span> | <span data-ttu-id="03748-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="03748-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03748-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="03748-120">Header</span></span><br/> | <dl> <span data-ttu-id="03748-121"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03748-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03748-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03748-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03748-123">Macros Assert et Breakpoint</span><span class="sxs-lookup"><span data-stu-id="03748-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




