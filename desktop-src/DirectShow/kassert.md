---
description: Évalue une expression et provoque une exception de point d’arrêt si l’expression est FALSe. Le texte de l’expression, le nom du fichier source et le numéro de ligne sont journalisés à l’aide de la macro DbgLog. Ignoré dans les builds de vente au détail.
ms.assetid: fd116403-df23-490f-b3a8-b2a8bf2b4a5f
title: KASSERT macro (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: f797e60a6175a86f2c1c9d675e9607a48a58c14a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534907"
---
# <a name="kassert-macro"></a><span data-ttu-id="c3d66-105">KASSERT macro)</span><span class="sxs-lookup"><span data-stu-id="c3d66-105">KASSERT macro</span></span>

<span data-ttu-id="c3d66-106">Évalue une expression et provoque une exception de point d’arrêt si l’expression est **false**.</span><span class="sxs-lookup"><span data-stu-id="c3d66-106">Evaluates an expression, and causes a breakpoint exception if the expression is **FALSE**.</span></span> <span data-ttu-id="c3d66-107">Le texte de l’expression, le nom du fichier source et le numéro de ligne sont journalisés à l’aide de la macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="c3d66-107">The text of the expression, the name of the source file, and the line number are logged using the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="c3d66-108">Ignoré dans les builds de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="c3d66-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d66-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3d66-109">Syntax</span></span>


```C++
void KASSERT(
    cond
);
```



## <a name="parameters"></a><span data-ttu-id="c3d66-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3d66-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3d66-111">*185*</span><span class="sxs-lookup"><span data-stu-id="c3d66-111">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="c3d66-112">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="c3d66-112">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3d66-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3d66-113">Return value</span></span>

<span data-ttu-id="c3d66-114">Cette macro ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c3d66-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3d66-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c3d66-115">Remarks</span></span>

<span data-ttu-id="c3d66-116">Contrairement aux [](assert.md) macros Assert et [**Execute \_ Assert**](execute-assert.md) , cette macro n’affiche pas de boîte de message invitant l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c3d66-116">Unlike the [**ASSERT**](assert.md) and [**EXECUTE\_ASSERT**](execute-assert.md) macros, this macro does not display a message box prompting the user.</span></span> <span data-ttu-id="c3d66-117">Dans les versions Debug, si l’expression est **false**, la macro provoque automatiquement l’apparition d’une exception de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="c3d66-117">In debug builds, if the expression is **FALSE**, the macro automatically causes a breakpoint exception to occur.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3d66-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3d66-118">Requirements</span></span>



| <span data-ttu-id="c3d66-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3d66-119">Requirement</span></span> | <span data-ttu-id="c3d66-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3d66-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3d66-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3d66-121">Header</span></span><br/> | <dl> <span data-ttu-id="c3d66-122"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3d66-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3d66-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3d66-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3d66-124">Macros Assert et Breakpoint</span><span class="sxs-lookup"><span data-stu-id="c3d66-124">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




