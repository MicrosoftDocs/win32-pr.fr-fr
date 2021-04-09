---
description: Récupère une description indépendante de l’ordinateur d’une exception et des informations sur l’état de l’ordinateur qui existe pour le thread lorsque l’exception se produit. Cette fonction ne peut être appelée qu’à partir de l’expression de filtre d’un gestionnaire d’exceptions.
ms.assetid: e982794a-d5f1-4fb4-a2b9-aa8da18cb8ae
title: GetExceptionInformation macro)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetExceptionInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 243831a94a26b86df29d3a50413bfa9d6830a0e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748892"
---
# <a name="getexceptioninformation-macro"></a><span data-ttu-id="51a12-104">GetExceptionInformation macro)</span><span class="sxs-lookup"><span data-stu-id="51a12-104">GetExceptionInformation macro</span></span>

<span data-ttu-id="51a12-105">Récupère une description indépendante de l’ordinateur d’une exception et des informations sur l’état de l’ordinateur qui existe pour le thread lorsque l’exception se produit.</span><span class="sxs-lookup"><span data-stu-id="51a12-105">Retrieves a computer-independent description of an exception, and information about the computer state that exists for the thread when the exception occurs.</span></span> <span data-ttu-id="51a12-106">Cette fonction ne peut être appelée qu’à partir de l’expression de filtre d’un gestionnaire d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="51a12-106">This function can be called only from within the filter expression of an exception handler.</span></span>

> [!Note]  
> <span data-ttu-id="51a12-107">Le compilateur d’optimisation Microsoft C/C++ interprète cette fonction comme un mot clé, et son utilisation en dehors de la syntaxe de gestion des exceptions appropriée génère une erreur du compilateur.</span><span class="sxs-lookup"><span data-stu-id="51a12-107">The Microsoft C/C++ Optimizing Compiler interprets this function as a keyword, and its use outside the appropriate exception-handling syntax generates a compiler error.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="51a12-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51a12-108">Syntax</span></span>


```C++
LPEXCEPTION_POINTERS GetExceptionInformation(void);
```



## <a name="parameters"></a><span data-ttu-id="51a12-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51a12-109">Parameters</span></span>

<span data-ttu-id="51a12-110">Cette macro n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="51a12-110">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="51a12-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="51a12-111">Return value</span></span>

<span data-ttu-id="51a12-112">Pointeur vers une structure [**de \_ pointeurs d’exception**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) qui contient des pointeurs vers les deux structures suivantes :</span><span class="sxs-lookup"><span data-stu-id="51a12-112">A pointer to an [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) structure that contains pointers to the following two structures:</span></span>

