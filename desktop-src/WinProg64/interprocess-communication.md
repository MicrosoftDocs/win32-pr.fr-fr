---
title: Communication entre processus
description: Les techniques suivantes peuvent être utilisées pour la communication entre les applications 32 bits et 64 bits.
ms.assetid: 9a60ccfe-4ccf-44d7-9522-42609d95217b
keywords:
- communication entre processus, programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2398174f011127973dfd0b1773e6eb040cdde898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382342"
---
# <a name="interprocess-communication-between-32-bit-and-64-bit-applications"></a><span data-ttu-id="81af1-104">Communication entre processus entre les applications 32 bits et 64 bits</span><span class="sxs-lookup"><span data-stu-id="81af1-104">Interprocess Communication Between 32-bit and 64-bit Applications</span></span>

<span data-ttu-id="81af1-105">Les techniques suivantes peuvent être utilisées pour la communication entre les applications 32 bits et 64 bits :</span><span class="sxs-lookup"><span data-stu-id="81af1-105">The following techniques can be used for communication between 32-bit and 64-bit applications:</span></span>

-   <span data-ttu-id="81af1-106">les versions 64 bits de Windows utilisent des handles 32 bits pour l’interopérabilité.</span><span class="sxs-lookup"><span data-stu-id="81af1-106">64-bit versions of Windows use 32-bit handles for interoperability.</span></span> <span data-ttu-id="81af1-107">Lors du partage d’un handle entre des applications 32 bits et 64 bits, seuls les 32 bits inférieurs sont significatifs. il est donc plus sûr de tronquer le descripteur (lors de son passage d’un 64-bit à un bit 32) ou d’étendre le descripteur (lors de son passage de 32-bit à 64-bit).</span><span class="sxs-lookup"><span data-stu-id="81af1-107">When sharing a handle between 32-bit and 64-bit applications, only the lower 32 bits are significant, so it is safe to truncate the handle (when passing it from 64-bit to 32-bit) or sign-extend the handle (when passing it from 32-bit to 64-bit).</span></span> <span data-ttu-id="81af1-108">Les handles qui peuvent être partagés incluent des handles d’objets utilisateur tels que Windows (**HWND**), des handles vers des objets GDI tels que des stylets et des pinceaux (**HBRUSH** et **HPEN**), ainsi que des handles vers des objets nommés tels que les mutex, les sémaphores et les descripteurs de fichiers.</span><span class="sxs-lookup"><span data-stu-id="81af1-108">Handles that can be shared include handles to user objects such as windows (**HWND**), handles to GDI objects such as pens and brushes (**HBRUSH** and **HPEN**), and handles to named objects such as mutexes, semaphores, and file handles.</span></span>
-   <span data-ttu-id="81af1-109">Les appels de procédure distante (RPC) peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="81af1-109">Remote procedure calls (RPC) can be used.</span></span>
-   <span data-ttu-id="81af1-110">COM LocalServers peut être utilisé si les dll proxy/stub 32 bits et 64 bits sont inscrites pour toutes les interfaces utilisées.</span><span class="sxs-lookup"><span data-stu-id="81af1-110">COM LocalServers can be used if both 32-bit and 64-bit proxy/stub DLLs are registered for all interfaces used.</span></span>
-   <span data-ttu-id="81af1-111">La mémoire partagée peut être utilisée si les types dépendants du pointeur sont convertis correctement (ou évités).</span><span class="sxs-lookup"><span data-stu-id="81af1-111">Shared memory can be used if pointer-dependent types are converted properly (or avoided).</span></span>
-   <span data-ttu-id="81af1-112">Les fonctions [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) et [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) peuvent lancer des processus 32 bits et 64 bits à partir de processus 32 bits ou 64 bits, avec certaines limitations.</span><span class="sxs-lookup"><span data-stu-id="81af1-112">The [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) and [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) functions can launch 32-bit and 64-bit processes from either 32-bit or 64-bit processes with certain limitations.</span></span>

<span data-ttu-id="81af1-113">Un fichier exécutable 64 bits situé sous% windir% \\ system32 ne peut pas être lancé à partir d’un processus 32 bits, car le redirecteur du système de fichiers redirige le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="81af1-113">A 64-bit executable file located under %windir%\\System32 cannot be launched from a 32-bit process, because the file system redirector redirects the path.</span></span> <span data-ttu-id="81af1-114">Ne désactivez pas la redirection pour effectuer cette opération. Utilisez à la place% windir% \\ SysNative.</span><span class="sxs-lookup"><span data-stu-id="81af1-114">Do not disable redirection to accomplish this; use %windir%\\Sysnative instead.</span></span> <span data-ttu-id="81af1-115">Pour plus d’informations, consultez [redirecteur de système de fichiers](file-system-redirector.md).</span><span class="sxs-lookup"><span data-stu-id="81af1-115">For more information, see [File System Redirector](file-system-redirector.md).</span></span>

 

 