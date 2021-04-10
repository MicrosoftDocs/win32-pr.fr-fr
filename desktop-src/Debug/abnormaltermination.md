---
description: Indique si le \_ \_ bloc try d’un gestionnaire de terminaisons se termine normalement. La fonction ne peut être appelée qu’à partir du \_ \_ bloc finally d’un gestionnaire de terminaisons.
ms.assetid: 0ddaef1f-03f0-45fc-9c5e-8d6a26a73245
title: AbnormalTermination macro)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbnormalTermination
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7c4869f36d8ba70c8dcd8ca526949d489f455e8c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950782"
---
# <a name="abnormaltermination-macro"></a><span data-ttu-id="004b8-104">AbnormalTermination macro)</span><span class="sxs-lookup"><span data-stu-id="004b8-104">AbnormalTermination macro</span></span>

<span data-ttu-id="004b8-105">Indique si le bloc **\_ \_ try** d’un gestionnaire de terminaisons se termine normalement.</span><span class="sxs-lookup"><span data-stu-id="004b8-105">Indicates whether the **\_\_try** block of a termination handler terminated normally.</span></span> <span data-ttu-id="004b8-106">La fonction ne peut être appelée qu’à partir du bloc **\_ \_ finally** d’un gestionnaire de terminaisons.</span><span class="sxs-lookup"><span data-stu-id="004b8-106">The function can be called only from within the **\_\_finally** block of a termination handler.</span></span>

> [!Note]  
> <span data-ttu-id="004b8-107">Le compilateur d’optimisation Microsoft C/C++ interprète cette fonction comme un mot clé, et son utilisation en dehors de la syntaxe de gestion des exceptions appropriée génère une erreur du compilateur.</span><span class="sxs-lookup"><span data-stu-id="004b8-107">The Microsoft C/C++ Optimizing Compiler interprets this function as a keyword, and its use outside the appropriate exception-handling syntax generates a compiler error.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="004b8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="004b8-108">Syntax</span></span>


```C++
BOOL AbnormalTermination(void);
```



## <a name="parameters"></a><span data-ttu-id="004b8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="004b8-109">Parameters</span></span>

<span data-ttu-id="004b8-110">Cette macro n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="004b8-110">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="004b8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="004b8-111">Return value</span></span>

<span data-ttu-id="004b8-112">Si le bloc **\_ \_ try** s’est arrêté anormalement, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="004b8-112">If the **\_\_try** block terminated abnormally, the return value is nonzero.</span></span>

<span data-ttu-id="004b8-113">Si le bloc **\_ \_ try** s’est arrêté normalement, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="004b8-113">If the **\_\_try** block terminated normally, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="004b8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="004b8-114">Remarks</span></span>

<span data-ttu-id="004b8-115">Le bloc **\_ \_ try** se termine normalement uniquement si l’exécution laisse le bloc séquentiellement après l’exécution de la dernière instruction dans le bloc.</span><span class="sxs-lookup"><span data-stu-id="004b8-115">The **\_\_try** block terminates normally only if execution leaves the block sequentially after executing the last statement in the block.</span></span> <span data-ttu-id="004b8-116">Les instructions (telles que **Return**, **goto**, **continue** ou **break**) qui forcent l’exécution à quitter le bloc **\_ \_ try** entraînent un arrêt anormal du bloc.</span><span class="sxs-lookup"><span data-stu-id="004b8-116">Statements (such as **return**, **goto**, **continue**, or **break**) that cause execution to leave the **\_\_try** block result in abnormal termination of the block.</span></span> <span data-ttu-id="004b8-117">C’est le cas même si une telle instruction est la dernière instruction du bloc **\_ \_ try** .</span><span class="sxs-lookup"><span data-stu-id="004b8-117">This is the case even if such a statement is the last statement in the **\_\_try** block.</span></span>

<span data-ttu-id="004b8-118">Un arrêt anormal d’un bloc **\_ \_ try** amène le système à parcourir tous les frames de pile pour déterminer si des gestionnaires de terminaison doivent être appelés.</span><span class="sxs-lookup"><span data-stu-id="004b8-118">Abnormal termination of a **\_\_try** block causes the system to search backward through all stack frames to determine whether any termination handlers must be called.</span></span> <span data-ttu-id="004b8-119">Cela peut entraîner l’exécution de centaines d’instructions. il est donc important d’éviter l’arrêt anormal d’un bloc **\_ \_ try** en raison d’une instruction **Return**, **goto**, **continue** ou **break** .</span><span class="sxs-lookup"><span data-stu-id="004b8-119">This can result in the execution of hundreds of instructions, so it is important to avoid abnormal termination of a **\_\_try** block due to a **return**, **goto**, **continue**, or **break** statement.</span></span> <span data-ttu-id="004b8-120">Notez que ces instructions ne génèrent pas d’exception, même si l’arrêt est anormal.</span><span class="sxs-lookup"><span data-stu-id="004b8-120">Note that these statements do not generate an exception, even though the termination is abnormal.</span></span>

<span data-ttu-id="004b8-121">Pour éviter un arrêt anormal, l’exécution doit se poursuivre jusqu’à la fin du bloc.</span><span class="sxs-lookup"><span data-stu-id="004b8-121">To avoid abnormal termination, execution should continue to the end of the block.</span></span> <span data-ttu-id="004b8-122">Vous pouvez également exécuter l’instruction **\_ \_ Leave** .</span><span class="sxs-lookup"><span data-stu-id="004b8-122">You can also execute the **\_\_leave** statement.</span></span> <span data-ttu-id="004b8-123">L’instruction **\_ \_ Leave** autorise l’arrêt immédiat du bloc **\_ \_ try** sans entraîner un arrêt anormal et une baisse des performances.</span><span class="sxs-lookup"><span data-stu-id="004b8-123">The **\_\_leave** statement allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span> <span data-ttu-id="004b8-124">Consultez la documentation de votre compilateur pour déterminer si l’instruction **\_ \_ Leave** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="004b8-124">Check your compiler documentation to determine if the **\_\_leave** statement is supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="004b8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="004b8-125">Requirements</span></span>



| <span data-ttu-id="004b8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="004b8-126">Requirement</span></span> | <span data-ttu-id="004b8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="004b8-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="004b8-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="004b8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="004b8-129">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="004b8-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="004b8-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="004b8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="004b8-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="004b8-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="004b8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="004b8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="004b8-133">Fonctions de gestion structurée des exceptions</span><span class="sxs-lookup"><span data-stu-id="004b8-133">Structured Exception Handling Functions</span></span>](structured-exception-handling-functions.md)
</dt> <dt>

[<span data-ttu-id="004b8-134">Vue d’ensemble de la gestion structurée des exceptions</span><span class="sxs-lookup"><span data-stu-id="004b8-134">Structured Exception Handling Overview</span></span>](structured-exception-handling.md)
</dt> </dl>

 

 




