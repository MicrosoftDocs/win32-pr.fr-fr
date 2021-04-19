---
description: Cette rubrique explique comment afficher la progression du travail d’impression à l’utilisateur et lui attribuer la possibilité d’annuler un travail d’impression en cours.
ms.assetid: 2b7a0ab7-bf7e-473d-ab43-8b79478d4453
title: 'Comment : afficher la progression du travail d’impression'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9effc778f6affaba5b53cbd96a7a428ea5554d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534507"
---
# <a name="how-to-display-the-print-job-progress"></a><span data-ttu-id="83b7f-103">Comment : afficher la progression du travail d’impression</span><span class="sxs-lookup"><span data-stu-id="83b7f-103">How To: Display the Print Job Progress</span></span>

<span data-ttu-id="83b7f-104">Cette rubrique explique comment afficher la progression du travail d’impression à l’utilisateur et lui attribuer la possibilité d’annuler un travail d’impression en cours.</span><span class="sxs-lookup"><span data-stu-id="83b7f-104">This topic describes how to display the print job progress to the user and give them the option to cancel a print job that is currently in progress.</span></span>

## <a name="overview"></a><span data-ttu-id="83b7f-105">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="83b7f-105">Overview</span></span>

<span data-ttu-id="83b7f-106">Une procédure de boîte de dialogue d’avancement de l’impression effectue généralement les fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="83b7f-106">A print progress dialog procedure typically performs the following functions.</span></span>

-   <span data-ttu-id="83b7f-107">Affichez la progression du travail d’impression à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="83b7f-107">Display print job progress to the user.</span></span>
-   <span data-ttu-id="83b7f-108">Démarrez le thread de traitement de l’impression.</span><span class="sxs-lookup"><span data-stu-id="83b7f-108">Start the print processing thread.</span></span>
-   <span data-ttu-id="83b7f-109">Affichez un bouton **Annuler** pour que l’utilisateur puisse arrêter un travail d’impression avant qu’il ne se termine.</span><span class="sxs-lookup"><span data-stu-id="83b7f-109">Display a **Cancel** button so the user can stop a print job before it finishes.</span></span>

<span data-ttu-id="83b7f-110">À proprement parler, la seule chose que la procédure de la boîte de dialogue de progression de l’impression doit faire est d’afficher la progression du travail d’impression à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="83b7f-110">Strictly speaking, the only thing that the print progress dialog box procedure must do is display the print job progress to the user.</span></span> <span data-ttu-id="83b7f-111">Toutefois, étant donné que les deux autres fonctions de la liste précédente sont étroitement liées, elles ont également été incluses dans ce module.</span><span class="sxs-lookup"><span data-stu-id="83b7f-111">However, because the other two functions in the preceding list are closely related, they have also been included in this module.</span></span>

## <a name="displaying-print-job-progress"></a><span data-ttu-id="83b7f-112">Affichage de la progression du travail d’impression</span><span class="sxs-lookup"><span data-stu-id="83b7f-112">Displaying Print Job Progress</span></span>

<span data-ttu-id="83b7f-113">Une procédure de la boîte de dialogue progression de l’impression gère les messages de fenêtre suivants.</span><span class="sxs-lookup"><span data-stu-id="83b7f-113">A print progress dialog box procedure handles the following window messages.</span></span>

-   <span data-ttu-id="83b7f-114">**\_INITDIALOG WM**</span><span class="sxs-lookup"><span data-stu-id="83b7f-114">**WM\_INITDIALOG**</span></span>

    <span data-ttu-id="83b7f-115">Initialise les contrôles que la boîte de dialogue utilise.</span><span class="sxs-lookup"><span data-stu-id="83b7f-115">Initializes the controls that the dialog box uses.</span></span>

-   <span data-ttu-id="83b7f-116">**\_SETCURSOR WM**</span><span class="sxs-lookup"><span data-stu-id="83b7f-116">**WM\_SETCURSOR**</span></span>

    <span data-ttu-id="83b7f-117">Définit le curseur sur un pointeur lorsque l’utilisateur est en mesure d’annuler un travail d’impression, et au curseur d’attente lorsque le travail d’impression se trouve à un point où il ne peut pas être annulé.</span><span class="sxs-lookup"><span data-stu-id="83b7f-117">Sets the cursor to a pointer when the user is able to cancel a print job, and to the wait cursor when the print job is at a point where it cannot be cancelled.</span></span>

-   <span data-ttu-id="83b7f-118">**impression du \_ début d’impression de \_ \_ l’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="83b7f-118">**USER\_PRINT\_START\_PRINTING**</span></span>

    <span data-ttu-id="83b7f-119">Définit les paramètres de barre de progression pour le travail d’impression et crée le thread d’impression pour démarrer le traitement du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="83b7f-119">Sets the progress bar parameters for the print job, and creates the printing thread to start processing the print job.</span></span>

    <span data-ttu-id="83b7f-120">Il s’agit d’un message de fenêtre spécifique à l’application.</span><span class="sxs-lookup"><span data-stu-id="83b7f-120">This is an application-specific window message.</span></span>

-   <span data-ttu-id="83b7f-121">**\_commande WM-IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="83b7f-121">**WM\_COMMAND - IDCANCEL**</span></span>

    <span data-ttu-id="83b7f-122">Définit l’événement CANCEL pour indiquer au thread de traitement de l’impression d’annuler le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="83b7f-122">Sets the cancel event to tell the print processing thread to cancel the print job.</span></span>

-   <span data-ttu-id="83b7f-123">**\_ \_ \_ mise à jour de l’état d’impression de l’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="83b7f-123">**USER\_PRINT\_STATUS\_UPDATE**</span></span>

    <span data-ttu-id="83b7f-124">Met à jour la barre de progression et le texte d’État pour afficher l’état actuel du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="83b7f-124">Updates the progress bar and status text to show the current state of the print job.</span></span>

    <span data-ttu-id="83b7f-125">Il s’agit d’un message de fenêtre spécifique à l’application.</span><span class="sxs-lookup"><span data-stu-id="83b7f-125">This is an application-specific window message.</span></span>

-   <span data-ttu-id="83b7f-126">**fermeture de l’impression de l’utilisateur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="83b7f-126">**USER\_PRINT\_CLOSING**</span></span>

    <span data-ttu-id="83b7f-127">Définit le texte d’état de fermeture dans la boîte de dialogue de progression pour indiquer que le travail d’impression est en cours de fermeture.</span><span class="sxs-lookup"><span data-stu-id="83b7f-127">Sets the closing status text in the progress dialog box to indicate that the print job is closing.</span></span>

    <span data-ttu-id="83b7f-128">Il s’agit d’un message de fenêtre spécifique à l’application.</span><span class="sxs-lookup"><span data-stu-id="83b7f-128">This is an application-specific window message.</span></span>

-   <span data-ttu-id="83b7f-129">**impression de l’utilisateur \_ \_ terminée**</span><span class="sxs-lookup"><span data-stu-id="83b7f-129">**USER\_PRINT\_COMPLETE**</span></span>

    <span data-ttu-id="83b7f-130">Affiche le message « travail d’impression terminé » pour l’utilisateur et libère les descripteurs et les événements qui ont été utilisés dans ce travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="83b7f-130">Displays the "Print job complete" message to the user, and releases handles and events that were used in this print job.</span></span>

    <span data-ttu-id="83b7f-131">Il s’agit d’un message de fenêtre spécifique à l’application.</span><span class="sxs-lookup"><span data-stu-id="83b7f-131">This is an application-specific window message.</span></span>

 

 



