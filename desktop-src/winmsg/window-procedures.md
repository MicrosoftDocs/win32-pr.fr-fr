---
description: Cette section traite des procédures relatives aux fenêtres. Chaque fenêtre est associée à une procédure de fenêtre qui traite tous les messages envoyés ou publiés dans toutes les fenêtres de la classe.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowprocedures.htm
title: Procédures de fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ae68ba9b64557a6dc70d5c83788b8337648a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523415"
---
# <a name="window-procedures"></a><span data-ttu-id="5fecd-104">Procédures de fenêtre</span><span class="sxs-lookup"><span data-stu-id="5fecd-104">Window Procedures</span></span>

<span data-ttu-id="5fecd-105">Chaque fenêtre a une procédure de fenêtre associée, c’est-à-dire une fonction qui traite tous les messages envoyés ou publiés dans toutes les fenêtres de la classe.</span><span class="sxs-lookup"><span data-stu-id="5fecd-105">Every window has an associated window procedure — a function that processes all messages sent or posted to all windows of the class.</span></span> <span data-ttu-id="5fecd-106">Tous les aspects de l’apparence et du comportement d’une fenêtre dépendent de la réponse de la procédure de fenêtre à ces messages.</span><span class="sxs-lookup"><span data-stu-id="5fecd-106">All aspects of a window's appearance and behavior depend on the window procedure's response to these messages.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="5fecd-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="5fecd-107">In This Section</span></span>



| <span data-ttu-id="5fecd-108">Nom</span><span class="sxs-lookup"><span data-stu-id="5fecd-108">Name</span></span>                                                         | <span data-ttu-id="5fecd-109">Description</span><span class="sxs-lookup"><span data-stu-id="5fecd-109">Description</span></span>                                                                                                                                                                                                    |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5fecd-110">À propos des procédures de fenêtre</span><span class="sxs-lookup"><span data-stu-id="5fecd-110">About Window Procedures</span></span>](about-window-procedures.md)       | <span data-ttu-id="5fecd-111">Traite des procédures de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5fecd-111">Discusses window procedures.</span></span> <span data-ttu-id="5fecd-112">Chaque fenêtre est un membre d’une classe de fenêtre particulière.</span><span class="sxs-lookup"><span data-stu-id="5fecd-112">Each window is a member of a particular window class.</span></span> <span data-ttu-id="5fecd-113">La classe de fenêtre détermine la procédure de fenêtre par défaut utilisée par une fenêtre individuelle pour traiter ses messages.</span><span class="sxs-lookup"><span data-stu-id="5fecd-113">The window class determines the default window procedure that an individual window uses to process its messages.</span></span><br/> |
| [<span data-ttu-id="5fecd-114">Utilisation des procédures de fenêtre</span><span class="sxs-lookup"><span data-stu-id="5fecd-114">Using Window Procedures</span></span>](using-window-procedures.md)       | <span data-ttu-id="5fecd-115">Explique comment effectuer les tâches suivantes associées aux procédures de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5fecd-115">Covers how to perform the following tasks associated with window procedures.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="5fecd-116">Référence de procédure de fenêtre</span><span class="sxs-lookup"><span data-stu-id="5fecd-116">Window Procedure Reference</span></span>](window-procedure-reference.md) | <span data-ttu-id="5fecd-117">Contient la référence de l’API.</span><span class="sxs-lookup"><span data-stu-id="5fecd-117">Contains the API reference.</span></span><br/>                                                                                                                                                                         |



 

### <a name="functions"></a><span data-ttu-id="5fecd-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="5fecd-118">Functions</span></span>



| <span data-ttu-id="5fecd-119">Nom</span><span class="sxs-lookup"><span data-stu-id="5fecd-119">Name</span></span>                                     | <span data-ttu-id="5fecd-120">Description</span><span class="sxs-lookup"><span data-stu-id="5fecd-120">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5fecd-121">**CallWindowProc**</span><span class="sxs-lookup"><span data-stu-id="5fecd-121">**CallWindowProc**</span></span>](/windows/win32/api/winuser/nf-winuser-callwindowproca) | <span data-ttu-id="5fecd-122">Transmet les informations de message à la procédure de fenêtre spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5fecd-122">Passes message information to the specified window procedure.</span></span> <br/>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="5fecd-123">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="5fecd-123">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)   | <span data-ttu-id="5fecd-124">Appelle la procédure de fenêtre par défaut pour fournir le traitement par défaut pour tous les messages de fenêtre qu’une application ne traite pas.</span><span class="sxs-lookup"><span data-stu-id="5fecd-124">Calls the default window procedure to provide default processing for any window messages that an application does not process.</span></span> <span data-ttu-id="5fecd-125">Cette fonction garantit que chaque message est traité.</span><span class="sxs-lookup"><span data-stu-id="5fecd-125">This function ensures that every message is processed.</span></span> <span data-ttu-id="5fecd-126">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) est appelé avec les mêmes paramètres que ceux reçus par la procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5fecd-126">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) is called with the same parameters received by the window procedure.</span></span> <br/> |
| <span data-ttu-id="5fecd-127">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5fecd-127">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span></span>           | <span data-ttu-id="5fecd-128">Fonction définie par l’application qui traite les messages envoyés à une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5fecd-128">An application-defined function that processes messages sent to a window.</span></span> <span data-ttu-id="5fecd-129">Le type **WNDPROC** définit un pointeur vers cette fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="5fecd-129">The **WNDPROC** type defines a pointer to this callback function.</span></span> <span data-ttu-id="5fecd-130">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) est un espace réservé pour le nom de la fonction définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="5fecd-130">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) is a placeholder for the application-defined function name.</span></span> <br/>                                                            |



 

 

 
