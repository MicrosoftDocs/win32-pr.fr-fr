---
description: Cette rubrique traite des minuteries. Un minuteur est une routine interne qui mesure à plusieurs reprises un intervalle spécifié, en millisecondes.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\timers.htm
title: Minuteurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa44be05acc09eafed550a200ed6bc61f79daa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529439"
---
# <a name="timers"></a><span data-ttu-id="2f07d-104">Minuteurs</span><span class="sxs-lookup"><span data-stu-id="2f07d-104">Timers</span></span>

<span data-ttu-id="2f07d-105">Un minuteur est une routine interne qui mesure à plusieurs reprises un intervalle spécifié, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="2f07d-105">A timer is an internal routine that repeatedly measures a specified interval, in milliseconds.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="2f07d-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="2f07d-106">In This Section</span></span>



| <span data-ttu-id="2f07d-107">Nom</span><span class="sxs-lookup"><span data-stu-id="2f07d-107">Name</span></span>                                   | <span data-ttu-id="2f07d-108">Description</span><span class="sxs-lookup"><span data-stu-id="2f07d-108">Description</span></span>                                                                                                               |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f07d-109">À propos des minuteries</span><span class="sxs-lookup"><span data-stu-id="2f07d-109">About Timers</span></span>](about-timers.md)       | <span data-ttu-id="2f07d-110">Décrit comment créer, identifier, définir et supprimer des minuteries.</span><span class="sxs-lookup"><span data-stu-id="2f07d-110">Describes how to create, identify, set, and delete timers.</span></span><br/>                                                     |
| [<span data-ttu-id="2f07d-111">Utilisation de minuteurs</span><span class="sxs-lookup"><span data-stu-id="2f07d-111">Using Timers</span></span>](using-timers.md)       | <span data-ttu-id="2f07d-112">Explique comment créer et détruire des minuteries, et comment utiliser un minuteur pour intercepter l’entrée de la souris à des intervalles spécifiés.</span><span class="sxs-lookup"><span data-stu-id="2f07d-112">Discusses how to create and destroy timers, and how to use a timer to trap mouse input at specified intervals.</span></span><br/> |
| [<span data-ttu-id="2f07d-113">Référence du minuteur</span><span class="sxs-lookup"><span data-stu-id="2f07d-113">Timer Reference</span></span>](timer-reference.md) | <span data-ttu-id="2f07d-114">Contient la référence de l’API.</span><span class="sxs-lookup"><span data-stu-id="2f07d-114">Contains the API reference.</span></span><br/>                                                                                    |



 

### <a name="timer-functions"></a><span data-ttu-id="2f07d-115">Fonctions de minuterie</span><span class="sxs-lookup"><span data-stu-id="2f07d-115">Timer Functions</span></span>



| <span data-ttu-id="2f07d-116">Nom</span><span class="sxs-lookup"><span data-stu-id="2f07d-116">Name</span></span>                           | <span data-ttu-id="2f07d-117">Description</span><span class="sxs-lookup"><span data-stu-id="2f07d-117">Description</span></span>                                                                                                                                                                                                                                                              |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f07d-118">**KillTimer**</span><span class="sxs-lookup"><span data-stu-id="2f07d-118">**KillTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-killtimer) | <span data-ttu-id="2f07d-119">Détruit la minuterie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2f07d-119">Destroys the specified timer.</span></span> <br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="2f07d-120">**SetTimer**</span><span class="sxs-lookup"><span data-stu-id="2f07d-120">**SetTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-settimer)   | <span data-ttu-id="2f07d-121">Crée un minuteur avec la valeur de délai d’attente spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2f07d-121">Creates a timer with the specified time-out value.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="2f07d-122">*TimerProc*</span><span class="sxs-lookup"><span data-stu-id="2f07d-122">*TimerProc*</span></span>](/windows/win32/api/winuser/nc-winuser-timerproc)   | <span data-ttu-id="2f07d-123">Fonction de rappel définie par l’application qui traite les messages [**\_ du minuteur WM**](wm-timer.md) .</span><span class="sxs-lookup"><span data-stu-id="2f07d-123">An application-defined callback function that processes [**WM\_TIMER**](wm-timer.md) messages.</span></span> <span data-ttu-id="2f07d-124">Le type **TIMERPROC** définit un pointeur vers cette fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="2f07d-124">The **TIMERPROC** type defines a pointer to this callback function.</span></span> <span data-ttu-id="2f07d-125">[*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) est un espace réservé pour le nom de la fonction définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="2f07d-125">[*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) is a placeholder for the application-defined function name.</span></span> <br/> |



 

### <a name="timer-notifications"></a><span data-ttu-id="2f07d-126">Notifications du minuteur</span><span class="sxs-lookup"><span data-stu-id="2f07d-126">Timer Notifications</span></span>



| <span data-ttu-id="2f07d-127">Nom</span><span class="sxs-lookup"><span data-stu-id="2f07d-127">Name</span></span>                          | <span data-ttu-id="2f07d-128">Description</span><span class="sxs-lookup"><span data-stu-id="2f07d-128">Description</span></span>                                                                                                                                                                                     |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f07d-129">**\_minuteur WM**</span><span class="sxs-lookup"><span data-stu-id="2f07d-129">**WM\_TIMER**</span></span>](wm-timer.md) | <span data-ttu-id="2f07d-130">Publié dans la file d’attente de messages du thread d’installation lors de l’expiration d’un minuteur.</span><span class="sxs-lookup"><span data-stu-id="2f07d-130">Posted to the installing thread's message queue when a timer expires.</span></span> <span data-ttu-id="2f07d-131">Le message est publié par la fonction [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .</span><span class="sxs-lookup"><span data-stu-id="2f07d-131">The message is posted by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span> <br/> |



 

 

 
