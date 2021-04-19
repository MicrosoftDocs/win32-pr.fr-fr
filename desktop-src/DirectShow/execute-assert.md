---
description: Évalue une expression dans les builds de débogage et de vente au détail. Dans les versions Debug, affiche un message de diagnostic si l’expression a la valeur FALSe.
ms.assetid: 259a3d30-0b20-4430-8b74-83ec619576ae
title: Macro EXECUTE_ASSERT (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXECUTE_ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 5db5e78d198cc9f66aa5de6fdb0160e325b82591
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539261"
---
# <a name="execute_assert-macro"></a><span data-ttu-id="6d030-104">EXÉCUTER la \_ macro Assert</span><span class="sxs-lookup"><span data-stu-id="6d030-104">EXECUTE\_ASSERT macro</span></span>

<span data-ttu-id="6d030-105">Évalue une expression dans les builds de débogage et de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="6d030-105">Evaluates an expression in debug and retail builds.</span></span> <span data-ttu-id="6d030-106">Dans les versions Debug, affiche un message de diagnostic si l’expression a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="6d030-106">In debug builds, displays a diagnostic message if the expression is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d030-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d030-107">Syntax</span></span>


```C++
void EXECUTE_ASSERT(
    cond
);
```



## <a name="parameters"></a><span data-ttu-id="6d030-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d030-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d030-109">*185*</span><span class="sxs-lookup"><span data-stu-id="6d030-109">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="6d030-110">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="6d030-110">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d030-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d030-111">Return value</span></span>

<span data-ttu-id="6d030-112">Cette macro ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6d030-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d030-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6d030-113">Remarks</span></span>

<span data-ttu-id="6d030-114">Contrairement à la macro [**Assert**](assert.md) , cette macro évalue l’expression dans les builds de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="6d030-114">Unlike the [**ASSERT**](assert.md) macro, this macro evaluates the expression in retail builds.</span></span> <span data-ttu-id="6d030-115">Dans les versions Debug, si l’expression est **false**, la macro affiche une boîte de message avec le texte de l’expression, le nom du fichier source et le numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="6d030-115">In debug builds, if the expression is **FALSE**, the macro displays a message box with the text of the expression, the name of the source file, and the line number.</span></span> <span data-ttu-id="6d030-116">L’utilisateur peut ignorer l’assertion, entrer le débogueur ou quitter l’application.</span><span class="sxs-lookup"><span data-stu-id="6d030-116">The user can ignore the assertion, enter the debugger, or quit the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d030-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d030-117">Requirements</span></span>



| <span data-ttu-id="6d030-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d030-118">Requirement</span></span> | <span data-ttu-id="6d030-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d030-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d030-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d030-120">Header</span></span><br/> | <dl> <span data-ttu-id="6d030-121"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d030-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d030-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d030-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d030-123">Macros Assert et Breakpoint</span><span class="sxs-lookup"><span data-stu-id="6d030-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




