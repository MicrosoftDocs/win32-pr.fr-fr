---
description: Cette section décrit comment imprimer à partir d’un programme Windows natif.
ms.assetid: D0AE8FF8-D02D-43D3-80CA-E13EAA894F87
title: 'Comment : imprimer à partir d’un programme Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84229823944d7f7104da359b953e579f1b21cdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518915"
---
# <a name="how-to-print-from-a-windows-program"></a><span data-ttu-id="9d680-103">Comment : imprimer à partir d’un programme Windows</span><span class="sxs-lookup"><span data-stu-id="9d680-103">How To: Print from a Windows Program</span></span>

<span data-ttu-id="9d680-104">Cette section décrit comment imprimer à partir d’un programme Windows natif.</span><span class="sxs-lookup"><span data-stu-id="9d680-104">This section describes how to print from a native Windows program.</span></span>

## <a name="overview"></a><span data-ttu-id="9d680-105">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="9d680-105">Overview</span></span>

<span data-ttu-id="9d680-106">L’impression fait généralement partie intégrante d’un programme Windows natif.</span><span class="sxs-lookup"><span data-stu-id="9d680-106">Printing is usually an integral part of a native Windows program.</span></span> <span data-ttu-id="9d680-107">Par conséquent, il ne s’agit pas d’une fonctionnalité que vous pouvez ajouter facilement après avoir écrit le programme.</span><span class="sxs-lookup"><span data-stu-id="9d680-107">Therefore, it is not a feature that you can add easily after you have written the program.</span></span> <span data-ttu-id="9d680-108">Cela dit, si le programme est conçu pour utiliser des documents XPS, il n’aura pas besoin d’une grande quantité de code pour afficher le contenu du document en vue de son impression.</span><span class="sxs-lookup"><span data-stu-id="9d680-108">That being said, if the program is designed to use XPS documents it will not need much, if any, additional code to render the document content for printing.</span></span> <span data-ttu-id="9d680-109">Les documents XPS de l’application peuvent être envoyés directement à une imprimante disposant d’un pilote d’imprimante XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="9d680-109">The XPS documents of the application can be sent directly to a printer that has an XPSDrv printer driver.</span></span>

<span data-ttu-id="9d680-110">Utilisez l' [API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) pour créer le contenu du document et l' [API d’impression XPS](xps-printing.md) pour envoyer le contenu du document à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="9d680-110">Use the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) to create the document content and the [XPS Print API](xps-printing.md) to send the document content to the printer.</span></span> <span data-ttu-id="9d680-111">L’API d’impression XPS traite le contenu du document pour l’imprimante de destination.</span><span class="sxs-lookup"><span data-stu-id="9d680-111">The XPS Print API processes the document content for the destination printer.</span></span> <span data-ttu-id="9d680-112">Si l’imprimante sélectionnée possède un pilote d’imprimante XPSDrv, le document est envoyé à l’imprimante sans conversion supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="9d680-112">If the selected printer has an XPSDrv printer driver, the document will be sent to the printer without any additional conversion.</span></span> <span data-ttu-id="9d680-113">Si l’imprimante sélectionnée possède un pilote d’imprimante GDI, le programme peut également envoyer le contenu à l’imprimante, et l’API d’impression XPS convertit le contenu du document afin qu’il soit compatible avec le pilote d’imprimante GDI.</span><span class="sxs-lookup"><span data-stu-id="9d680-113">If the selected printer has a GDI-based printer driver, the program can also send the content to the printer, and the XPS Print API converts the document content so that it will be compatible with the GDI-based printer driver.</span></span> <span data-ttu-id="9d680-114">Dans les deux cas, le traitement effectué par l’application est le même.</span><span class="sxs-lookup"><span data-stu-id="9d680-114">In either case, the processing that the application performs is the same.</span></span>

## <a name="printing-tasks"></a><span data-ttu-id="9d680-115">Tâches d’impression</span><span class="sxs-lookup"><span data-stu-id="9d680-115">Printing tasks</span></span>

<span data-ttu-id="9d680-116">Les rubriques suivantes décrivent les étapes de base de l’impression du contenu d’un programme.</span><span class="sxs-lookup"><span data-stu-id="9d680-116">The following topics describe the basic steps of printing program content.</span></span>

1.  <span data-ttu-id="9d680-117">**Collecter les informations de travail d’impression de l’utilisateur.**</span><span class="sxs-lookup"><span data-stu-id="9d680-117">**Collect print job information from user.**</span></span>

    <span data-ttu-id="9d680-118">En règle générale, un utilisateur lance un travail d’impression lorsqu’il sélectionne l’option d’impression dans un menu et le programme affiche une boîte de dialogue Imprimer pour collecter les détails du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="9d680-118">Typically, a user initiates a print job when they select the print option from a menu and the program displays a print dialog box to collect the details of the print job.</span></span> <span data-ttu-id="9d680-119">L’utilisateur sélectionne généralement l’imprimante, le nombre de copies et les détails de configuration de l’imprimante, tels que l’impression recto verso et l’agrafage.</span><span class="sxs-lookup"><span data-stu-id="9d680-119">The user typically selects the printer, the number of copies, and printer configuration details such as two-sided printing and stapling.</span></span>

    <span data-ttu-id="9d680-120">Pour plus d’informations sur la procédure à suivre, consultez [Comment : collecter des informations de travail d’impression à partir de l’utilisateur](preparing-to-print.md).</span><span class="sxs-lookup"><span data-stu-id="9d680-120">For information about how to do this, see [How To: Collect Print Job Information from the User](preparing-to-print.md).</span></span>

