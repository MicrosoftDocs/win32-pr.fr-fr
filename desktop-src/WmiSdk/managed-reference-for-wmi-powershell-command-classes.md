---
description: Référence managée pour les classes de commandes WMI Windows PowerShell
ms.assetid: 30e77956-8428-4259-9218-b93f143fd987
ms.tgt_platform: multiple
title: Référence managée pour les classes de commandes WMI Windows PowerShell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb309a9ca421a3966f84ba1ae825bd0c81eee8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541928"
---
# <a name="managed-reference-for-wmi-windows-powershell-command-classes"></a><span data-ttu-id="162fb-103">Référence managée pour les classes de commandes WMI Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="162fb-103">Managed Reference for WMI Windows PowerShell Command Classes</span></span>

<span data-ttu-id="162fb-104">Windows PowerShell implémente la fonctionnalité de Windows Management Instrumentation (WMI) via un ensemble d’applets de commande.</span><span class="sxs-lookup"><span data-stu-id="162fb-104">Windows PowerShell implements Windows Management Instrumentation (WMI) functionality through a set of cmdlets.</span></span> <span data-ttu-id="162fb-105">Vous pouvez utiliser ces applets de commande pour effectuer les tâches de bout en bout nécessaires à la gestion des ordinateurs locaux et distants.</span><span class="sxs-lookup"><span data-stu-id="162fb-105">You can use these cmdlets to complete the end-to-end tasks that are necessary to manage local and remote computers.</span></span>

<span data-ttu-id="162fb-106">Pour plus d’informations, consultez [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="162fb-106">See [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) for more information.</span></span>

## <a name="wmi-powershell-classes"></a><span data-ttu-id="162fb-107">Classes PowerShell WMI</span><span class="sxs-lookup"><span data-stu-id="162fb-107">WMI PowerShell Classes</span></span>

<span data-ttu-id="162fb-108">**Espace de noms**: Microsoft. PowerShell. Commands</span><span class="sxs-lookup"><span data-stu-id="162fb-108">**Namespace**: Microsoft.PowerShell.Commands</span></span>

<span data-ttu-id="162fb-109">**Assembly**: Microsoft. PowerShell. Commands. Management</span><span class="sxs-lookup"><span data-stu-id="162fb-109">**Assembly**: Microsoft.PowerShell.Commands.Management</span></span>

<span data-ttu-id="162fb-110">**Dll**: Microsoft.PowerShell.Commands.Management.dll</span><span class="sxs-lookup"><span data-stu-id="162fb-110">**DLL**: Microsoft.PowerShell.Commands.Management.dll</span></span>

<span data-ttu-id="162fb-111">Ces classes de commandes WMI sont implémentées par Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="162fb-111">These WMI command classes are implemented by Windows PowerShell.</span></span> <span data-ttu-id="162fb-112">Ces classes sont incluses dans ce kit de développement logiciel (SDK) à des fins d’exhaustivité uniquement.</span><span class="sxs-lookup"><span data-stu-id="162fb-112">These classes are included in this software development kit (SDK) for completeness only.</span></span> <span data-ttu-id="162fb-113">Les membres de ces classes ne peuvent pas être utilisés directement, ni être utilisés pour dériver d’autres classes.</span><span class="sxs-lookup"><span data-stu-id="162fb-113">The members of these classes cannot be used directly, nor should they be used to derive other classes.</span></span>



| <span data-ttu-id="162fb-114">Classe</span><span class="sxs-lookup"><span data-stu-id="162fb-114">Class</span></span>                   | <span data-ttu-id="162fb-115">Description</span><span class="sxs-lookup"><span data-stu-id="162fb-115">Description</span></span>                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="162fb-116">GetWmiObjectCommand</span><span class="sxs-lookup"><span data-stu-id="162fb-116">GetWmiObjectCommand</span></span>     | <span data-ttu-id="162fb-117">Obtient des instances de classes WMI ou des informations sur les classes disponibles.</span><span class="sxs-lookup"><span data-stu-id="162fb-117">Gets instances of WMI classes or information about the available classes.</span></span><br/> <span data-ttu-id="162fb-118">Pour obtenir des exemples et des informations détaillées sur les paramètres, consultez l’applet de commande [obtenir-WmiObject](/previous-versions//dd315295(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="162fb-118">See the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/> |
| <span data-ttu-id="162fb-119">InvokeWmiMethod</span><span class="sxs-lookup"><span data-stu-id="162fb-119">InvokeWmiMethod</span></span>         | <span data-ttu-id="162fb-120">Appelle les méthodes WMI.</span><span class="sxs-lookup"><span data-stu-id="162fb-120">Calls WMI methods.</span></span><br/> <span data-ttu-id="162fb-121">Pour obtenir des exemples et des informations détaillées sur les paramètres, consultez l’applet de commande [Invoke-WmiMethod](/previous-versions//dd315300(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="162fb-121">See the [Invoke-WmiMethod](/previous-versions//dd315300(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                                                     |
| <span data-ttu-id="162fb-122">RegisterWmiEventCommand</span><span class="sxs-lookup"><span data-stu-id="162fb-122">RegisterWmiEventCommand</span></span> | <span data-ttu-id="162fb-123">S’abonne à un événement WMI.</span><span class="sxs-lookup"><span data-stu-id="162fb-123">Subscribes to a WMI event.</span></span><br/> <span data-ttu-id="162fb-124">Consultez l’applet de commande [Register-WmiEvent](/previous-versions//dd315242(v=technet.10)) pour obtenir des exemples et des informations détaillées sur les paramètres.</span><span class="sxs-lookup"><span data-stu-id="162fb-124">See the [Register-WmiEvent](/previous-versions//dd315242(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                                            |
| <span data-ttu-id="162fb-125">RemoveWmiObject</span><span class="sxs-lookup"><span data-stu-id="162fb-125">RemoveWmiObject</span></span>         | <span data-ttu-id="162fb-126">Supprime une instance d’une classe WMI existante.</span><span class="sxs-lookup"><span data-stu-id="162fb-126">Deletes an instance of an existing WMI class.</span></span><br/> <span data-ttu-id="162fb-127">Pour obtenir des exemples et des informations détaillées sur les paramètres, consultez l’applet de commande [Remove-WmiObject](/previous-versions//dd347605(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="162fb-127">See the [Remove-WmiObject](/previous-versions//dd347605(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                          |
| <span data-ttu-id="162fb-128">SetWmiInstance</span><span class="sxs-lookup"><span data-stu-id="162fb-128">SetWmiInstance</span></span>          | <span data-ttu-id="162fb-129">Crée ou met à jour une instance d’une classe WMI existante.</span><span class="sxs-lookup"><span data-stu-id="162fb-129">Creates or updates an instance of an existing WMI class.</span></span><br/> <span data-ttu-id="162fb-130">Pour obtenir des exemples et des informations détaillées sur les paramètres, consultez l’applet de commande [Set-WmiInstance](/previous-versions//dd315391(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="162fb-130">See the [Set-WmiInstance](/previous-versions//dd315391(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                |



 

 

