---
description: Les fonctions suivantes sont utilisées dans la gestion structurée des exceptions.
ms.assetid: 61cf055b-eb9a-4e56-9d36-21fc95adea77
title: Fonctions de gestion structurée des exceptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70b431be2961a55bba28bdfe07723e93b95ac69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514925"
---
# <a name="structured-exception-handling-functions"></a><span data-ttu-id="9ee94-103">Fonctions de gestion structurée des exceptions</span><span class="sxs-lookup"><span data-stu-id="9ee94-103">Structured Exception Handling Functions</span></span>

<span data-ttu-id="9ee94-104">Les fonctions suivantes sont utilisées dans la gestion structurée des exceptions.</span><span class="sxs-lookup"><span data-stu-id="9ee94-104">The following functions are used in structured exception handling.</span></span>

-   [<span data-ttu-id="9ee94-105">**AbnormalTermination**</span><span class="sxs-lookup"><span data-stu-id="9ee94-105">**AbnormalTermination**</span></span>](abnormaltermination.md)

    <span data-ttu-id="9ee94-106">Indique si le bloc **\_ \_ try** d’un gestionnaire de terminaisons se termine normalement.</span><span class="sxs-lookup"><span data-stu-id="9ee94-106">Indicates whether the **\_\_try** block of a termination handler terminated normally.</span></span>

-   [<span data-ttu-id="9ee94-107">**AddVectoredContinueHandler**</span><span class="sxs-lookup"><span data-stu-id="9ee94-107">**AddVectoredContinueHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler)

    <span data-ttu-id="9ee94-108">Inscrit un gestionnaire continue vectorisé.</span><span class="sxs-lookup"><span data-stu-id="9ee94-108">Registers a vectored continue handler.</span></span>

-   [<span data-ttu-id="9ee94-109">**AddVectoredExceptionHandler**</span><span class="sxs-lookup"><span data-stu-id="9ee94-109">**AddVectoredExceptionHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler)

    <span data-ttu-id="9ee94-110">Inscrit un gestionnaire d’exceptions vectorisées.</span><span class="sxs-lookup"><span data-stu-id="9ee94-110">Registers a vectored exception handler.</span></span>

-   [<span data-ttu-id="9ee94-111">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="9ee94-111">**GetExceptionCode**</span></span>](getexceptioncode.md)

    <span data-ttu-id="9ee94-112">Récupère un code qui identifie le type d’exception qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="9ee94-112">Retrieves a code that identifies the type of exception that occurred.</span></span>

-   [<span data-ttu-id="9ee94-113">**GetExceptionInformation**</span><span class="sxs-lookup"><span data-stu-id="9ee94-113">**GetExceptionInformation**</span></span>](getexceptioninformation.md)

    <span data-ttu-id="9ee94-114">Récupère une description indépendante de l’ordinateur d’une exception et des informations sur l’état de l’ordinateur qui existait pour le thread lorsque l’exception s’est produite.</span><span class="sxs-lookup"><span data-stu-id="9ee94-114">Retrieves a machine-independent description of an exception, and information about the machine state that existed for the thread when the exception occurred.</span></span>

-   [<span data-ttu-id="9ee94-115">**RaiseException**</span><span class="sxs-lookup"><span data-stu-id="9ee94-115">**RaiseException**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)

    <span data-ttu-id="9ee94-116">Lève une exception dans le thread appelant.</span><span class="sxs-lookup"><span data-stu-id="9ee94-116">Raises an exception in the calling thread.</span></span>

