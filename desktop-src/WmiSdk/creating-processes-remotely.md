---
description: Vous pouvez utiliser Win32 \_ Process. Create pour exécuter un script ou une application sur un ordinateur distant. Toutefois, pour des raisons de sécurité, le processus ne peut pas être interactif. Lorsque \_ le processus Win32. Create est appelé sur l’ordinateur local, le processus peut être interactif.
ms.assetid: 11fea8b1-7d05-4f44-9103-ea804a1d4b38
ms.tgt_platform: multiple
title: Création de processus à distance à l’aide de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e7b97f8f4fdddd608f6ee8c3368bde6ad6e854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758746"
---
# <a name="creating-processes-remotely-using-wmi"></a><span data-ttu-id="56e7c-105">Création de processus à distance à l’aide de WMI</span><span class="sxs-lookup"><span data-stu-id="56e7c-105">Creating Processes Remotely using WMI</span></span>

<span data-ttu-id="56e7c-106">Vous pouvez utiliser [**Win32 \_ Process. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) pour exécuter un script ou une application sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="56e7c-106">You can use [**Win32\_Process.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) to execute a script or application on a remote computer.</span></span> <span data-ttu-id="56e7c-107">Toutefois, pour des raisons de sécurité, le processus ne peut pas être interactif.</span><span class="sxs-lookup"><span data-stu-id="56e7c-107">However, for security reasons, the process cannot be interactive.</span></span> <span data-ttu-id="56e7c-108">Lorsque **le \_ processus Win32. Create** est appelé sur l’ordinateur local, le processus peut être interactif.</span><span class="sxs-lookup"><span data-stu-id="56e7c-108">When **Win32\_Process.Create** is called on the local computer, the process can be interactive.</span></span>

> [!WARNING]
> <span data-ttu-id="56e7c-109">Cette rubrique décrit la procédure générale à respecter pour créer un processus distant avec WMI.</span><span class="sxs-lookup"><span data-stu-id="56e7c-109">This topic describes the general procedure for creating a remote process with WMI.</span></span> <span data-ttu-id="56e7c-110">Si vous cherchez simplement à exécuter un script sur un système distant, consultez [connexion à WMI à distance à partir de Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md)ou [connexion à WMI sur un ordinateur distant à l’aide de Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="56e7c-110">If you are simply looking to run a script on a remote system, see [Connecting to WMI Remotely Starting with Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md), or [Connecting to WMI on a Remote Computer by Using Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span></span> <span data-ttu-id="56e7c-111">Pour plus d’informations générales sur la communication à distance avec PowerShell, consultez [exécution de commandes distantes](https://technet.microsoft.com/library/dd819505.aspx).</span><span class="sxs-lookup"><span data-stu-id="56e7c-111">For more general information on remoting with PowerShell, see [Running Remote Commands](https://technet.microsoft.com/library/dd819505.aspx).</span></span>

 

<span data-ttu-id="56e7c-112">Le processus distant n’a pas d’interface utilisateur, mais il est listé dans le **Gestionnaire des tâches**.</span><span class="sxs-lookup"><span data-stu-id="56e7c-112">The remote process has no user interface but it is listed in the **Task Manager**.</span></span> <span data-ttu-id="56e7c-113">Un processus créé localement peut s’exécuter sous n’importe quel compte si le compte dispose de l’autorisation **Execute Method** pour l' \\ espace de noms CIMV2 racine.</span><span class="sxs-lookup"><span data-stu-id="56e7c-113">A process created locally can run under any account if the account has the **Execute Method** permission for the root\\cimv2 namespace.</span></span> <span data-ttu-id="56e7c-114">Un processus créé à distance peut s’exécuter sous n’importe quel compte si le compte a la **méthode Execute** et les autorisations **Remote Enable** pour la racine \\ cimv2.</span><span class="sxs-lookup"><span data-stu-id="56e7c-114">A process created remotely can run under any account if the account has the **Execute Method** and **Remote Enable** permissions for root\\cimv2.</span></span> <span data-ttu-id="56e7c-115">La **méthode Execute** et les autorisations **Remote Enable** sont définies dans le contrôle WMI dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="56e7c-115">The **Execute Method** and **Remote Enable** permissions are set in WMI Control in the Control Panel.</span></span> <span data-ttu-id="56e7c-116">Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms avec le contrôle WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="56e7c-116">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>

<span data-ttu-id="56e7c-117">Vous pouvez utiliser [**Win32 \_ ScheduledJob. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) pour créer un processus interactif à distance.</span><span class="sxs-lookup"><span data-stu-id="56e7c-117">You can use [**Win32\_ScheduledJob.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) to create an interactive process remotely.</span></span> <span data-ttu-id="56e7c-118">Mais les processus démarrés par **Win32 \_ ScheduledJob. Create** s’exécutent sous le compte LocalSystem qui peut confère un trop grand privilège.</span><span class="sxs-lookup"><span data-stu-id="56e7c-118">But processes started by **Win32\_ScheduledJob.Create** run under the LocalSystem account that can confer too much privilege.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56e7c-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="56e7c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56e7c-120">Sécurisation d’une connexion WMI à distance</span><span class="sxs-lookup"><span data-stu-id="56e7c-120">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> <dt>

[<span data-ttu-id="56e7c-121">Connexion à un troisième ordinateur-délégation</span><span class="sxs-lookup"><span data-stu-id="56e7c-121">Connecting to a 3rd Computer-Delegation</span></span>](connecting-to-a-3rd-computer-delegation.md)
</dt> </dl>

 

 
