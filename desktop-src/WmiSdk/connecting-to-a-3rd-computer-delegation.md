---
description: Lorsque vous exécutez un script sur un système local qui obtient des données à partir d’un système distant, WMI fournit vos informations d’identification au fournisseur des données sur le système distant.
ms.assetid: e27ff207-b067-47df-9706-e8af51646d28
ms.tgt_platform: multiple
title: Délégation avec WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8a624f3d437d977ff73b3854a59cfd634350e7
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104393867"
---
# <a name="delegating-with-wmi"></a><span data-ttu-id="71e74-103">Délégation avec WMI</span><span class="sxs-lookup"><span data-stu-id="71e74-103">Delegating with WMI</span></span>

<span data-ttu-id="71e74-104">Lorsque vous exécutez un script sur un système local qui obtient des données à partir d’un système distant, WMI fournit vos informations d’identification au fournisseur des données sur le système distant.</span><span class="sxs-lookup"><span data-stu-id="71e74-104">When you run a script on a local system that obtains data from a remote system, WMI supplies your credentials to the provider of the data on the remote system.</span></span> <span data-ttu-id="71e74-105">Cela nécessite uniquement un niveau d’emprunt d’identité d' **emprunt d’identité**, car un seul tronçon réseau est requis.</span><span class="sxs-lookup"><span data-stu-id="71e74-105">This requires only an impersonation level of **Impersonate**, because only one network hop is required.</span></span> <span data-ttu-id="71e74-106">Toutefois, si le script se connecte à WMI sur le système distant et tente d’ouvrir un fichier journal sur un autre système distant, le script échoue, sauf si le niveau d’emprunt d’identité est **délégué**.</span><span class="sxs-lookup"><span data-stu-id="71e74-106">However, if the script connects to WMI on the remote system and attempts to open a log file on an additional remote system, then the script fails unless the impersonation level is **Delegate**.</span></span> <span data-ttu-id="71e74-107">Le niveau d’emprunt d’identité **délégué** est requis par toute opération qui implique plusieurs sauts réseau.</span><span class="sxs-lookup"><span data-stu-id="71e74-107">**Delegate** impersonation level is required by any operation that involves more than one network hop.</span></span> <span data-ttu-id="71e74-108">Pour plus d’informations sur la sécurité DCOM dans WMI, consultez Définition de la [sécurité des processus des applications clientes](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="71e74-108">For more information about DCOM security in WMI, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="71e74-109">Pour plus d’informations sur la connexion d’un saut de réseau entre deux ordinateurs, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="71e74-109">For more information about a one-network hop connection between two computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="71e74-110">**Pour utiliser la délégation pour se connecter à un ordinateur par le biais d’un autre ordinateur**</span><span class="sxs-lookup"><span data-stu-id="71e74-110">**To use delegation to connect to a computer through another computer**</span></span>

1.  <span data-ttu-id="71e74-111">Activez la délégation dans Active Directory (**Active Directory les utilisateurs et les ordinateurs** dans les **tâches d’administration** du **panneau de configuration** ) sur le contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="71e74-111">Enable delegation in Active Directory (**Active Directory Users and Computers** in **Control Panel** **Administrative Tasks**) on the domain controller.</span></span> <span data-ttu-id="71e74-112">Le compte sur le système distant doit être marqué comme **approuvé pour la délégation** et le compte sur le système local ne doit pas être marqué comme étant **sensible et ne peut pas être délégué**.</span><span class="sxs-lookup"><span data-stu-id="71e74-112">The account on the remote system must be marked as **Trusted for delegation** and the account on the local system must not be marked as **Account is sensitive and cannot be delegated**.</span></span> <span data-ttu-id="71e74-113">le système local, le système distant et le contrôleur de domaine doivent être membres du même domaine ou dans des domaines approuvés.</span><span class="sxs-lookup"><span data-stu-id="71e74-113">the local system, the remote system, and the domain controller must be members of the same domain or in trusted domains.</span></span>

    <span data-ttu-id="71e74-114">**Remarque**  L’utilisation de la délégation est un risque pour la sécurité, car elle permet aux processus en dehors de votre contrôle direct d’utiliser vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="71e74-114">**Note**  Using delegation is a security risk because it gives processes outside of your direct control the ability to use your credentials.</span></span>

