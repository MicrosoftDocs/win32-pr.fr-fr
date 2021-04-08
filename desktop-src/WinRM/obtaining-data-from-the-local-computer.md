---
title: Obtention de données à partir de l’ordinateur local
description: Bien que Windows Remote Management et WS-Management protocole soient explicitement conçus pour la communication à distance, l’établissement d’une session sur l’ordinateur local est le cas le plus simple.
ms.assetid: 7f08b557-bbd4-4f67-b5e5-b84e8af58657
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ccb71fd176bf3faf425ea57d06beb27788f41a62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727405"
---
# <a name="obtaining-data-from-the-local-computer"></a><span data-ttu-id="30685-103">Obtention de données à partir de l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="30685-103">Obtaining Data from the Local Computer</span></span>

<span data-ttu-id="30685-104">Bien que Windows Remote Management et WS-Management protocole soient explicitement conçus pour la communication à distance, l’établissement d’une session sur l’ordinateur local est le cas le plus simple.</span><span class="sxs-lookup"><span data-stu-id="30685-104">Although Windows Remote Management and WS-Management protocol are explicitly designed for remote communication, establishing a session on the local computer is the simplest case.</span></span> <span data-ttu-id="30685-105">Certains scripts peuvent nécessiter des données d’accès sur l’ordinateur local, ainsi que sur des ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="30685-105">Some scripts may require access data on the local computer as well as remote computers.</span></span>

<span data-ttu-id="30685-106">**WinRM version 2,0 :  **</span><span class="sxs-lookup"><span data-stu-id="30685-106">**WinRM version 2.0:  **</span></span>

