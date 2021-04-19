---
description: À partir de TAPI 2,1, les dll de l’interface utilisateur du fournisseur de services de téléphonie peuvent être utilisées pour gérer et afficher des boîtes de dialogue. L’interface TAPI charge la DLL dans le processus d’une application qui appelle l’une des fonctions du fournisseur de services qui peut afficher une boîte de dialogue.
ms.assetid: 0a0320d1-fb75-405e-8074-b37cef956c9f
title: Nouveautés de TSPI version 2,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51642fb9ac960732f8e4a56805652333d0c32468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522713"
---
# <a name="whats-new-for-tspi-version-21"></a><span data-ttu-id="d52bc-104">Nouveautés de TSPI version 2,1</span><span class="sxs-lookup"><span data-stu-id="d52bc-104">What's New for TSPI Version 2.1</span></span>

<span data-ttu-id="d52bc-105">À partir de TAPI 2,1, les dll de l’interface utilisateur du fournisseur de services de téléphonie peuvent être utilisées pour gérer et afficher des boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d52bc-105">Starting with TAPI 2.1, the telephony service provider user interface DLLs can be used to manage and display dialog boxes.</span></span> <span data-ttu-id="d52bc-106">L’interface TAPI charge la DLL dans le processus d’une application qui appelle l’une des fonctions du fournisseur de services qui peut afficher une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d52bc-106">TAPI loads the DLL into the process of an application that invokes any of the service provider functions that can display a dialog.</span></span>

<span data-ttu-id="d52bc-107">À partir de TAPI 2,1, les gestionnaires de demandes de proxy peuvent être implémentés.</span><span class="sxs-lookup"><span data-stu-id="d52bc-107">Starting with TAPI 2.1, proxy request handlers can be implemented.</span></span> <span data-ttu-id="d52bc-108">Un gestionnaire est une application de téléphonie complète qui s’exécute normalement sur un serveur de téléphonie et fournit des services qui sont implémentés de manière plus appropriée dans une application qu’un pilote.</span><span class="sxs-lookup"><span data-stu-id="d52bc-108">A handler is a full telephony application that normally executes on a telephony server and provides services that are more appropriately implemented in an application than a driver.</span></span>

<span data-ttu-id="d52bc-109">Les fonctions et les messages qui ont été nouveaux ou modifiés pour TSPI version 2,1 sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="d52bc-109">Functions and messages that were new or changed for TSPI version 2.1 are as follows:</span></span>