-   [<span data-ttu-id="9ee94-117">**RemoveVectoredContinueHandler**</span><span class="sxs-lookup"><span data-stu-id="9ee94-117">**RemoveVectoredContinueHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

    <span data-ttu-id="9ee94-118">Annule l’inscription d’un gestionnaire de continuation vectorisé.</span><span class="sxs-lookup"><span data-stu-id="9ee94-118">Unregisters a vectored continue handler.</span></span>

-   [<span data-ttu-id="9ee94-119">**RemoveVectoredExceptionHandler**</span><span class="sxs-lookup"><span data-stu-id="9ee94-119">**RemoveVectoredExceptionHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

    <span data-ttu-id="9ee94-120">Annule l’inscription d’un gestionnaire d’exceptions vectorisées.</span><span class="sxs-lookup"><span data-stu-id="9ee94-120">Unregisters a vectored exception handler.</span></span>

-   [<span data-ttu-id="9ee94-121">**RtlAddGrowableFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="9ee94-121">**RtlAddGrowableFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtladdgrowablefunctiontable)

    <span data-ttu-id="9ee94-122">Informe le système d’une table de fonctions dynamiques représentant une région de mémoire contenant du code.</span><span class="sxs-lookup"><span data-stu-id="9ee94-122">Informs the system of a dynamic function table representing a region of memory containing code.</span></span>

-   [<span data-ttu-id="9ee94-123">**RtlDeleteGrowableFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="9ee94-123">**RtlDeleteGrowableFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtldeletegrowablefunctiontable)

    <span data-ttu-id="9ee94-124">Informe le système qu’une table de fonctions dynamiques précédemment signalée n’est plus utilisée.</span><span class="sxs-lookup"><span data-stu-id="9ee94-124">Informs the system that a previously reported dynamic function table is no longer in use.</span></span>

-   [<span data-ttu-id="9ee94-125">**RtlGrowFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="9ee94-125">**RtlGrowFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlgrowfunctiontable)

    <span data-ttu-id="9ee94-126">Signale que la taille d’une table de fonctions dynamiques a augmenté.</span><span class="sxs-lookup"><span data-stu-id="9ee94-126">Reports that a dynamic function table has increased in size.</span></span>

-   [<span data-ttu-id="9ee94-127">**SetUnhandledExceptionFilter**</span><span class="sxs-lookup"><span data-stu-id="9ee94-127">**SetUnhandledExceptionFilter**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter)

    <span data-ttu-id="9ee94-128">Permet à une application de remplacer le gestionnaire d’exceptions de niveau supérieur de chaque thread et processus.</span><span class="sxs-lookup"><span data-stu-id="9ee94-128">Enables an application to supersede the top-level exception handler of each thread and process.</span></span>

-   [<span data-ttu-id="9ee94-129">**UnhandledExceptionFilter**</span><span class="sxs-lookup"><span data-stu-id="9ee94-129">**UnhandledExceptionFilter**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)

    <span data-ttu-id="9ee94-130">Passe des exceptions non gérées au débogueur, si le processus est en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="9ee94-130">Passes unhandled exceptions to the debugger, if the process is being debugged.</span></span>

-   [<span data-ttu-id="9ee94-131">**VectoredHandler**</span><span class="sxs-lookup"><span data-stu-id="9ee94-131">**VectoredHandler**</span></span>](/windows/desktop/api/WinNT/nc-winnt-pvectored_exception_handler)

    <span data-ttu-id="9ee94-132">Fonction définie par l’application qui sert de gestionnaire d’exceptions vectorisées.</span><span class="sxs-lookup"><span data-stu-id="9ee94-132">An application-defined function that serves as a vectored exception handler.</span></span>

<span data-ttu-id="9ee94-133">Les fonctions suivantes sont utilisées uniquement sur les fenêtres 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9ee94-133">The following functions are used only on 64-bit Windows.</span></span>

-   [<span data-ttu-id="9ee94-134">**RtlAddFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="9ee94-134">**RtlAddFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtladdfunctiontable)

    <span data-ttu-id="9ee94-135">Ajoute une table de fonctions dynamiques à la liste des tables de fonctions dynamiques.</span><span class="sxs-lookup"><span data-stu-id="9ee94-135">Adds a dynamic function table to the dynamic function table list.</span></span>

-   [<span data-ttu-id="9ee94-136">**RtlCaptureContext**</span><span class="sxs-lookup"><span data-stu-id="9ee94-136">**RtlCaptureContext**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlcapturecontext)

    <span data-ttu-id="9ee94-137">Récupère un enregistrement de contexte dans le contexte de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="9ee94-137">Retrieves a context record in the context of the caller.</span></span>

-   [<span data-ttu-id="9ee94-138">**RtlDeleteFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="9ee94-138">**RtlDeleteFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtldeletefunctiontable)

    <span data-ttu-id="9ee94-139">Supprime une table de fonctions dynamiques de la liste des tables de fonctions dynamiques.</span><span class="sxs-lookup"><span data-stu-id="9ee94-139">Removes a dynamic function table from the dynamic function table list.</span></span>

-   [<span data-ttu-id="9ee94-140">**RtlInstallFunctionTableCallback**</span><span class="sxs-lookup"><span data-stu-id="9ee94-140">**RtlInstallFunctionTableCallback**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlinstallfunctiontablecallback)

    <span data-ttu-id="9ee94-141">Ajoute une table de fonctions dynamiques à la liste des tables de fonctions dynamiques.</span><span class="sxs-lookup"><span data-stu-id="9ee94-141">Adds a dynamic function table to the dynamic function table list.</span></span>

-   [<span data-ttu-id="9ee94-142">**RtlRestoreContext**</span><span class="sxs-lookup"><span data-stu-id="9ee94-142">**RtlRestoreContext**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlrestorecontext)

    <span data-ttu-id="9ee94-143">Restaure le contexte de l’appelant à l’enregistrement de contexte spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ee94-143">Restores the context of the caller to the specified context record.</span></span>

 

 