2.  <span data-ttu-id="9d680-121">**Créer un indicateur de progression.**</span><span class="sxs-lookup"><span data-stu-id="9d680-121">**Create progress indicator.**</span></span>

    <span data-ttu-id="9d680-122">Un indicateur de progression fournit à l’utilisateur des commentaires sur la progression du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="9d680-122">A progress indicator provides the user with feedback about how the print job is progressing.</span></span> <span data-ttu-id="9d680-123">L’indicateur de progression peut être une barre de progression qui fait partie d’une boîte de dialogue qui comprend le bouton **Annuler** pour le travail, ou il peut s’agir d’une barre de progression dans la barre d’État en bas de la fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="9d680-123">The progress indicator can be a progress bar that is part of a dialog box that includes the **Cancel** button for the job, or it can be a progress bar in the status bar at the bottom of the main window.</span></span>

    <span data-ttu-id="9d680-124">Pour plus d’informations sur le fonctionnement de l’indicateur de progression, consultez [procédure : afficher la progression du travail d’impression](cancel-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="9d680-124">For information about the progress indicator works, see [How To: Display the Print Job Progress](cancel-dialog-box.md).</span></span>

    <span data-ttu-id="9d680-125">Pour plus d’informations sur l’affichage de la progression du travail d’impression, consultez les informations dans les instructions de développement de l' [interface utilisateur de l’application Windows](/windows/desktop/windows-application-ui-development) .</span><span class="sxs-lookup"><span data-stu-id="9d680-125">For more ideas about how to display the progress of the print job, see the information in the [Windows Application UI Development](/windows/desktop/windows-application-ui-development) guidelines.</span></span>

3.  <span data-ttu-id="9d680-126">**Démarrez le thread d’impression.**</span><span class="sxs-lookup"><span data-stu-id="9d680-126">**Start the printing thread.**</span></span>

    <span data-ttu-id="9d680-127">Une fois que le programme a collecté les informations du travail d’impression auprès de l’utilisateur, il peut démarrer le thread d’impression pour effectuer le traitement réel du document en vue de l’impression.</span><span class="sxs-lookup"><span data-stu-id="9d680-127">After the program has collected the print job information from the user, it can start the printing thread to perform the actual processing of the document for printing.</span></span>

    <span data-ttu-id="9d680-128">Pour plus d’informations sur le thread d’impression, consultez [procédure : Démarrer et arrêter un thread d’impression](how-to--start-and-stop-a-printing-thread.md).</span><span class="sxs-lookup"><span data-stu-id="9d680-128">For information about the printing thread, see [How To: Start and Stop a Printing Thread](how-to--start-and-stop-a-printing-thread.md).</span></span>

4.  <span data-ttu-id="9d680-129">**Affichez les données du travail d’impression.**</span><span class="sxs-lookup"><span data-stu-id="9d680-129">**Render print job data.**</span></span>

    <span data-ttu-id="9d680-130">Le thread d’impression restitue les données du document pour l’impression.</span><span class="sxs-lookup"><span data-stu-id="9d680-130">The printing thread renders the document data for printing.</span></span> <span data-ttu-id="9d680-131">Vous devez décomposer ce traitement en étapes de traitement discrètes afin que l’utilisateur puisse interrompre le traitement et annuler le travail, ainsi que pour ne pas autoriser le thread de traitement à bloquer d’autres threads et processus.</span><span class="sxs-lookup"><span data-stu-id="9d680-131">You should break down this processing into discrete processing steps so that the user can interrupt the processing and cancel the job as well as to not allow the processing thread to block other threads and processes.</span></span>

    <span data-ttu-id="9d680-132">Pour plus d’informations sur le rendu des données du travail d’impression, consultez [Comment : afficher des données de travail d’impression](how-to--render-the-print-job-data.md).</span><span class="sxs-lookup"><span data-stu-id="9d680-132">For information about how the renders the print job data, see [How To: Render Print Job Data](how-to--render-the-print-job-data.md).</span></span>

5.  <span data-ttu-id="9d680-133">**Surveiller la progression du travail d’impression.**</span><span class="sxs-lookup"><span data-stu-id="9d680-133">**Monitor print job progress.**</span></span>

    <span data-ttu-id="9d680-134">À mesure que chaque étape de traitement est effectuée, mettez à jour la barre de progression pour informer l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="9d680-134">As each processing step is performed, update the progress bar to inform the use.</span></span> <span data-ttu-id="9d680-135">Calculez les étapes de traitement pour terminer la tâche demandée, puis mettre à jour la barre de progression à mesure que ces étapes sont effectuées.</span><span class="sxs-lookup"><span data-stu-id="9d680-135">Compute the processing steps to complete the requested job and then updates the progress bar as those steps are performed.</span></span>

6.  <span data-ttu-id="9d680-136">**Fermer le travail d’impression et terminer le thread d’impression.**</span><span class="sxs-lookup"><span data-stu-id="9d680-136">**Close print job and terminate printing thread.**</span></span>

    <span data-ttu-id="9d680-137">Une fois que le programme a envoyé le travail d’impression à l’imprimante, ou si l’utilisateur a annulé le travail d’impression, vous devez fermer le travail d’impression et libérer les ressources utilisées par le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="9d680-137">After the program has sent the print job to the printer, or if the user has cancelled the print job, you must close the print job and release the resources used by the print job.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d680-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9d680-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d680-139">Procédure : collecter des informations de travail d’impression à partir de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="9d680-139">How To: Collect Print Job Information from the User</span></span>](preparing-to-print.md)
</dt> </dl>

 

 