<span data-ttu-id="30685-107">Toutes les opérations sont considérées comme distantes et le service WinRM doit être démarré avant l’exécution d’une opération.</span><span class="sxs-lookup"><span data-stu-id="30685-107">All operations are considered remote and the WinRM service must be started before any operation is performed.</span></span> <span data-ttu-id="30685-108">Si une destination distante n’est pas spécifiée, l’hôte local est utilisé par défaut, et toutes les opérations sont envoyées au service WinRM local.</span><span class="sxs-lookup"><span data-stu-id="30685-108">If a remote destination is not specified, then the localhost is used by default, and all operations will be sent to the local WinRM service.</span></span> <span data-ttu-id="30685-109">Pour plus d’informations sur le démarrage du service WinRM, consultez [installation et configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="30685-109">For more information about starting the WinRM service, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<span data-ttu-id="30685-110">Lors de l’utilisation du service WinRM pour les opérations locales, les facteurs suivants doivent être pris en compte :</span><span class="sxs-lookup"><span data-stu-id="30685-110">When using the WinRM service for local operations, the following factors should be considered:</span></span>

-   <span data-ttu-id="30685-111">La configuration WinRM locale ne peut être lue que par les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="30685-111">The local WinRM configuration can only be read by administrators.</span></span>
-   <span data-ttu-id="30685-112">Les autorisations Remote Enable doivent être définies pour les espaces de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="30685-112">WMI namespaces must have remote enable permissions set.</span></span> <span data-ttu-id="30685-113">Pour plus d’informations, consultez [sécurisation d’une connexion WMI à distance](../wmisdk/securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="30685-113">For more information, see [Securing a Remote WMI Connection](../wmisdk/securing-a-remote-wmi-connection.md).</span></span>
-   <span data-ttu-id="30685-114">Si aucun [*écouteur*](windows-remote-management-glossary.md) WinRM n’est créé, le service WinRM écoute les demandes locales sur le port 47001.</span><span class="sxs-lookup"><span data-stu-id="30685-114">If a WinRM [*listener*](windows-remote-management-glossary.md) is not created, then the WinRM service listens for local requests on port 47001.</span></span>

<span data-ttu-id="30685-115">Chaque script WinRM doit commencer par l’établissement d’une session ou d’une connexion à un ordinateur en créant un objet de [**session**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="30685-115">Every WinRM script must start by establishing a session or connection to a computer by creating a [**Session**](session.md) object.</span></span> <span data-ttu-id="30685-116">Une fois la session créée, vous pouvez utiliser les méthodes d’objet de **session** , telles que [**session. Enumerate**](session-enumerate.md) ou [**session. Invoke**](session-invoke.md) pour obtenir des données ou exécuter des méthodes.</span><span class="sxs-lookup"><span data-stu-id="30685-116">After the session is created, you can use the **Session** object methods, such as [**Session.Enumerate**](session-enumerate.md) or [**Session.Invoke**](session-invoke.md) to obtain data or to execute methods.</span></span>

<span data-ttu-id="30685-117">La création d’une session est quelque peu similaire à la [connexion](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) à un espace de noms Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page)).</span><span class="sxs-lookup"><span data-stu-id="30685-117">The creation of a session is somewhat similar to [connecting](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) to a Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page)) namespace.</span></span> <span data-ttu-id="30685-118">La session est essentiellement une couche qui vous permet d’envoyer et de recevoir des données par le biais de messages [*SOAP*](windows-remote-management-glossary.md) et du protocole WS-Management.</span><span class="sxs-lookup"><span data-stu-id="30685-118">The session is essentially a layer that allows you to send and receive data through [*SOAP*](windows-remote-management-glossary.md) messages and the WS-Management protocol.</span></span> <span data-ttu-id="30685-119">Pour plus d’informations, consultez [protocole WS-Management](ws-management-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="30685-119">For more information, see [WS-Management Protocol](ws-management-protocol.md).</span></span>

<span data-ttu-id="30685-120">L’appel de la méthode [**WSMan. CreateSession**](wsman-createsession.md) pour créer un objet de [**session**](session.md) démarre une [*session*](windows-remote-management-glossary.md) qui se connecte au WinRM local.</span><span class="sxs-lookup"><span data-stu-id="30685-120">Calling the [**WSMan.CreateSession**](wsman-createsession.md) method to create a [**Session**](session.md) object will start a [*session*](windows-remote-management-glossary.md) that connects to the local WinRM.</span></span>

<span data-ttu-id="30685-121">**Pour créer une session WSMan et obtenir des données**</span><span class="sxs-lookup"><span data-stu-id="30685-121">**To Create a WSMan Session and Obtain Data**</span></span>

1.  <span data-ttu-id="30685-122">Créez un objet [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="30685-122">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  <span data-ttu-id="30685-123">Créez une session en appelant la méthode [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="30685-123">Create a session by calling the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="30685-124">Cette session s’exécute sous votre nom d’utilisateur et votre mot de passe d’ouverture de session et peut obtenir des données via le WinRM local.</span><span class="sxs-lookup"><span data-stu-id="30685-124">This session runs under your logon username and password and can obtain data through the local WinRM.</span></span>

    ```VB
    Set objSession = objWsman.CreateSession()
    ```

    

3.  <span data-ttu-id="30685-125">Créez un [*URI*](windows-remote-management-glossary.md) de ressource pour identifier la [*ressource*](windows-remote-management-glossary.md) que vous souhaitez gérer ou pour laquelle vous souhaitez obtenir des données.</span><span class="sxs-lookup"><span data-stu-id="30685-125">Create a resource [*URI*](windows-remote-management-glossary.md) to identify the [*resource*](windows-remote-management-glossary.md) you want to manage or for which you want to obtain data.</span></span> <span data-ttu-id="30685-126">Pour plus d’informations sur la mise en forme d’un URI, consultez [URI de ressource](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="30685-126">For more information about formatting a URI, see [Resource URIs](resource-uris.md).</span></span> <span data-ttu-id="30685-127">Cet URI de ressource est destiné à une instance spécifique de la classe de [**\_ service WMI Win32**](/windows/desktop/CIMWin32Prov/win32-service) , le service WinMgmt.</span><span class="sxs-lookup"><span data-stu-id="30685-127">This resource URI is for a specific instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class, the Winmgmt service.</span></span> <span data-ttu-id="30685-128">Pour plus d’informations, consultez [Windows Remote Management et WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="30685-128">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
    ```

    

4.  <span data-ttu-id="30685-129">Appeler des méthodes de [**session**](session.md) qui obtiennent ou énumèrent des données à l’aide de l’URI de ressource.</span><span class="sxs-lookup"><span data-stu-id="30685-129">Call [**Session**](session.md) methods that get or enumerate data using the resource URI.</span></span> <span data-ttu-id="30685-130">Pour plus d’informations, consultez [API de script WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="30685-130">For more information, see [WinRM Scripting API](winrm-scripting-api.md).</span></span>

    ```VB
    strResponse = objSession.Get(strResource)
    Wscript.Echo strResponse
    ```

    

5.  <span data-ttu-id="30685-131">Pour obtenir ou gérer des données à partir d’un autre ordinateur ou utiliser différentes méthodes d’authentification, consultez [obtention de données à partir d’un ordinateur distant](obtaining-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="30685-131">To get or manage data from another computer or use different methods of authentication, see [Obtaining Data from a Remote Computer](obtaining-data-from-a-remote-computer.md).</span></span>

<span data-ttu-id="30685-132">L’exemple de code VBScript suivant montre le script complet qui obtient l’instance spécifique du service WMI [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service) nommé « winmgmt ».</span><span class="sxs-lookup"><span data-stu-id="30685-132">The following VBScript code example shows the complete script that obtains the specific instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) named "Winmgmt".</span></span>


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Wscript.Echo strResponse
```



<span data-ttu-id="30685-133">L’exemple de code VBScript suivant montre le script complet avec la transformation de données.</span><span class="sxs-lookup"><span data-stu-id="30685-133">The following VBScript code example shows the complete script with the data transform.</span></span> <span data-ttu-id="30685-134">Pour plus d’informations, consultez [affichage de la sortie XML des scripts WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="30685-134">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Set xmlFile = CreateObject("MSXml.DOMDocument")
Set xslFile = CreateObject("MSXml.DOMDocument")
xmlFile.LoadXml(strResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)

```



## <a name="related-topics"></a><span data-ttu-id="30685-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="30685-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30685-136">À propos de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="30685-136">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="30685-137">Utilisation de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="30685-137">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="30685-138">Référence Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="30685-138">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 