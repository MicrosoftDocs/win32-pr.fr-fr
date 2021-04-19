---
description: Provoque une exception de point d’arrêt et journalise la chaîne spécifiée à l’aide de la macro DbgLog. Ignoré dans les builds de vente au détail.
ms.assetid: 475810db-692b-4727-9ef1-ece74e9618d0
title: KDbgBreak macro (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KDbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 9631dc8d956652137810b25ae5923cc1c6927bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540994"
---
# <a name="kdbgbreak-macro"></a><span data-ttu-id="e670b-104">KDbgBreak macro)</span><span class="sxs-lookup"><span data-stu-id="e670b-104">KDbgBreak macro</span></span>

<span data-ttu-id="e670b-105">Provoque une exception de point d’arrêt et journalise la chaîne spécifiée à l’aide de la macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="e670b-105">Causes a breakpoint exception, and logs the specified string using the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="e670b-106">Ignoré dans les builds de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="e670b-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="e670b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e670b-107">Syntax</span></span>


```C++
void KDbgBreak(
    strLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="e670b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e670b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e670b-109">*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="e670b-109">*strLiteral*</span></span> 
</dt> <dd>

<span data-ttu-id="e670b-110">Chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="e670b-110">Text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e670b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e670b-111">Return value</span></span>

<span data-ttu-id="e670b-112">Cette macro ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e670b-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e670b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e670b-113">Remarks</span></span>

<span data-ttu-id="e670b-114">Contrairement à la macro [**DbgBreak**](dbgbreak.md) , cette macro n’affiche pas de boîte de message invitant l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e670b-114">Unlike the [**DbgBreak**](dbgbreak.md) macro, this macro does not display a message box prompting the user.</span></span> <span data-ttu-id="e670b-115">Dans les versions Debug, il provoque automatiquement une exception de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="e670b-115">In debug builds, it automatically causes a breakpoint exception to occur.</span></span>

## <a name="requirements"></a><span data-ttu-id="e670b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e670b-116">Requirements</span></span>



| <span data-ttu-id="e670b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e670b-117">Requirement</span></span> | <span data-ttu-id="e670b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e670b-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e670b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="e670b-119">Header</span></span><br/> | <dl> <span data-ttu-id="e670b-120"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e670b-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e670b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e670b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e670b-122">Macros Assert et Breakpoint</span><span class="sxs-lookup"><span data-stu-id="e670b-122">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




