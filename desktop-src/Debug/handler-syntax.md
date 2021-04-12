---
description: Cette section décrit la syntaxe et l’utilisation de la gestion structurée des exceptions telle qu’elle est implémentée dans le compilateur d’optimisation Microsoft C/C++. Les mots clés suivants sont interprétés par le compilateur dans le cadre du mécanisme de gestion structurée des exceptions.
ms.assetid: 22190b75-417c-49d3-83fe-546018fb61ea
title: Syntaxe du gestionnaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c50b8d12a74312c8b0a843ea300d23e278e88
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860681"
---
# <a name="handler-syntax"></a><span data-ttu-id="250ba-104">Syntaxe du gestionnaire</span><span class="sxs-lookup"><span data-stu-id="250ba-104">Handler Syntax</span></span>

<span data-ttu-id="250ba-105">Cette section décrit la syntaxe et l’utilisation de la gestion structurée des exceptions telle qu’elle est implémentée dans le compilateur d’optimisation Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="250ba-105">This section describes the syntax and usage of structured exception handling as implemented in the Microsoft C/C++ Optimizing Compiler.</span></span> <span data-ttu-id="250ba-106">Les mots clés suivants sont interprétés par le compilateur dans le cadre du mécanisme de gestion structurée des exceptions.</span><span class="sxs-lookup"><span data-stu-id="250ba-106">The following keywords are interpreted by the compiler as part of the structured exception-handling mechanism.</span></span>



| <span data-ttu-id="250ba-107">Mot clé</span><span class="sxs-lookup"><span data-stu-id="250ba-107">Keyword</span></span>         | <span data-ttu-id="250ba-108">Description</span><span class="sxs-lookup"><span data-stu-id="250ba-108">Description</span></span>                                                                                                                                                                                                                                      |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="250ba-109">**\_\_Essayez**</span><span class="sxs-lookup"><span data-stu-id="250ba-109">**\_\_try**</span></span>     | <span data-ttu-id="250ba-110">Commence un corps de code protégé.</span><span class="sxs-lookup"><span data-stu-id="250ba-110">Begins a guarded body of code.</span></span> <span data-ttu-id="250ba-111">Utilisé avec le mot clé **\_ \_ except** pour construire un [Gestionnaire d’exceptions](exception-handler-syntax.md), ou avec le mot clé **\_ \_ finally** pour construire un gestionnaire de [terminaisons](termination-handler-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="250ba-111">Used with the **\_\_except** keyword to construct an [exception handler](exception-handler-syntax.md), or with the **\_\_finally** keyword to construct a [termination handler](termination-handler-syntax.md).</span></span> |
| <span data-ttu-id="250ba-112">**\_\_mais**</span><span class="sxs-lookup"><span data-stu-id="250ba-112">**\_\_except**</span></span>  | <span data-ttu-id="250ba-113">Commence un bloc de code qui est exécuté uniquement lorsqu’une exception se produit dans son bloc **\_ \_ try** associé.</span><span class="sxs-lookup"><span data-stu-id="250ba-113">Begins a block of code that is executed only when an exception occurs within its associated **\_\_try** block.</span></span>                                                                                                                                   |
| <span data-ttu-id="250ba-114">**\_\_suivie**</span><span class="sxs-lookup"><span data-stu-id="250ba-114">**\_\_finally**</span></span> | <span data-ttu-id="250ba-115">Commence un bloc de code qui est exécuté chaque fois que le workflow de contrôle quitte son bloc **\_ \_ try** associé.</span><span class="sxs-lookup"><span data-stu-id="250ba-115">Begins a block of code that is executed whenever the flow of control leaves its associated **\_\_try** block.</span></span>                                                                                                                                    |
| <span data-ttu-id="250ba-116">**\_\_congé**</span><span class="sxs-lookup"><span data-stu-id="250ba-116">**\_\_leave**</span></span>   | <span data-ttu-id="250ba-117">Autorise l’arrêt immédiat du bloc **\_ \_ try** sans entraîner un arrêt anormal et une baisse des performances.</span><span class="sxs-lookup"><span data-stu-id="250ba-117">Allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span>                                                                                                                      |



 

<span data-ttu-id="250ba-118">Le compilateur interprète également les fonctions [**GetExceptionCode**](getexceptioncode.md), [**GetExceptionInformation**](getexceptioninformation.md)et [**AbnormalTermination**](abnormaltermination.md) comme des mots clés, et leur utilisation en dehors de la syntaxe de gestion des exceptions appropriée génère une erreur du compilateur.</span><span class="sxs-lookup"><span data-stu-id="250ba-118">The compiler also interprets the [**GetExceptionCode**](getexceptioncode.md), [**GetExceptionInformation**](getexceptioninformation.md), and [**AbnormalTermination**](abnormaltermination.md) functions as keywords, and their use outside the appropriate exception-handling syntax generates a compiler error.</span></span> <span data-ttu-id="250ba-119">Vous trouverez ci-dessous une brève description de ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="250ba-119">The following are brief descriptions of these functions.</span></span>



| <span data-ttu-id="250ba-120">Fonction</span><span class="sxs-lookup"><span data-stu-id="250ba-120">Function</span></span>                                                   | <span data-ttu-id="250ba-121">Description</span><span class="sxs-lookup"><span data-stu-id="250ba-121">Description</span></span>                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="250ba-122">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="250ba-122">**GetExceptionCode**</span></span>](getexceptioncode.md)               | <span data-ttu-id="250ba-123">Retourne un code qui identifie le type d’exception.</span><span class="sxs-lookup"><span data-stu-id="250ba-123">Returns a code that identifies the type of exception.</span></span> <span data-ttu-id="250ba-124">Cette fonction ne peut être appelée qu’à partir de l’expression de filtre ou du bloc de gestionnaire d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="250ba-124">This function can be called only from within the filter expression or the exception-handler block.</span></span>                                                                                                |
| [<span data-ttu-id="250ba-125">**GetExceptionInformation**</span><span class="sxs-lookup"><span data-stu-id="250ba-125">**GetExceptionInformation**</span></span>](getexceptioninformation.md) | <span data-ttu-id="250ba-126">Retourne un pointeur vers une structure de [**\_ pointeurs d’exception**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) contenant des pointeurs vers l’enregistrement de contexte et l’enregistrement d’exception.</span><span class="sxs-lookup"><span data-stu-id="250ba-126">Returns a pointer to an [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) structure containing pointers to the context record and the exception record.</span></span> <span data-ttu-id="250ba-127">Cette fonction ne peut être appelée qu’à partir de l’expression de filtre d’un gestionnaire d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="250ba-127">This function can be called only from within the filter expression of an exception handler.</span></span> |
| [<span data-ttu-id="250ba-128">**AbnormalTermination**</span><span class="sxs-lookup"><span data-stu-id="250ba-128">**AbnormalTermination**</span></span>](abnormaltermination.md)         | <span data-ttu-id="250ba-129">Indique si le workflow de contrôle a quitté le bloc **\_ \_ try** associé de manière séquentielle après l’exécution de la dernière instruction dans le bloc.</span><span class="sxs-lookup"><span data-stu-id="250ba-129">Indicates whether the flow of control left the associated **\_\_try** block sequentially after executing the last statement in the block.</span></span> <span data-ttu-id="250ba-130">Cette fonction ne peut être appelée qu’à partir du bloc **\_ \_ finally** d’un gestionnaire de terminaisons.</span><span class="sxs-lookup"><span data-stu-id="250ba-130">This function can be called only from within the **\_\_finally** block of a termination handler.</span></span>              |



 

 

 



