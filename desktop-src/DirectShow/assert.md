---
description: Évalue une expression et affiche un message de diagnostic si l’expression a la valeur FALSe. Ignoré dans les builds de vente au détail.
ms.assetid: 8c3815bb-3164-4066-a947-974e791af5cd
title: DÉCLARER la macro (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 8617d1c86f655cc9b44ea6619931f73888ae2a67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520933"
---
# <a name="assert-macro"></a><span data-ttu-id="a1d58-104">ASSERT (macro)</span><span class="sxs-lookup"><span data-stu-id="a1d58-104">ASSERT macro</span></span>

<span data-ttu-id="a1d58-105">Évalue une expression et affiche un message de diagnostic si l’expression a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="a1d58-105">Evaluates an expression, and displays a diagnostic message if the expression is **FALSE**.</span></span> <span data-ttu-id="a1d58-106">Ignoré dans les builds de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="a1d58-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1d58-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1d58-107">Syntax</span></span>


```C++
void ASSERT(
   BOOL cond
);
```



## <a name="parameters"></a><span data-ttu-id="a1d58-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1d58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1d58-109">*185*</span><span class="sxs-lookup"><span data-stu-id="a1d58-109">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="a1d58-110">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="a1d58-110">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1d58-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a1d58-111">Return value</span></span>

<span data-ttu-id="a1d58-112">Cette macro ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a1d58-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1d58-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a1d58-113">Remarks</span></span>

<span data-ttu-id="a1d58-114">Dans les versions Debug, si l’expression est **false**, cette macro affiche une boîte de message avec le texte de l’expression, le nom du fichier source et le numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="a1d58-114">In debug builds, if the expression is **FALSE**, this macro displays a message box with the text of the expression, the name of the source file, and the line number.</span></span> <span data-ttu-id="a1d58-115">L’utilisateur peut ignorer l’assertion, entrer le débogueur ou quitter l’application.</span><span class="sxs-lookup"><span data-stu-id="a1d58-115">The user can ignore the assertion, enter the debugger, or quit the application.</span></span>

## <a name="examples"></a><span data-ttu-id="a1d58-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="a1d58-116">Examples</span></span>


```
ASSERT(rtStartTime <= rtEndTime);
```



## <a name="requirements"></a><span data-ttu-id="a1d58-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1d58-117">Requirements</span></span>



| <span data-ttu-id="a1d58-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1d58-118">Requirement</span></span> | <span data-ttu-id="a1d58-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1d58-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d58-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1d58-120">Header</span></span><br/> | <dl> <span data-ttu-id="a1d58-121"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1d58-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1d58-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1d58-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1d58-123">Macros Assert et Breakpoint</span><span class="sxs-lookup"><span data-stu-id="a1d58-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




