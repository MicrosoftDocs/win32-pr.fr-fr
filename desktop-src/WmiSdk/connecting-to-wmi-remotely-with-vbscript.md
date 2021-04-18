---
description: Vous pouvez créer une connexion à distance à WMI avec VBScript en créant un objet de connexion. Cet objet contient le nom de l’ordinateur, l’espace de noms WMI auquel vous souhaitez vous connecter, ainsi que les informations d’identification et les niveaux d’authentification appropriés.
ms.assetid: b2ad262b-148d-47cc-8be7-6df99245aa7f
ms.tgt_platform: multiple
title: Connexion à WMI à distance avec VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 07cff2f0cd0ca06de059d9b39e36d715b5555eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106522687"
---
# <a name="connecting-to-wmi-remotely-with-vbscript"></a><span data-ttu-id="1ae95-104">Connexion à WMI à distance avec VBScript</span><span class="sxs-lookup"><span data-stu-id="1ae95-104">Connecting to WMI Remotely with VBScript</span></span>

<span data-ttu-id="1ae95-105">Vous pouvez créer une connexion à distance à WMI avec VBScript en créant un objet de connexion.</span><span class="sxs-lookup"><span data-stu-id="1ae95-105">You can create a remote connection to WMI with VBScript by creating a connection object.</span></span> <span data-ttu-id="1ae95-106">Cet objet contient le nom de l’ordinateur, l’espace de noms WMI auquel vous souhaitez vous connecter, ainsi que les informations d’identification et les niveaux d’authentification appropriés.</span><span class="sxs-lookup"><span data-stu-id="1ae95-106">This object contains the name of the computer, the WMI namespace you want to connect to, as well as any relevant credentials and authentication levels.</span></span>

<span data-ttu-id="1ae95-107">**Pour vous connecter à un système distant à l’aide de VBScript**</span><span class="sxs-lookup"><span data-stu-id="1ae95-107">**To connect to a remote system using VBScript**</span></span>

1.  <span data-ttu-id="1ae95-108">Spécifiez les informations de connexion, telles que le nom de l’ordinateur distant, les informations d’identification et le niveau d’authentification pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="1ae95-108">Specify the connection information such as the remote computer name, credentials, and the authentication level for the connection.</span></span>

    <span data-ttu-id="1ae95-109">Si vous vous connectez à un ordinateur distant à l’aide des mêmes informations d’identification (domaine et nom d’utilisateur) que vous avez ouvert une session, vous pouvez spécifier les informations de connexion dans un [moniker](constructing-a-moniker-string.md) [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), comme décrit dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="1ae95-109">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you can specify the connection information in a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)[moniker](constructing-a-moniker-string.md), as described in the following code sample.</span></span>

    ```VB
    strComputer = "Computer_B"
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & "\Root\CIMv2")
    ```

    

    <span data-ttu-id="1ae95-110">En règle générale, vous devez spécifier l’espace de noms WMI auquel se connecter sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="1ae95-110">Generally speaking, you should specify the WMI namespace to connect to on the remote computer.</span></span> <span data-ttu-id="1ae95-111">En effet, il est possible que l’espace de noms par défaut ne soit pas le même sur des ordinateurs différents.</span><span class="sxs-lookup"><span data-stu-id="1ae95-111">This is because it is possible that the default namespace is not the same on different computers.</span></span> <span data-ttu-id="1ae95-112">La spécification de l’espace de noms garantit que vous vous connectez au même espace de noms sur tous les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="1ae95-112">Specifying the namespace ensures that you connect to the same namespace on all computers.</span></span>

    <span data-ttu-id="1ae95-113">Pour plus d’informations sur les constantes et les chaînes de script VBScript pour l’utilisation de la connexion moniker, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="1ae95-113">For more information on VBScript constants and scripting strings for using the moniker connection, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