-   <span data-ttu-id="51a12-113">[**Exception \_**](/windows/desktop/api/WinNT/ns-winnt-exception_record) Structure d’enregistrement qui contient une description de l’exception.</span><span class="sxs-lookup"><span data-stu-id="51a12-113">[**EXCEPTION\_RECORD**](/windows/desktop/api/WinNT/ns-winnt-exception_record) structure that contains a description of the exception.</span></span>
-   <span data-ttu-id="51a12-114">Structure de [**contexte**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) qui contient les informations sur l’état de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="51a12-114">[**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure that contains the computer state information.</span></span>

## <a name="remarks"></a><span data-ttu-id="51a12-115">Notes</span><span class="sxs-lookup"><span data-stu-id="51a12-115">Remarks</span></span>

<span data-ttu-id="51a12-116">L’expression de filtre (à partir de laquelle la fonction est appelée) est évaluée si une exception se produit pendant l’exécution du bloc **\_ \_ try** et détermine si le bloc **\_ \_ except** est exécuté ou non.</span><span class="sxs-lookup"><span data-stu-id="51a12-116">The filter expression (from which the function is called) is evaluated if an exception occurs during execution of the **\_\_try** block, and it determines whether or not the **\_\_except** block is executed.</span></span>

<span data-ttu-id="51a12-117">L’expression de filtre peut appeler une fonction de filtre.</span><span class="sxs-lookup"><span data-stu-id="51a12-117">The filter expression can invoke a filter function.</span></span> <span data-ttu-id="51a12-118">La fonction de filtre ne peut pas appeler **GetExceptionInformation**.</span><span class="sxs-lookup"><span data-stu-id="51a12-118">The filter function cannot call **GetExceptionInformation**.</span></span> <span data-ttu-id="51a12-119">Toutefois, la valeur de retour de **GetExceptionInformation** peut être transmise en tant que paramètre à une fonction de filtre.</span><span class="sxs-lookup"><span data-stu-id="51a12-119">However, the return value of **GetExceptionInformation** can be passed as a parameter to a filter function.</span></span>

<span data-ttu-id="51a12-120">Pour passer les informations relatives aux [**\_ pointeurs d’exception**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) au bloc de gestionnaire d’exceptions, l’expression de filtre ou la fonction de filtre doit copier le pointeur ou les données dans un stockage sécurisé auquel le gestionnaire peut accéder ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="51a12-120">To pass the [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) information to the exception-handler block, the filter expression or filter function must copy the pointer or the data to safe storage that the handler can later access.</span></span>

<span data-ttu-id="51a12-121">Dans le cas de gestionnaires imbriqués, chaque expression de filtre est évaluée jusqu’à ce qu’elle soit évaluée en tant que **\_ \_ Gestionnaire d’exécution d’exception** ou que **\_ l’exception continue \_ l’exécution**.</span><span class="sxs-lookup"><span data-stu-id="51a12-121">In the case of nested handlers, each filter expression is evaluated until one is evaluated as **EXCEPTION\_EXECUTE\_HANDLER** or **EXCEPTION\_CONTINUE\_EXECUTION**.</span></span> <span data-ttu-id="51a12-122">Chaque expression de filtre peut appeler **GetExceptionInformation** pour recevoir des informations sur les exceptions.</span><span class="sxs-lookup"><span data-stu-id="51a12-122">Each filter expression can invoke **GetExceptionInformation** to get exception information.</span></span>

## <a name="requirements"></a><span data-ttu-id="51a12-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51a12-123">Requirements</span></span>



| <span data-ttu-id="51a12-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51a12-124">Requirement</span></span> | <span data-ttu-id="51a12-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="51a12-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="51a12-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51a12-126">Minimum supported client</span></span><br/> | <span data-ttu-id="51a12-127">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51a12-127">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="51a12-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51a12-128">Minimum supported server</span></span><br/> | <span data-ttu-id="51a12-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51a12-129">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="51a12-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51a12-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51a12-131">**CONTEXTE**</span><span class="sxs-lookup"><span data-stu-id="51a12-131">**CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)
</dt> <dt>

[<span data-ttu-id="51a12-132">**\_pointeurs d’exception**</span><span class="sxs-lookup"><span data-stu-id="51a12-132">**EXCEPTION\_POINTERS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)
</dt> <dt>

[<span data-ttu-id="51a12-133">**enregistrement d’EXCEPTION \_**</span><span class="sxs-lookup"><span data-stu-id="51a12-133">**EXCEPTION\_RECORD**</span></span>](/windows/desktop/api/WinNT/ns-winnt-exception_record)
</dt> <dt>

[<span data-ttu-id="51a12-134">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="51a12-134">**GetExceptionCode**</span></span>](getexceptioncode.md)
</dt> <dt>

[<span data-ttu-id="51a12-135">**GetXStateFeaturesMask**</span><span class="sxs-lookup"><span data-stu-id="51a12-135">**GetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)
</dt> <dt>

[<span data-ttu-id="51a12-136">Fonctions de gestion structurée des exceptions</span><span class="sxs-lookup"><span data-stu-id="51a12-136">Structured Exception Handling Functions</span></span>](structured-exception-handling-functions.md)
</dt> <dt>

[<span data-ttu-id="51a12-137">Vue d’ensemble de la gestion structurée des exceptions</span><span class="sxs-lookup"><span data-stu-id="51a12-137">Structured Exception Handling Overview</span></span>](structured-exception-handling.md)
</dt> <dt>

[<span data-ttu-id="51a12-138">Activer la prise en charge de Windows pour Intel AVX</span><span class="sxs-lookup"><span data-stu-id="51a12-138">Enable Windows Support for Intel AVX</span></span>](../win7appqual/enable-windows-7-support-for-intel-avx.md)
</dt> </dl>

 

 