-   [<span data-ttu-id="d52bc-110">**TSPI_lineConditionalMediaDetection**</span><span class="sxs-lookup"><span data-stu-id="d52bc-110">**TSPI_lineConditionalMediaDetection**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   <span data-ttu-id="d52bc-111">**TSPI_lineDropNoOwner**:**obsolète**</span><span class="sxs-lookup"><span data-stu-id="d52bc-111">**TSPI_lineDropNoOwner**—**obsolete**</span></span>
-   <span data-ttu-id="d52bc-112">**TSPI_lineDropOnClose**:**obsolète**</span><span class="sxs-lookup"><span data-stu-id="d52bc-112">**TSPI_lineDropOnClose**—**obsolete**</span></span>
-   [<span data-ttu-id="d52bc-113">**TSPI_lineGetID**</span><span class="sxs-lookup"><span data-stu-id="d52bc-113">**TSPI_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [<span data-ttu-id="d52bc-114">**TSPI_lineSetCallData**</span><span class="sxs-lookup"><span data-stu-id="d52bc-114">**TSPI_lineSetCallData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [<span data-ttu-id="d52bc-115">**TSPI_lineSetCallQualityOfService**</span><span class="sxs-lookup"><span data-stu-id="d52bc-115">**TSPI_lineSetCallQualityOfService**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [<span data-ttu-id="d52bc-116">**TSPI_lineSetCallTreatment**</span><span class="sxs-lookup"><span data-stu-id="d52bc-116">**TSPI_lineSetCallTreatment**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [<span data-ttu-id="d52bc-117">**TSPI_lineSetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="d52bc-117">**TSPI_lineSetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [<span data-ttu-id="d52bc-118">**TSPI_phoneGetID**</span><span class="sxs-lookup"><span data-stu-id="d52bc-118">**TSPI_phoneGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonegetid)
-   [<span data-ttu-id="d52bc-119">**TSPI_providerInit**</span><span class="sxs-lookup"><span data-stu-id="d52bc-119">**TSPI_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)
-   [<span data-ttu-id="d52bc-120">**TSPI_providerShutdown**</span><span class="sxs-lookup"><span data-stu-id="d52bc-120">**TSPI_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)
-   <span data-ttu-id="d52bc-121">[**LINE_GATHERDIGITS**](/previous-versions/windows/desktop/legacy/ms725229(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d52bc-121">[**LINE_GATHERDIGITS**](/previous-versions/windows/desktop/legacy/ms725229(v=vs.85))</span></span>
-   <span data-ttu-id="d52bc-122">[**LINE_GENERATE**](/previous-versions/windows/desktop/legacy/ms725230(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d52bc-122">[**LINE_GENERATE**](/previous-versions/windows/desktop/legacy/ms725230(v=vs.85))</span></span>
-   <span data-ttu-id="d52bc-123">[**LINE_MONITORDIGITS**](/previous-versions/windows/desktop/legacy/ms725232(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d52bc-123">[**LINE_MONITORDIGITS**](/previous-versions/windows/desktop/legacy/ms725232(v=vs.85))</span></span>
-   <span data-ttu-id="d52bc-124">[**LINE_MONITORMEDIA**](/previous-versions/windows/desktop/legacy/ms725233(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d52bc-124">[**LINE_MONITORMEDIA**](/previous-versions/windows/desktop/legacy/ms725233(v=vs.85))</span></span>
-   <span data-ttu-id="d52bc-125">[**LINE_MONITORTONE**](/previous-versions/windows/desktop/legacy/ms725234(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d52bc-125">[**LINE_MONITORTONE**](/previous-versions/windows/desktop/legacy/ms725234(v=vs.85))</span></span>
-   <span data-ttu-id="d52bc-126">[**LINE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725237(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d52bc-126">[**LINE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725237(v=vs.85))</span></span>
-   <span data-ttu-id="d52bc-127">[**PHONE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725260(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d52bc-127">[**PHONE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725260(v=vs.85))</span></span>

<span data-ttu-id="d52bc-128">La DLL de l’interface utilisateur du fournisseur de services de téléphonie fournit un moyen d’autoriser l’interaction de l’utilisateur dans le contexte de l’application plutôt que dans le fournisseur de services lui-même.</span><span class="sxs-lookup"><span data-stu-id="d52bc-128">The Telephony service provider user interface DLL provides a means of allowing user interaction within the context of the application rather than the service provider itself.</span></span> <span data-ttu-id="d52bc-129">TSPI version 2,1 a fourni les nouvelles fonctions, messages et structures suivants pour l’implémentation :</span><span class="sxs-lookup"><span data-stu-id="d52bc-129">TSPI version 2.1 delivered the following new functions, messages, and structures for implementation:</span></span>

-   [<span data-ttu-id="d52bc-130">**TSPI_providerFreeDialogInstance**</span><span class="sxs-lookup"><span data-stu-id="d52bc-130">**TSPI_providerFreeDialogInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance)
-   [<span data-ttu-id="d52bc-131">**TSPI_providerGenericDialogData**</span><span class="sxs-lookup"><span data-stu-id="d52bc-131">**TSPI_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata)
-   [<span data-ttu-id="d52bc-132">**TSPI_providerUIIdentify**</span><span class="sxs-lookup"><span data-stu-id="d52bc-132">**TSPI_providerUIIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify)
-   [<span data-ttu-id="d52bc-133">**TUISPI_lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="d52bc-133">**TUISPI_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)
-   [<span data-ttu-id="d52bc-134">**TUISPI_lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="d52bc-134">**TUISPI_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit)
-   [<span data-ttu-id="d52bc-135">**TUISPI_phoneConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="d52bc-135">**TUISPI_phoneConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog)
-   [<span data-ttu-id="d52bc-136">**TUISPI_providerConfig**</span><span class="sxs-lookup"><span data-stu-id="d52bc-136">**TUISPI_providerConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig)
-   [<span data-ttu-id="d52bc-137">**TUISPI_providerGenericDialog**</span><span class="sxs-lookup"><span data-stu-id="d52bc-137">**TUISPI_providerGenericDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog)
-   [<span data-ttu-id="d52bc-138">**TUISPI_providerGenericDialogData**</span><span class="sxs-lookup"><span data-stu-id="d52bc-138">**TUISPI_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
-   [<span data-ttu-id="d52bc-139">**TUISPI_providerInstall**</span><span class="sxs-lookup"><span data-stu-id="d52bc-139">**TUISPI_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall)
-   [<span data-ttu-id="d52bc-140">**TUISPI_providerRemove**</span><span class="sxs-lookup"><span data-stu-id="d52bc-140">**TUISPI_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)
-   [<span data-ttu-id="d52bc-141">**TUISPICREATEDIALOGINSTANCEPARAMS**</span><span class="sxs-lookup"><span data-stu-id="d52bc-141">**TUISPICREATEDIALOGINSTANCEPARAMS**</span></span>](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
-   [<span data-ttu-id="d52bc-142">**TUISPIDLLCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="d52bc-142">**TUISPIDLLCALLBACK**</span></span>](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
-   [<span data-ttu-id="d52bc-143">**LINE_CREATEDIALOGINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="d52bc-143">**LINE_CREATEDIALOGINSTANCE**</span></span>](line-createdialoginstance.md)
-   [<span data-ttu-id="d52bc-144">**LINE_SENDDIALOGINSTANCEDATA**</span><span class="sxs-lookup"><span data-stu-id="d52bc-144">**LINE_SENDDIALOGINSTANCEDATA**</span></span>](line-senddialoginstancedata.md)

 

 
