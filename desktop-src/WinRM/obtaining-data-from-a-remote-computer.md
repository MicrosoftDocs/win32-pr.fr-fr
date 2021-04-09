---
title: Obtention de données à partir d’un ordinateur distant
description: Vous pouvez obtenir des données ou gérer des ressources sur des ordinateurs distants, ainsi que sur l’ordinateur local. La connexion à un ordinateur distant dans un script Windows Remote Management est très similaire à l’établissement d’une connexion locale.
ms.assetid: 578eee80-a6c1-4456-9683-14e0a3386248
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8cfc95a73dab4c9a0f19481b7ba41f3c40a3862d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842317"
---
# <a name="obtaining-data-from-a-remote-computer"></a><span data-ttu-id="c3777-104">Obtention de données à partir d’un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="c3777-104">Obtaining Data from a Remote Computer</span></span>

<span data-ttu-id="c3777-105">Vous pouvez obtenir des données ou gérer des ressources sur des ordinateurs distants, ainsi que sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c3777-105">You can obtain data or manage resources on remote computers as well as the local computer.</span></span> <span data-ttu-id="c3777-106">La connexion à un ordinateur distant dans un script Windows Remote Management est très similaire à l’établissement d’une connexion locale.</span><span class="sxs-lookup"><span data-stu-id="c3777-106">Connecting to a remote computer in a Windows Remote Management script is very similar to making a local connection.</span></span> <span data-ttu-id="c3777-107">Les données d’instance WMI sont disponibles et, si l’ordinateur distant dispose d’un matériel BMC capable de communiquer à l’aide du protocole WS-Management, les données [IPMI (Intelligent Platform Management Interface)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) sont également disponibles.</span><span class="sxs-lookup"><span data-stu-id="c3777-107">WMI instance data is available and, if the remote computer has BMC hardware that can communicate using the WS-Management protocol, then [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) data is also available.</span></span> <span data-ttu-id="c3777-108">Pour plus d’informations, consultez [Windows Remote Management et WMI](windows-remote-management-and-wmi.md) et [gestion du matériel à distance](remote-hardware-management.md).</span><span class="sxs-lookup"><span data-stu-id="c3777-108">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md) and [Remote Hardware Management](remote-hardware-management.md).</span></span>

<span data-ttu-id="c3777-109">Vous devrez peut-être créer un objet [**ConnectionOptions**](connectionoptions.md) pour spécifier des informations sur le type d’authentification demandé pour l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="c3777-109">You may need to create a [**ConnectionOptions**](connectionoptions.md) object to specify information about the type of authentication requested for the logon.</span></span>

<span data-ttu-id="c3777-110">Si le compte sur l’ordinateur distant possède les mêmes nom d’utilisateur et mot de passe d’ouverture de session, les seules informations supplémentaires dont vous avez besoin sont le transport, le nom de domaine et le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c3777-110">If the account on the remote computer has the same logon username and password, the only extra information you need is the transport, the domain name, and the computer name.</span></span> <span data-ttu-id="c3777-111">En raison du [contrôle de compte d’utilisateur (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista), le compte distant doit être un compte de domaine et un membre du groupe administrateurs d’ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="c3777-111">Because of [User Account Control (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista), the remote account must be a domain account and a member of the remote computer Administrators group.</span></span> <span data-ttu-id="c3777-112">Si le compte est un membre de l’ordinateur local du groupe administrateurs, le contrôle de compte d’utilisateur n’autorise pas l’accès au service WinRM.</span><span class="sxs-lookup"><span data-stu-id="c3777-112">If the account is a local computer member of the Administrators group, then UAC does not allow access to the WinRM service.</span></span> <span data-ttu-id="c3777-113">Pour accéder à un service WinRM distant dans un groupe de travail, le filtrage UAC pour les comptes locaux doit être désactivé en créant l’entrée de Registre DWORD suivante et en définissant sa valeur sur 1 : **\[ HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Policies \\ System \] LocalAccountTokenFilterPolicy**.</span><span class="sxs-lookup"><span data-stu-id="c3777-113">To access a remote WinRM service in a workgroup, UAC filtering for local accounts must be disabled by creating the following DWORD registry entry and setting its value to 1: **\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\System\] LocalAccountTokenFilterPolicy**.</span></span>

