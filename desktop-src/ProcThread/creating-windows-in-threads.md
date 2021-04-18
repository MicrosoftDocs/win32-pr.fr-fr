---
description: Tout thread peut créer une fenêtre.
ms.assetid: 27f04f9f-52d9-46d6-8e06-9b032682b7c7
title: Créer des fenêtres dans les threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebcde45ca37696b6dbc90e639f630a689498b04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533889"
---
# <a name="creating-windows-in-threads"></a><span data-ttu-id="7b8b2-103">Créer des fenêtres dans les threads</span><span class="sxs-lookup"><span data-stu-id="7b8b2-103">Creating Windows in Threads</span></span>

<span data-ttu-id="7b8b2-104">Tout thread peut créer une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7b8b2-104">Any thread can create a window.</span></span> <span data-ttu-id="7b8b2-105">Le thread qui crée la fenêtre est propriétaire de la fenêtre et de sa file d’attente de messages associée.</span><span class="sxs-lookup"><span data-stu-id="7b8b2-105">The thread that creates the window owns the window and its associated message queue.</span></span> <span data-ttu-id="7b8b2-106">Par conséquent, le thread doit fournir une boucle de messages pour traiter les messages dans sa file d’attente de messages.</span><span class="sxs-lookup"><span data-stu-id="7b8b2-106">Therefore, the thread must provide a message loop to process the messages in its message queue.</span></span> <span data-ttu-id="7b8b2-107">En outre, vous devez utiliser [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) ou [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) dans ce thread, plutôt que les autres [fonctions Wait](/windows/desktop/Sync/wait-functions), afin qu’il puisse traiter les messages.</span><span class="sxs-lookup"><span data-stu-id="7b8b2-107">In addition, you must use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) or [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) in that thread, rather than the other [wait functions](/windows/desktop/Sync/wait-functions), so that it can process messages.</span></span> <span data-ttu-id="7b8b2-108">Dans le cas contraire, le système peut devenir bloqué lorsque le thread reçoit un message alors qu’il est en attente.</span><span class="sxs-lookup"><span data-stu-id="7b8b2-108">Otherwise, the system can become deadlocked when the thread is sent a message while it is waiting.</span></span>

<span data-ttu-id="7b8b2-109">La fonction [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) peut être utilisée pour permettre à un ensemble de threads de partager le même état d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7b8b2-109">The [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) function can be used to allow a set of threads to share the same input state.</span></span> <span data-ttu-id="7b8b2-110">En partageant l’état d’entrée, les threads partagent leur concept de fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="7b8b2-110">By sharing input state, the threads share their concept of the active window.</span></span> <span data-ttu-id="7b8b2-111">En procédant ainsi, un thread peut toujours activer la fenêtre d’un autre thread.</span><span class="sxs-lookup"><span data-stu-id="7b8b2-111">By doing this, one thread can always activate another thread's window.</span></span> <span data-ttu-id="7b8b2-112">Cette fonction est également utile pour partager l’état du focus, l’état de capture de la souris, l’état du clavier et l’état de l’ordre des fenêtres dans les fenêtres créées par différents threads dont l’état d’entrée est partagé.</span><span class="sxs-lookup"><span data-stu-id="7b8b2-112">This function is also useful for sharing focus state, mouse capture state, keyboard state, and window Z-order state among windows created by different threads whose input state is shared.</span></span>

<span data-ttu-id="7b8b2-113">Pour plus d’informations sur la création de fenêtres, consultez [classes Windows](../winmsg/window-classes.md).</span><span class="sxs-lookup"><span data-stu-id="7b8b2-113">For information about creating windows, see [Windows Classes](../winmsg/window-classes.md).</span></span>

 

 