2.  <span data-ttu-id="1ae95-114">Si vous vous connectez à un ordinateur distant dans un autre domaine ou à l’aide d’un nom d’utilisateur et d’un mot de passe différents, vous devez utiliser la méthode [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="1ae95-114">If you connect to a remote computer in a different domain or using a different user name and password, then you must use the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

    <span data-ttu-id="1ae95-115">Comme pour un moniker, vous utilisez **ConnectServer** pour spécifier les informations d’identification, le niveau d’authentification et l’espace de noms pour la connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="1ae95-115">As with a moniker, you use **ConnectServer** to specify the credentials, authentication level, and namespace for the remote connection.</span></span> <span data-ttu-id="1ae95-116">L’exemple de code suivant décrit l’utilisation de ConnectServer pour accéder à un ordinateur distant à l’aide d’un compte et d’un mot de passe d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="1ae95-116">The following code sample describes using ConnectServer to access a remote computer using an administrator account and password.</span></span>

    ```VB
    strComputer = "Computer_B"
    Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                         "Root\CIMv2", _
                                                         "fabrikam\administrator", _
                                                         "password")
    ```

    

3.  <span data-ttu-id="1ae95-117">Quand vous utilisez la fonction [**ConnectServer**](swbemlocator-connectserver.md) pour des connexions distantes, définissez l’emprunt d’identité et l’authentification sur l’objet de sécurité obtenu par un appel à [**SWbemServices. Security**](swbemservices-security-.md).</span><span class="sxs-lookup"><span data-stu-id="1ae95-117">When using the [**ConnectServer**](swbemlocator-connectserver.md) function for remote connections, set impersonation and authentication on the security object obtained by a call to [**SWbemServices.Security**](swbemservices-security-.md).</span></span> <span data-ttu-id="1ae95-118">Vous pouvez utiliser l’énumération [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) pour spécifier le niveau d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="1ae95-118">You can use the enumeration [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) to specify impersonation level.</span></span>

    <span data-ttu-id="1ae95-119">L’exemple de code suivant définit le niveau d’emprunt d’identité pour l’exemple de code VBScript précédent.</span><span class="sxs-lookup"><span data-stu-id="1ae95-119">The following code sample sets the impersonation level for the previous VBScript code sample.</span></span>

    ```VB
    objSWbemServices.Security_.ImpersonationLevel = 3
    ```

    

    <span data-ttu-id="1ae95-120">Notez que certaines connexions nécessitent un niveau d’authentification spécifique.</span><span class="sxs-lookup"><span data-stu-id="1ae95-120">Note that some connections require a specific authentication level.</span></span> <span data-ttu-id="1ae95-121">Pour plus d’informations, consultez Définition de la [sécurité des processus des applications clientes](setting-client-application-process-security.md) et [sécurisation des scripts des clients](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="1ae95-121">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md) and [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

    <span data-ttu-id="1ae95-122">En particulier, vous devez définir le niveau d’authentification sur la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC C** ou 6 si l’espace de noms sur lequel vous vous connectez sur l’ordinateur distant requiert une connexion chiffrée avant de retourner des données.</span><span class="sxs-lookup"><span data-stu-id="1ae95-122">In particular, you should set the authentication level to **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** or 6 if the namespace to which you are connecting on the remote computer requires an encrypted connection before it will return data.</span></span> <span data-ttu-id="1ae95-123">Vous pouvez également utiliser ce niveau d’authentification, même si l’espace de noms ne l’exige pas.</span><span class="sxs-lookup"><span data-stu-id="1ae95-123">You can also use this authentication level, even if the namespace does not require it.</span></span> <span data-ttu-id="1ae95-124">Cela permet de s’assurer que les données sont chiffrées lorsqu’elles traversent le réseau.</span><span class="sxs-lookup"><span data-stu-id="1ae95-124">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="1ae95-125">Si vous tentez de définir un niveau d’authentification inférieur à celui autorisé, un message d’accès refusé est retourné.</span><span class="sxs-lookup"><span data-stu-id="1ae95-125">If you attempt to set a lower authentication level than is allowed, an access denied message will be returned.</span></span> <span data-ttu-id="1ae95-126">Pour plus d’informations, consultez [la page exiger une connexion chiffrée à un espace de noms](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="1ae95-126">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="1ae95-127">Une fois que vous avez établi votre connexion, vous pouvez continuer à accéder aux données WMI.</span><span class="sxs-lookup"><span data-stu-id="1ae95-127">Once you have made your connection, you can continue to access WMI data.</span></span> <span data-ttu-id="1ae95-128">Pour plus d’informations, consultez [tâches WMI pour les scripts et les applications](wmi-tasks-for-scripts-and-applications.md).</span><span class="sxs-lookup"><span data-stu-id="1ae95-128">For more information, see [WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1ae95-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="1ae95-129">Examples</span></span>

<span data-ttu-id="1ae95-130">Pour obtenir un exemple VBScript plus grand, consultez la section exemples dans la page de référence de [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="1ae95-130">For a larger VBScript sample, see the Examples section in the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) reference page.</span></span>

<span data-ttu-id="1ae95-131">L’exemple de code VBScript suivant se connecte à un groupe d’ordinateurs distants dans le même domaine en créant un tableau de noms d’ordinateurs distants, puis en affichant les noms des appareils Plug-and-Play (instances de [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)) sur chaque ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1ae95-131">The following VBScript code example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of [**Win32\_PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)—on each computer.</span></span> <span data-ttu-id="1ae95-132">Pour exécuter le script ci-dessous, vous devez être administrateur sur les ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="1ae95-132">To run the script below, you must be an administrator on the remote computers.</span></span> <span data-ttu-id="1ae95-133">Notez que le « \\ \\ » requis avant le nom de l’ordinateur distant est ajouté par le script après le paramètre niveau d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="1ae95-133">Note that the "\\\\" required before the remote computer name is added by the script following the impersonation level setting.</span></span> <span data-ttu-id="1ae95-134">Pour plus d’informations sur les chemins d’accès WMI, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="1ae95-134">For more information about WMI paths, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" & strComputer& "\Root\CIMv2") 
    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



<span data-ttu-id="1ae95-135">L’exemple de code VBScript suivant vous permet de vous connecter à un ordinateur distant à l’aide d’autres informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="1ae95-135">The following VBScript code example enables you to connect to a remote computer using different credentials.</span></span> <span data-ttu-id="1ae95-136">Par exemple, un ordinateur distant dans un domaine différent ou qui se connecte à un ordinateur distant nécessitant un nom d’utilisateur et un mot de passe différents.</span><span class="sxs-lookup"><span data-stu-id="1ae95-136">For example, a remote computer in a different domain or connecting to a remote computer requiring a different user name and password.</span></span> <span data-ttu-id="1ae95-137">Dans ce cas, utilisez la connexion [**SWbemServices. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="1ae95-137">In this case, use the [**SWbemServices.ConnectServer**](swbemlocator-connectserver.md) connection.</span></span>


```VB
' Full Computer Name
' can be found by right-clicking My Computer,
' then click Properties, then click the Computer Name tab)
' or use the computer's IP address
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```



## <a name="related-topics"></a><span data-ttu-id="1ae95-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ae95-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ae95-139">Connexion à WMI sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="1ae95-139">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