<span data-ttu-id="c3777-114">**Pour vous connecter à un ordinateur distant en utilisant votre nom d’utilisateur et votre mot de passe d’ouverture de session**</span><span class="sxs-lookup"><span data-stu-id="c3777-114">**To connect to a remote computer using your logon username and password**</span></span>

1.  <span data-ttu-id="c3777-115">Spécifiez l’ordinateur cible avec un nom de domaine complet ou une adresse IP et affectez-le à une constante.</span><span class="sxs-lookup"><span data-stu-id="c3777-115">Specify the target computer with a fully qualified domain name or an IP address and assign this to a constant.</span></span> <span data-ttu-id="c3777-116">Si une adresse IPv6 est spécifiée, l’adresse doit être placée entre crochets.</span><span class="sxs-lookup"><span data-stu-id="c3777-116">If an IPv6 address is specified, then the address must be enclosed in square brackets.</span></span>

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  <span data-ttu-id="c3777-117">Créez un objet [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="c3777-117">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("WSMan.Automation")
    ```

    

3.  <span data-ttu-id="c3777-118">Créez la session, en spécifiant le transport, HTTP ou HTTPs et en la concaténant avec la constante représentant l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="c3777-118">Create the session, specifying the transport, HTTP or HTTPS, and concatenating it with the constant representing the target computer.</span></span>

    ```VB
    
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

<span data-ttu-id="c3777-119">L’exemple de code VBScript suivant montre le script complet.</span><span class="sxs-lookup"><span data-stu-id="c3777-119">The following VBScript code example shows the complete script.</span></span> <span data-ttu-id="c3777-120">Le script comprend une sous-routine permettant de transformer les données XML brutes au format lisible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c3777-120">The script includes a subroutine to transform the data from raw XML to human-readable form.</span></span> <span data-ttu-id="c3777-121">Pour plus d’informations, consultez [affichage de la sortie XML des scripts WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="c3777-121">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



<span data-ttu-id="c3777-122">**Pour se connecter à un ordinateur distant à l’aide d’un autre compte**</span><span class="sxs-lookup"><span data-stu-id="c3777-122">**To connect to a remote computer using a different account**</span></span>

1.  <span data-ttu-id="c3777-123">Spécifiez l’ordinateur cible avec un nom de domaine complet ou une adresse IP et affectez-le à une constante.</span><span class="sxs-lookup"><span data-stu-id="c3777-123">Specify the target computer with a fully qualified domain name or an IP address and assign this to a constant.</span></span> <span data-ttu-id="c3777-124">Si une adresse IPv6 est spécifiée, l’adresse doit être placée entre crochets.</span><span class="sxs-lookup"><span data-stu-id="c3777-124">If an IPv6 address is specified, then the address must be enclosed in square brackets.</span></span>

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  <span data-ttu-id="c3777-125">Créez un objet [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="c3777-125">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    
    ```

    

3.  <span data-ttu-id="c3777-126">Appelez la méthode [**WSMan. CreateConnectionOptions**](wsman-createconnectionoptions.md) pour créer un objet [**ConnectionOptions**](connectionoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="c3777-126">Call the [**WSMan.CreateConnectionOptions**](wsman-createconnectionoptions.md) method to create a [**ConnectionOptions**](connectionoptions.md) object.</span></span> <span data-ttu-id="c3777-127">Le compte sur l’ordinateur distant doit être membre du groupe administrateurs de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c3777-127">The account on the remote computer must be a member of the local computer administrators group.</span></span>

    ```VB
    Set objConnectionOptions = objWsman.CreateConnectionOptions
    objConnectionOptions.UserName = "Username"
    objConnectionOptions.Password = "Password"
    ```

    

4.  <span data-ttu-id="c3777-128">Sur l’appel [**WSman. CreateSession**](wsman-createsession.md) , spécifiez les indicateurs de connexion de session appropriés dans le paramètre *Flags* .</span><span class="sxs-lookup"><span data-stu-id="c3777-128">On the [**WSman.CreateSession**](wsman-createsession.md) call, specify the appropriate session connection flags in the *flags* parameter.</span></span> <span data-ttu-id="c3777-129">Pour plus d’informations, consultez [sessions, constantes](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c3777-129">For more information, see [Session Constants](session-constants.md).</span></span> <span data-ttu-id="c3777-130">Spécifiez l’ordinateur cible avec un nom d’ordinateur complet ou une adresse IP et le transport (http ou https).</span><span class="sxs-lookup"><span data-stu-id="c3777-130">Specify the target computer with a fully qualified computer name or an IP address and the transport—http or https.</span></span> <span data-ttu-id="c3777-131">Ce script demande l’authentification [*Kerberos*](windows-remote-management-glossary.md) auprès du service WinRM distant.</span><span class="sxs-lookup"><span data-stu-id="c3777-131">This script requests [*Kerberos*](windows-remote-management-glossary.md) authentication from the remote WinRM service.</span></span>

    <span data-ttu-id="c3777-132">Contrairement aux scripts WMI, vous pouvez utiliser plusieurs méthodes d’authentification dans les scripts WinRM.</span><span class="sxs-lookup"><span data-stu-id="c3777-132">Unlike WMI scripts, you can use several methods of authentication in WinRM scripts.</span></span> <span data-ttu-id="c3777-133">Pour plus d’informations, consultez [authentification pour les connexions à distance](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="c3777-133">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

    ```VB
    iFlags = objWsman.SessionFlagUseKerberos Or _
      objWsman.SessionFlagCredUserNamePassword
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
      iFlags, objConnectionOptions)
    ```

    

5.  <span data-ttu-id="c3777-134">Une fois l’objet de session disponible, vous pouvez appeler n’importe quelle méthode d’objet de [**session**](session.md) pour obtenir des données pour une ressource.</span><span class="sxs-lookup"><span data-stu-id="c3777-134">After the session object is available, you can call any of the [**Session**](session.md) object methods to obtain data for a resource.</span></span> <span data-ttu-id="c3777-135">Vous pouvez obtenir des données pour toutes les ressources disponibles sur l’ordinateur sur lequel la session est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c3777-135">You can get data for any resource that is available on the computer on which the session is running.</span></span> <span data-ttu-id="c3777-136">Pour plus d’informations, consultez [obtention de données à partir de l’ordinateur local](obtaining-data-from-the-local-computer.md).</span><span class="sxs-lookup"><span data-stu-id="c3777-136">For more information, see [Obtaining Data from the Local Computer](obtaining-data-from-the-local-computer.md).</span></span>

<span data-ttu-id="c3777-137">L’exemple de code VBScript suivant montre le script complet.</span><span class="sxs-lookup"><span data-stu-id="c3777-137">The following VBScript code example shows the complete script.</span></span> <span data-ttu-id="c3777-138">Le script comprend une sous-routine permettant de transformer les données XML brutes au format lisible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c3777-138">The script includes a subroutine to transform the data from raw XML to human-readable form.</span></span> <span data-ttu-id="c3777-139">Pour plus d’informations, consultez [affichage de la sortie XML des scripts WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="c3777-139">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span> <span data-ttu-id="c3777-140">Le script spécifie l’authentification Kerberos, mais si l’ordinateur distant se trouve dans un groupe de travail et non dans un domaine, la spécification de Kerberos génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="c3777-140">The script specifies Kerberos authentication, but if the remote computer is in a workgroup rather than a domain, specifying Kerberos generates an error.</span></span>


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("Wsman.Automation")
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "Username"
objConnectionOptions.Password = "Password"
iFlags = objWsman.SessionFlagUseKerberos Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
  iFlags, objConnectionOptions)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="c3777-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c3777-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3777-142">À propos de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="c3777-142">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="c3777-143">Utilisation de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="c3777-143">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="c3777-144">Référence Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="c3777-144">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 