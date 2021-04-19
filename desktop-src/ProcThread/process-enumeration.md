---
description: Tous les utilisateurs ont un accès en lecture à la liste des processus du système et il existe plusieurs fonctions différentes qui énumèrent les processus actifs. La fonction que vous devez utiliser dépend de facteurs tels que la prise en charge de plateforme souhaitée.
ms.assetid: 4c73fb10-7ee8-4d8a-9cdb-a2ae59aef5bd
title: Énumération des processus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911d11a50e898656b56fe89001811b939473c2e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527468"
---
# <a name="process-enumeration"></a><span data-ttu-id="d52a6-104">Énumération des processus</span><span class="sxs-lookup"><span data-stu-id="d52a6-104">Process Enumeration</span></span>

<span data-ttu-id="d52a6-105">Tous les utilisateurs ont un accès en lecture à la liste des processus du système et il existe plusieurs fonctions différentes qui énumèrent les processus actifs.</span><span class="sxs-lookup"><span data-stu-id="d52a6-105">All users have read access to the list of processes in the system and there are a number of different functions that enumerate the active processes.</span></span> <span data-ttu-id="d52a6-106">La fonction que vous devez utiliser dépend de facteurs tels que la prise en charge de plateforme souhaitée.</span><span class="sxs-lookup"><span data-stu-id="d52a6-106">The function you should use will depend on factors such as desired platform support.</span></span>

<span data-ttu-id="d52a6-107">Les fonctions suivantes sont utilisées pour énumérer les processus.</span><span class="sxs-lookup"><span data-stu-id="d52a6-107">The following functions are used to enumerate processes.</span></span>



| <span data-ttu-id="d52a6-108">Fonction</span><span class="sxs-lookup"><span data-stu-id="d52a6-108">Function</span></span>                                                    | <span data-ttu-id="d52a6-109">Description</span><span class="sxs-lookup"><span data-stu-id="d52a6-109">Description</span></span>                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="d52a6-110">**EnumProcesses**</span><span class="sxs-lookup"><span data-stu-id="d52a6-110">**EnumProcesses**</span></span>](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | <span data-ttu-id="d52a6-111">Récupère l’identificateur de processus pour chaque objet de processus dans le système.</span><span class="sxs-lookup"><span data-stu-id="d52a6-111">Retrieves the process identifier for each process object in the system.</span></span>            |
| [<span data-ttu-id="d52a6-112">**Process32First**</span><span class="sxs-lookup"><span data-stu-id="d52a6-112">**Process32First**</span></span>](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | <span data-ttu-id="d52a6-113">Récupère des informations sur le premier processus rencontré dans un instantané système.</span><span class="sxs-lookup"><span data-stu-id="d52a6-113">Retrieves information about the first process encountered in a system snapshot.</span></span>    |
| [<span data-ttu-id="d52a6-114">**Process32Next**</span><span class="sxs-lookup"><span data-stu-id="d52a6-114">**Process32Next**</span></span>](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | <span data-ttu-id="d52a6-115">Récupère des informations sur le processus suivant enregistré dans un instantané système.</span><span class="sxs-lookup"><span data-stu-id="d52a6-115">Retrieves information about the next process recorded in a system snapshot.</span></span>        |
| [<span data-ttu-id="d52a6-116">**WTSEnumerateProcesses**</span><span class="sxs-lookup"><span data-stu-id="d52a6-116">**WTSEnumerateProcesses**</span></span>](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | <span data-ttu-id="d52a6-117">Récupère des informations sur les processus actifs sur le serveur Terminal Server spécifié.</span><span class="sxs-lookup"><span data-stu-id="d52a6-117">Retrieves information about the active processes on the specified terminal server.</span></span> |



 

<span data-ttu-id="d52a6-118">Les fonctions toolhelp et [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) énumèrent tous les processus.</span><span class="sxs-lookup"><span data-stu-id="d52a6-118">The toolhelp functions and [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) enumerate all process.</span></span> <span data-ttu-id="d52a6-119">Pour répertorier les processus qui s’exécutent dans un compte d’utilisateur spécifique, utilisez [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) et filtrez sur le SID de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d52a6-119">To list the processes that are running in a specific user account, use [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) and filter on the user SID.</span></span> <span data-ttu-id="d52a6-120">Vous pouvez filtrer sur l’ID de session pour masquer les processus qui s’exécutent dans d’autres sessions Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="d52a6-120">You can filter on the session ID to hide processes running in other terminal server sessions.</span></span>

<span data-ttu-id="d52a6-121">Vous pouvez également filtrer les processus par compte d’utilisateur, quelle que soit la fonction d’énumération, en appelant [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)et [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) avec **TokenUser**.</span><span class="sxs-lookup"><span data-stu-id="d52a6-121">You can also filter processes by user account, regardless of the enumeration function, by calling [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken), and [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) with **TokenUser**.</span></span> <span data-ttu-id="d52a6-122">Toutefois, vous ne pouvez pas ouvrir un processus qui est protégé par un descripteur de sécurité, sauf si vous avez reçu l’autorisation d’accès.</span><span class="sxs-lookup"><span data-stu-id="d52a6-122">However, you cannot open a process that is protected by a security descriptor unless you have been granted access.</span></span>

 

 
