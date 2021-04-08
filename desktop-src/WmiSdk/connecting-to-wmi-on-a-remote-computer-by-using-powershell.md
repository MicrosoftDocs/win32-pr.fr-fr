---
description: Connexion à WMI à distance avec PowerShell
ms.assetid: 9a06f0c3-2845-48aa-9988-79cc4607ce19
ms.tgt_platform: multiple
title: Connexion à WMI à distance avec PowerShell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a2bb1ad982a20a10dbadd89856d118f1be9bd82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755349"
---
# <a name="connecting-to-wmi-remotely-with-powershell"></a><span data-ttu-id="a5e89-103">Connexion à WMI à distance avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="a5e89-103">Connecting to WMI Remotely with PowerShell</span></span>

<span data-ttu-id="a5e89-104">Windows PowerShell fournit un mécanisme simple pour se connecter à Windows Management Instrumentation (WMI) sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="a5e89-104">Windows PowerShell provides a simple mechanism to connect to Windows Management Instrumentation (WMI) on a remote computer.</span></span> <span data-ttu-id="a5e89-105">Les connexions à distance dans WMI sont affectées par le [pare-feu Windows](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), les paramètres DCOM et le [contrôle de compte d’utilisateur (UAC)](/previous-versions/aa905108(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="a5e89-105">Remote connections in WMI are affected by the [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), DCOM settings, and [User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)).</span></span> <span data-ttu-id="a5e89-106">Pour plus d’informations sur la configuration des connexions à distance, consultez [connexion à WMI à distance à partir de Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span><span class="sxs-lookup"><span data-stu-id="a5e89-106">For more information about configuring remote connections, see [Connecting to WMI Remotely Starting with Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

<span data-ttu-id="a5e89-107">Les exemples de cette rubrique sont basés sur les VBScripts de la [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="a5e89-107">The examples in this topic are based on the VBScripts from [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="a5e89-108">Tous les exemples de cette rubrique utilisent l’applet de commande [« obtient-WmiObject »](/previous-versions//dd315295(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="a5e89-108">All of the examples in this topic use the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="a5e89-109">Pour plus d’informations, consultez la rubrique [obtenir-WmiObject](/previous-versions//dd315295(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="a5e89-109">For more information, see [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span></span>

## <a name="windows-powershell-examples"></a><span data-ttu-id="a5e89-110">Exemples Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a5e89-110">Windows PowerShell examples</span></span>

<span data-ttu-id="a5e89-111">Lors de la création d’une connexion à un ordinateur distant, un utilisateur peut spécifier les informations de connexion, telles que le nom de l’ordinateur distant, les informations d’identification et le niveau d’authentification de la connexion.</span><span class="sxs-lookup"><span data-stu-id="a5e89-111">When creating a connection to a remote computer, a user can specify the connection information such as the remote computer name, credentials, and the authentication level for the connection.</span></span> <span data-ttu-id="a5e89-112">Les exemples suivants montrent comment se connecter à un ordinateur distant à l’aide de différents jeux d’informations d’identification et comment accéder aux informations WMI.</span><span class="sxs-lookup"><span data-stu-id="a5e89-112">The following examples illustrate how to connect to a remote computer by using different sets of credentials and how to access WMI information.</span></span>

<span data-ttu-id="a5e89-113">L’exemple Windows PowerShell suivant illustre la définition du niveau d’emprunt d’identité :</span><span class="sxs-lookup"><span data-stu-id="a5e89-113">The following Windows PowerShell example shows setting the impersonation level:</span></span>


```PowerShell

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -ComputerName Computer_B
```



<span data-ttu-id="a5e89-114">Dans l’exemple précédent, l’utilisateur se connecte à un ordinateur distant en utilisant les mêmes informations d’identification (domaine et nom d’utilisateur) avec lesquelles il s’est connecté.</span><span class="sxs-lookup"><span data-stu-id="a5e89-114">In the preceding example, the user connects to a remote computer by using the same credentials (domain and user name) that they logged on with.</span></span> <span data-ttu-id="a5e89-115">L’utilisateur a également demandé à utiliser l’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="a5e89-115">The user also requested to use impersonation.</span></span> <span data-ttu-id="a5e89-116">Contrairement à l’exemple VBScript d’origine, une chaîne de moniker n’est pas nécessaire, car le niveau d’emprunt d’identité est défini par la propriété « emprunt d’identité ».</span><span class="sxs-lookup"><span data-stu-id="a5e89-116">Unlike the original VBScript example, a moniker string is not needed because the impersonation level is set by the "Impersonation" property.</span></span> <span data-ttu-id="a5e89-117">Par défaut, le niveau d’emprunt d’identité a la valeur 3 (emprunter l’identité).</span><span class="sxs-lookup"><span data-stu-id="a5e89-117">By default, the impersonation level is set to 3 (Impersonate).</span></span>

<span data-ttu-id="a5e89-118">L’exemple répertorie toutes les instances de la classe de [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) qui s’exécutent sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="a5e89-118">The example lists all the instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class that are running on remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="a5e89-119">Vous devez spécifier l’espace de noms WMI auquel se connecter sur l’ordinateur distant, car il est possible que l’espace de noms par défaut ne soit pas le même sur des ordinateurs différents.</span><span class="sxs-lookup"><span data-stu-id="a5e89-119">You should specify the WMI namespace to connect to on the remote computer because it is possible that the default namespace is not the same on different computers.</span></span>

 

<span data-ttu-id="a5e89-120">L’exemple Windows PowerShell suivant montre comment se connecter à un ordinateur distant avec des informations d’identification différentes et définir le niveau d’emprunt d’identité à 3, ce qui correspond à l’emprunt d’identité :</span><span class="sxs-lookup"><span data-stu-id="a5e89-120">The following Windows PowerShell example shows how to connect to a remote computer with different credentials and to set the impersonation level to 3, which is Impersonate:</span></span>


```PowerShell

$Computer = "atl-dc-01"

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -Credential `
FABRIKAM\administrator -ComputerName $Computer
```



<span data-ttu-id="a5e89-121">Dans l’exemple précédent, le nom de l’ordinateur a été affecté à la variable $Computer.</span><span class="sxs-lookup"><span data-stu-id="a5e89-121">In the preceding example, the computer name was assigned to the $Computer variable.</span></span> <span data-ttu-id="a5e89-122">L’utilisateur se connecte à un ordinateur distant en utilisant des informations d’identification spécifiques (domaine et nom d’utilisateur) et demande l’emprunt d’identité pour le niveau d’authentification.</span><span class="sxs-lookup"><span data-stu-id="a5e89-122">The user connects to a remote computer by using specific credentials (domain and user name) and requests impersonation for the authentication level.</span></span>

> [!Note]  
> <span data-ttu-id="a5e89-123">Le caractère d’accent grave ( \` ) est utilisé pour indiquer un saut de ligne.</span><span class="sxs-lookup"><span data-stu-id="a5e89-123">The grave-accent character (\`) is used to indicate a line break.</span></span> <span data-ttu-id="a5e89-124">Elle est équivalente au trait de soulignement ( \_ ) dans VBScript.</span><span class="sxs-lookup"><span data-stu-id="a5e89-124">It is equivalent to the underscore character (\_) in VBScript.</span></span>

 

<span data-ttu-id="a5e89-125">L’exemple Windows PowerShell suivant se connecte à un groupe d’ordinateurs distants dans le même domaine en créant un tableau de noms d’ordinateurs distants, puis en affichant les noms des appareils Plug-and-Play (instances de [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)) sur chaque ordinateur :</span><span class="sxs-lookup"><span data-stu-id="a5e89-125">The following Windows PowerShell example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of [**Win32\_PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)—on each computer:</span></span>


```PowerShell
$ArrComputers = "Computer1", "Computer2", "Computer3"
foreach ($Computer in $ArrComputers) 
{
write-host ""
write-host "===================================="
write-host "Computer: $Computer"
write-host "===================================="

write-host "-----------------------------------"
write-host "Win32_PnPEntity instance"
write-host "-----------------------------------"

$ColItems = Get-WmiObject -Class Win32_PnPEntity -Namespace "root\cimv2" -Computer $Computer
$ColItems[0..47] | Format-List Name, Status
}
```



> [!Note]  
> <span data-ttu-id="a5e89-126">Pour exécuter le script Windows PowerShell précédent, vous devez être administrateur sur les ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="a5e89-126">To run the preceding Windows PowerShell script, you must be an administrator on the remote computers.</span></span> <span data-ttu-id="a5e89-127">En outre, en rapport avec l’exemple précédent, notez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="a5e89-127">Also, relating to the preceding example, note the following:</span></span>

 

-   <span data-ttu-id="a5e89-128">Les noms d’ordinateur dans le tableau doivent être placés entre guillemets, car il s’agit de chaînes.</span><span class="sxs-lookup"><span data-stu-id="a5e89-128">The computer names in the array must be enclosed in quotation marks because they are strings.</span></span>
-   <span data-ttu-id="a5e89-129">Les objets retournés par la [prise en main](/previous-versions//dd315295(v=technet.10)) sont assignés à la variable $ColItems.</span><span class="sxs-lookup"><span data-stu-id="a5e89-129">The objects returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) are assigned to the $ColItems variable.</span></span>
-   <span data-ttu-id="a5e89-130">L’opérateur \[ \] de plage limite la liste des appareils Plug-and-Play à 48 instances.</span><span class="sxs-lookup"><span data-stu-id="a5e89-130">The range operator \[\] limited the list of Plug and Play devices to 48 instances.</span></span> <span data-ttu-id="a5e89-131">Pour plus d’informations, consultez [à propos des \_ opérateurs](/previous-versions//dd347588(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="a5e89-131">For more information, see [About\_Operators](/previous-versions//dd347588(v=technet.10)).</span></span>
-   <span data-ttu-id="a5e89-132">« \| » Est le caractère de pipeline.</span><span class="sxs-lookup"><span data-stu-id="a5e89-132">The "\|" is the pipeline character.</span></span> <span data-ttu-id="a5e89-133">L’objet retourné par ColItems est envoyé à l’applet de commande [format-list]( /previous-versions//dd347700(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="a5e89-133">The object returned by ColItems is sent to the [Format-List]( /previous-versions//dd347700(v=technet.10)) cmdlet.</span></span>

<span data-ttu-id="a5e89-134">L’exemple Windows PowerShell suivant vous permet de vous connecter à un ordinateur distant situé sur un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="a5e89-134">The following Windows PowerShell example enables you to connect to a remote computer on a different domain.</span></span> <span data-ttu-id="a5e89-135">Cet exemple affiche également les noms des processus pour les instances de [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="a5e89-135">This example also displays the process names for instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) on the remote computer.</span></span>


```PowerShell
$Computer = "FullComputerName" 
$Domain = "DOMAIN"
$Credential = Get-Credential
$ColItems = Get-WmiObject -Class Win32_Process -Authority "ntlmdomain:$Domain" `
-Credential $Credential -Locale "MS_409" -Namespace "root\cimv2"  -ComputerName $Computer

foreach ($ObjItem in $colItems) 
{
write-host "Process Name:" $ObjItem.name
}
```



> [!Note]  
> <span data-ttu-id="a5e89-136">Pour exécuter le script Windows PowerShell précédent, vous devez être administrateur sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="a5e89-136">To run the preceding Windows PowerShell script, you must be an administrator on the remote computer.</span></span>

 

<span data-ttu-id="a5e89-137">Dans l’exemple précédent, l’utilisateur se connecte à un ordinateur distant situé sur un autre domaine et spécifie des paramètres régionaux préférés.</span><span class="sxs-lookup"><span data-stu-id="a5e89-137">In the preceding example, the user connects to a remote computer on a different domain and specifies a preferred locale.</span></span> <span data-ttu-id="a5e89-138">La commande de [récupération des informations d’identification](/previous-versions//dd315327(v=technet.10)) demande les informations d’identification de l’utilisateur et assigne les informations d’identification à un objet.</span><span class="sxs-lookup"><span data-stu-id="a5e89-138">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) command requests the user's credentials and assigns the credentials to an object.</span></span> <span data-ttu-id="a5e89-139">L’exemple répertorie également les noms des instances de la classe de [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) qui s’exécutent sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a5e89-139">The example also lists the names of instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class that are running on the computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5e89-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a5e89-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5e89-141">Connexion à WMI sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="a5e89-141">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