2.  <span data-ttu-id="71e74-115">Modifiez votre code de la manière suivante pour indiquer que vous souhaitez utiliser la délégation.</span><span class="sxs-lookup"><span data-stu-id="71e74-115">Modify your code in the following manner to indicate that you want to use delegation.</span></span>

    <dl> <dt>

    <span data-ttu-id="71e74-116"><span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>PowerShell</span><span class="sxs-lookup"><span data-stu-id="71e74-116"><span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>PowerShell</span></span>
    </dt> <dd>

    <span data-ttu-id="71e74-117">Définissez le paramètre *-emprunt d’identité* de l’applet de commande WMI sur **déléguer**.</span><span class="sxs-lookup"><span data-stu-id="71e74-117">Set the *-Impersonation* parameter on the WMI cmdlet to **Delegate**.</span></span>

    </dd> <dt>

    <span data-ttu-id="71e74-118"><span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>VBScript</span><span class="sxs-lookup"><span data-stu-id="71e74-118"><span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>VBScript</span></span>
    </dt> <dd>

    <span data-ttu-id="71e74-119">Définissez le paramètre *ImpersonationLevel* à **déléguer** dans l’appel à [SWbemLocator. ConnectServer](swbemlocator-connectserver.md) ou au **délégué** dans la chaîne de [moniker](constructing-a-moniker-string.md) .</span><span class="sxs-lookup"><span data-stu-id="71e74-119">Set the *impersonationLevel* parameter to **Delegate** in the call to [SWbemLocator.ConnectServer](swbemlocator-connectserver.md) or **Delegate** in the [moniker](constructing-a-moniker-string.md) string.</span></span> <span data-ttu-id="71e74-120">Vous pouvez également définir l’emprunt d’identité dans un objet [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="71e74-120">You can also set the impersonation in a [**SWbemSecurity**](swbemsecurity.md)object.</span></span>

    </dd> <dt>

    <span data-ttu-id="71e74-121"><span id="C__"></span><span id="c__"></span>C++</span><span class="sxs-lookup"><span data-stu-id="71e74-121"><span id="C__"></span><span id="c__"></span>C++</span></span>
    </dt> <dd>

    <span data-ttu-id="71e74-122">Définissez le paramètre de niveau d’emprunt d’identité sur **RPC \_ C \_ IMP \_ Level \_ Delegate** dans l’appel à [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="71e74-122">Set the impersonation level parameter to **RPC\_C\_IMP\_LEVEL\_DELEGATE** in the call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="71e74-123">Pour plus d’informations sur le moment d’effectuer ces appels, consultez [initialisation de com pour une application WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="71e74-123">For more information about when to make these calls, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="71e74-124">Pour transmettre l’identité du client aux serveurs COM distants en C++, définissez le masquage dans l’appel à [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="71e74-124">To pass the client identity to remote COM servers in C++, set cloaking in the call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="71e74-125">Pour plus d’informations, consultez [masquage](../com/cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="71e74-125">For more information, see [Cloaking](../com/cloaking.md).</span></span>

    </dd> </dl>

## <a name="examples"></a><span data-ttu-id="71e74-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="71e74-126">Examples</span></span>

<span data-ttu-id="71e74-127">L’exemple de code suivant montre une chaîne de moniker qui définit l’emprunt d’identité à **déléguer**.</span><span class="sxs-lookup"><span data-stu-id="71e74-127">The following code example shows a moniker string that sets the impersonation to **Delegate**.</span></span> <span data-ttu-id="71e74-128">N’oubliez pas que l’autorité doit avoir la valeur Kerberos.</span><span class="sxs-lookup"><span data-stu-id="71e74-128">Be aware that the authority must be set to Kerberos.</span></span>


```vb
set objWMIServices = Getobject("winmgmts:{impersonationLevel=Delegate,authority=kerberos:MyDomain\Computer_B}!\\ComputerB\Root\CIMv2")
```



<span data-ttu-id="71e74-129">L’exemple de code suivant montre comment définir l’emprunt d’identité sur **Delegate** (une valeur de 4) à l’aide de [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="71e74-129">The following code example shows how to set impersonation to **Delegate** (a value of 4) using [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span>


```vb
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = objLocator.ConnectServer(Computer_B, _
                                             "Root\CIMv2", _
                                             AdminAccount, _
                                             MyPassword, _
                                             "kerberos:Domain\Computer_B")
objWMIService.Security_.ImpersonationLevel = 4
```



## <a name="related-topics"></a><span data-ttu-id="71e74-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="71e74-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71e74-131">Sécurisation d’une connexion WMI à distance</span><span class="sxs-lookup"><span data-stu-id="71e74-131">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> <dt>

[<span data-ttu-id="71e74-132">Création de processus à distance avec WMI</span><span class="sxs-lookup"><span data-stu-id="71e74-132">Creating Processes Remotely with WMI</span></span>](creating-processes-remotely.md)
</dt> </dl>

 

 
