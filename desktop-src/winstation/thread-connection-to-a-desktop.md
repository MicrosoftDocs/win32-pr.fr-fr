---
title: Connexion de thread à un bureau
description: Une fois qu’un processus s’est connecté à une station Windows, le système affecte un bureau au thread qui effectue la connexion.
ms.assetid: 45016619-ed11-4b0c-84e3-f8662553c64d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a503390468ea5ed1771ece7a942a2d615ac6f0a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199265"
---
# <a name="thread-connection-to-a-desktop"></a><span data-ttu-id="6401a-103">Connexion de thread à un bureau</span><span class="sxs-lookup"><span data-stu-id="6401a-103">Thread Connection to a Desktop</span></span>

<span data-ttu-id="6401a-104">Une fois qu’un processus s’est connecté à une station Windows, le système affecte un bureau au thread qui effectue la connexion.</span><span class="sxs-lookup"><span data-stu-id="6401a-104">After a process connects to a window station, the system assigns a desktop to the thread making the connection.</span></span> <span data-ttu-id="6401a-105">Le système détermine le Bureau à assigner au thread conformément aux règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="6401a-105">The system determines the desktop to assign to the thread according to the following rules:</span></span>

1.  <span data-ttu-id="6401a-106">Si le thread a appelé la fonction [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) , il se connecte au bureau spécifié.</span><span class="sxs-lookup"><span data-stu-id="6401a-106">If the thread has called the [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) function, it connects to the specified desktop.</span></span>
2.  <span data-ttu-id="6401a-107">Si le thread n’a pas appelé [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop), il se connecte au bureau hérité du processus parent.</span><span class="sxs-lookup"><span data-stu-id="6401a-107">If the thread did not call [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop), it connects to the desktop inherited from the parent process.</span></span>
3.  <span data-ttu-id="6401a-108">Si le thread n’a pas appelé [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) et n’a pas hérité de bureau, le système tente d’ouvrir pour un maximum d' \_ accès autorisé et se connecte à un bureau comme suit :</span><span class="sxs-lookup"><span data-stu-id="6401a-108">If the thread did not call [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) and did not inherit a desktop, the system attempts to open for MAXIMUM\_ALLOWED access and connect to a desktop as follows:</span></span>
    -   <span data-ttu-id="6401a-109">Si un nom de bureau a été spécifié dans le membre **lpDesktop** de la structure [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) qui a été utilisée lors de la création du processus, le thread se connecte au bureau spécifié.</span><span class="sxs-lookup"><span data-stu-id="6401a-109">If a desktop name was specified in the **lpDesktop** member of the [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure that was used when the process was created, the thread connects to the specified desktop.</span></span>
    -   <span data-ttu-id="6401a-110">Dans le cas contraire, le thread se connecte au bureau par défaut de la station Windows à laquelle le processus est connecté.</span><span class="sxs-lookup"><span data-stu-id="6401a-110">Otherwise, the thread connects to the default desktop of the window station to which the process connected.</span></span>

<span data-ttu-id="6401a-111">Le bureau affecté au cours de ce processus de connexion ne peut pas être fermé en appelant la fonction [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop) .</span><span class="sxs-lookup"><span data-stu-id="6401a-111">The desktop assigned during this connection process cannot be closed by calling the [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop) function.</span></span>

<span data-ttu-id="6401a-112">Lorsqu’un processus se connecte à un ordinateur de bureau, le système recherche les descripteurs hérités dans la table de handles du processus.</span><span class="sxs-lookup"><span data-stu-id="6401a-112">When a process is connecting to a desktop, the system searches the process's handle table for inherited handles.</span></span> <span data-ttu-id="6401a-113">Le système utilise le premier handle de bureau qu’il trouve.</span><span class="sxs-lookup"><span data-stu-id="6401a-113">The system uses the first desktop handle it finds.</span></span> <span data-ttu-id="6401a-114">Si vous souhaitez qu’un processus enfant se connecte à un bureau hérité particulier, vous devez vous assurer que le seul handle souhaité est marqué comme étant pouvant être hérité.</span><span class="sxs-lookup"><span data-stu-id="6401a-114">If you want a child process to connect to a particular inherited desktop, you must ensure that the only the desired handle is marked inheritable.</span></span> <span data-ttu-id="6401a-115">Si un processus enfant hérite de plusieurs handles de bureau, les résultats de la connexion au bureau ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="6401a-115">If a child process inherits multiple desktop handles, the results of the desktop connection are undefined.</span></span>

<span data-ttu-id="6401a-116">Handles vers un bureau que le système ouvre lors de la connexion d’un processus à un bureau ne peuvent pas être hérités.</span><span class="sxs-lookup"><span data-stu-id="6401a-116">Handles to a desktop that the system opens while connecting a process to a desktop are not inheritable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6401a-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6401a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6401a-118">Traiter la connexion à une station Windows</span><span class="sxs-lookup"><span data-stu-id="6401a-118">Process Connection to a Window Station</span></span>](process-connection-to-a-window-station.md)
</dt> </dl>

 

 