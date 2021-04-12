---
description: Macros Assert et Breakpoint
ms.assetid: c34db182-1f65-4a2f-9534-268638c2502d
title: Macros Assert et Breakpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4771fb7e302ec9e1093fca82d7842212e0b68e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109734"
---
# <a name="assert-and-breakpoint-macros"></a><span data-ttu-id="531c1-103">Macros Assert et Breakpoint</span><span class="sxs-lookup"><span data-stu-id="531c1-103">Assert and Breakpoint Macros</span></span>

<span data-ttu-id="531c1-104">Les [classes de base DirectShow](directshow-base-classes.md) fournissent plusieurs macros qui effectuent des assertions ou génèrent des points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="531c1-104">The [DirectShow Base Classes](directshow-base-classes.md) provide several macros that perform asserts or cause breakpoints.</span></span>



| <span data-ttu-id="531c1-105">Macro</span><span class="sxs-lookup"><span data-stu-id="531c1-105">Macro</span></span>                                        | <span data-ttu-id="531c1-106">Description</span><span class="sxs-lookup"><span data-stu-id="531c1-106">Description</span></span>                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="531c1-107">**ASSERT**</span><span class="sxs-lookup"><span data-stu-id="531c1-107">**ASSERT**</span></span>](assert.md)                     | <span data-ttu-id="531c1-108">Évalue une expression et affiche un message de diagnostic si l’expression a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="531c1-108">Evaluates an expression, and displays a diagnostic message if the expression is **FALSE**.</span></span>                                         |
| [<span data-ttu-id="531c1-109">**DbgAssertAligned**</span><span class="sxs-lookup"><span data-stu-id="531c1-109">**DbgAssertAligned**</span></span>](dbgassertaligned.md) | <span data-ttu-id="531c1-110">Teste si un pointeur est aligné sur une limite spécifiée.</span><span class="sxs-lookup"><span data-stu-id="531c1-110">Tests whether a pointer is aligned to a specified boundary.</span></span>                                                                        |
| [<span data-ttu-id="531c1-111">**DbgBreak**</span><span class="sxs-lookup"><span data-stu-id="531c1-111">**DbgBreak**</span></span>](dbgbreak.md)                 | <span data-ttu-id="531c1-112">Affiche une boîte de message avec la chaîne spécifiée, le nom du fichier source et le numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="531c1-112">Displays a message box with the specified string, the name of the source file, and the line number.</span></span>                                |
| [<span data-ttu-id="531c1-113">**EXÉCUTER une \_ assertion**</span><span class="sxs-lookup"><span data-stu-id="531c1-113">**EXECUTE\_ASSERT**</span></span>](execute-assert.md)    | <span data-ttu-id="531c1-114">Évalue une expression dans les builds de débogage et de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="531c1-114">Evaluates an expression in debug and retail builds.</span></span> <span data-ttu-id="531c1-115">Dans les versions Debug, affiche un message de diagnostic si l’expression a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="531c1-115">In debug builds, displays a diagnostic message if the expression is **FALSE**.</span></span> |
| [<span data-ttu-id="531c1-116">**KASSERT**</span><span class="sxs-lookup"><span data-stu-id="531c1-116">**KASSERT**</span></span>](kassert.md)                   | <span data-ttu-id="531c1-117">Évalue une expression et provoque une exception de point d’arrêt si l’expression est **false**.</span><span class="sxs-lookup"><span data-stu-id="531c1-117">Evaluates an expression, and causes a breakpoint exception if the expression is **FALSE**.</span></span>                                         |
| [<span data-ttu-id="531c1-118">**KDbgBreak**</span><span class="sxs-lookup"><span data-stu-id="531c1-118">**KDbgBreak**</span></span>](kdbgbreak.md)               | <span data-ttu-id="531c1-119">Provoque une exception de point d’arrêt et journalise la chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="531c1-119">Causes a breakpoint exception, and logs the specified string.</span></span>                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="531c1-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="531c1-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="531c1-121">Utilitaires de débogage</span><span class="sxs-lookup"><span data-stu-id="531c1-121">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



