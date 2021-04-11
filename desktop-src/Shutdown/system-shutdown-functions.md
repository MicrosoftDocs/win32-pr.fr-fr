---
description: Les fonctions suivantes sont utilisées avec l’arrêt du système.
ms.assetid: 6a08a769-1acf-49eb-ba95-beaf56a374bf
title: Fonctions d’arrêt du système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd457c86129b3e5f80d6359018c1474f837b9e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952104"
---
# <a name="system-shutdown-functions"></a><span data-ttu-id="dd820-103">Fonctions d’arrêt du système</span><span class="sxs-lookup"><span data-stu-id="dd820-103">System Shutdown Functions</span></span>

<span data-ttu-id="dd820-104">Les fonctions suivantes sont utilisées avec l’arrêt du système.</span><span class="sxs-lookup"><span data-stu-id="dd820-104">The following functions are used with system shutdown.</span></span>



| <span data-ttu-id="dd820-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="dd820-105">Function</span></span>                                                         | <span data-ttu-id="dd820-106">Description</span><span class="sxs-lookup"><span data-stu-id="dd820-106">Description</span></span>                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd820-107">**AbortSystemShutdown**</span><span class="sxs-lookup"><span data-stu-id="dd820-107">**AbortSystemShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna)               | <span data-ttu-id="dd820-108">Arrête un arrêt du système qui a été initié.</span><span class="sxs-lookup"><span data-stu-id="dd820-108">Stops a system shutdown that has been initiated.</span></span>                                                                                    |
| [<span data-ttu-id="dd820-109">**ExitWindows**</span><span class="sxs-lookup"><span data-stu-id="dd820-109">**ExitWindows**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindows)                               | <span data-ttu-id="dd820-110">Déconnecte l’utilisateur interactif.</span><span class="sxs-lookup"><span data-stu-id="dd820-110">Logs off the interactive user.</span></span>                                                                                                      |
| [<span data-ttu-id="dd820-111">**ExitWindowsEx**</span><span class="sxs-lookup"><span data-stu-id="dd820-111">**ExitWindowsEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)                           | <span data-ttu-id="dd820-112">Déconnecte l’utilisateur interactif, arrête le système ou arrête et redémarre le système.</span><span class="sxs-lookup"><span data-stu-id="dd820-112">Logs off the interactive user, shuts down the system, or shuts down and restarts the system.</span></span>                                        |
| [<span data-ttu-id="dd820-113">**InitiateShutdown**</span><span class="sxs-lookup"><span data-stu-id="dd820-113">**InitiateShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)                     | <span data-ttu-id="dd820-114">Lance un arrêt et un redémarrage de l’ordinateur spécifié, puis redémarre toutes les applications qui ont été inscrites pour le redémarrage.</span><span class="sxs-lookup"><span data-stu-id="dd820-114">Initiates a shutdown and restart of the specified computer, and restarts any applications that have been registered for restart.</span></span>    |
| [<span data-ttu-id="dd820-115">**InitiateSystemShutdown**</span><span class="sxs-lookup"><span data-stu-id="dd820-115">**InitiateSystemShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)         | <span data-ttu-id="dd820-116">Lance un arrêt et un redémarrage facultatif de l’ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="dd820-116">Initiates a shutdown and optional restart of the specified computer.</span></span>                                                                |
| [<span data-ttu-id="dd820-117">**InitiateSystemShutdownEx**</span><span class="sxs-lookup"><span data-stu-id="dd820-117">**InitiateSystemShutdownEx**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)     | <span data-ttu-id="dd820-118">Lance un arrêt et un redémarrage facultatif de l’ordinateur spécifié et enregistre éventuellement la raison de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="dd820-118">Initiates a shutdown and optional restart of the specified computer, and optionally records the reason for the shutdown.</span></span>            |
| [<span data-ttu-id="dd820-119">**LockWorkStation**</span><span class="sxs-lookup"><span data-stu-id="dd820-119">**LockWorkStation**</span></span>](/windows/desktop/api/Winuser/nf-winuser-lockworkstation)                       | <span data-ttu-id="dd820-120">Verrouille l’affichage de la station de travail.</span><span class="sxs-lookup"><span data-stu-id="dd820-120">Locks the workstation's display.</span></span>                                                                                                    |
| [<span data-ttu-id="dd820-121">**ShutdownBlockReasonCreate**</span><span class="sxs-lookup"><span data-stu-id="dd820-121">**ShutdownBlockReasonCreate**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)   | <span data-ttu-id="dd820-122">Indique que le système ne peut pas être arrêté et définit une chaîne de motif à afficher à l’utilisateur si l’arrêt du système est initié.</span><span class="sxs-lookup"><span data-stu-id="dd820-122">Indicates that the system cannot be shut down and sets a reason string to be displayed to the user if system shutdown is initiated.</span></span> |
| [<span data-ttu-id="dd820-123">**ShutdownBlockReasonDestroy**</span><span class="sxs-lookup"><span data-stu-id="dd820-123">**ShutdownBlockReasonDestroy**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasondestroy) | <span data-ttu-id="dd820-124">Indique que le système peut être arrêté et libère la chaîne de raison.</span><span class="sxs-lookup"><span data-stu-id="dd820-124">Indicates that the system can be shut down and frees the reason string.</span></span>                                                             |
| [<span data-ttu-id="dd820-125">**ShutdownBlockReasonQuery**</span><span class="sxs-lookup"><span data-stu-id="dd820-125">**ShutdownBlockReasonQuery**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasonquery)     | <span data-ttu-id="dd820-126">Récupère la chaîne de raison définie par la fonction [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) .</span><span class="sxs-lookup"><span data-stu-id="dd820-126">Retrieves the reason string set by the [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) function.</span></span>                     |



 

 

 



