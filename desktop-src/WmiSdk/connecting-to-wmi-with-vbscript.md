---
description: Les scripts WMI peuvent condenser la plupart des étapes requises dans un programme C++.
ms.assetid: 77168079-7253-4DB1-8252-7016F5A58DBA
ms.tgt_platform: multiple
title: Connexion à WMI avec VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6952c42a024ebedd10d9ec8ced0bc4946d808c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866897"
---
# <a name="connecting-to-wmi-with-vbscript"></a><span data-ttu-id="99e14-103">Connexion à WMI avec VBScript</span><span class="sxs-lookup"><span data-stu-id="99e14-103">Connecting to WMI with VBScript</span></span>

<span data-ttu-id="99e14-104">Les scripts WMI peuvent condenser la plupart des étapes requises dans un programme C++.</span><span class="sxs-lookup"><span data-stu-id="99e14-104">WMI scripts can condense many of the steps required in a C++ program.</span></span> <span data-ttu-id="99e14-105">Ils peuvent se connecter à WMI, non seulement via un objet [**SWbemLocator**](swbemlocator.md) , mais également par le moniker « winmgmts : ».</span><span class="sxs-lookup"><span data-stu-id="99e14-105">They can connect to WMI, not only through an [**SWbemLocator**](swbemlocator.md) object, but also through the moniker "winmgmts:".</span></span> <span data-ttu-id="99e14-106">Un moniker est un nom abrégé qui localise un espace de noms, une classe ou une instance dans WMI.</span><span class="sxs-lookup"><span data-stu-id="99e14-106">A moniker is a short name that locates a namespace, class, or instance in WMI.</span></span> <span data-ttu-id="99e14-107">Le nom « winmgmts : » est le moniker WMI qui indique à Windows Script Host d’utiliser les objets WMI, se connecte à l’espace de noms par défaut et obtient un objet [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="99e14-107">The name "winmgmts:" is the WMI moniker that tells the Windows Script Host to use the WMI objects, connects to the default namespace, and obtains an [**SWbemServices**](swbemservices.md) object.</span></span> <span data-ttu-id="99e14-108">D’autres informations de connexion, telles qu’un niveau d’emprunt d’identité ou une classe ou une instance spécifique, apparaissent dans la chaîne qui suit le nom du moniker.</span><span class="sxs-lookup"><span data-stu-id="99e14-108">Other connection information, such as an impersonation level or a specific class or instance, appears in the string following the moniker name.</span></span> <span data-ttu-id="99e14-109">Vous pouvez utiliser des monikers dans les appels qui créent ou obtiennent des objets WMI.</span><span class="sxs-lookup"><span data-stu-id="99e14-109">You can use monikers in calls that either create or get WMI objects.</span></span> <span data-ttu-id="99e14-110">Pour plus d’informations, consultez [construction d’une chaîne de moniker](constructing-a-moniker-string.md).</span><span class="sxs-lookup"><span data-stu-id="99e14-110">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md).</span></span>

<span data-ttu-id="99e14-111">La procédure suivante décrit comment se connecter à WMI à l’aide de **SWbemLocator**.</span><span class="sxs-lookup"><span data-stu-id="99e14-111">The following procedure describes how to connect to WMI using **SWbemLocator**.</span></span>

<span data-ttu-id="99e14-112">**Pour se connecter à WMI à l’aide de SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="99e14-112">**To connect to WMI using SWbemLocator**</span></span>

1.  <span data-ttu-id="99e14-113">Récupérez un objet localisateur avec un appel à [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="99e14-113">Retrieve a locator object with a call to [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span>

    ```VB
    Set Locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

2.  <span data-ttu-id="99e14-114">Connectez-vous à l’espace de noms à l’aide d’un appel à la méthode [**ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="99e14-114">Log on to the namespace using a call to the [**ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    ```

    

    <span data-ttu-id="99e14-115">Si vous ne spécifiez pas d’ordinateur dans l’appel à [**ConnectServer**](swbemlocator-connectserver.md), WMI se connecte à l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="99e14-115">If you do not specify a computer in the call to [**ConnectServer**](swbemlocator-connectserver.md), then WMI connects to the local computer.</span></span> <span data-ttu-id="99e14-116">Si vous ne spécifiez pas d’espace de noms, WMI se connecte à l’espace de noms spécifié dans la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="99e14-116">If you do not specify a namespace, then WMI connects to the namespace specified in the registry key.</span></span>

    <span data-ttu-id="99e14-117">**HKEY \_ Logiciel de l' \_ ordinateur local** espace de \\  \\  \\  \\  \\ **noms par défaut** de script WBEM Microsoft</span><span class="sxs-lookup"><span data-stu-id="99e14-117">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Namespace**</span></span>

    <span data-ttu-id="99e14-118">L’espace de noms par défaut est le \\ \\ cimv2 racine.</span><span class="sxs-lookup"><span data-stu-id="99e14-118">The default namespace is \\root\\cimv2.</span></span> <span data-ttu-id="99e14-119">Pour plus d’informations sur les espaces de noms, consultez [création de hiérarchies dans WMI](creating-hierarchies-within-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="99e14-119">For more information about namespaces, see [Creating Hierarchies Within WMI](creating-hierarchies-within-wmi.md).</span></span>

3.  <span data-ttu-id="99e14-120">Définissez le niveau d’emprunt d’identité avec un appel à la méthode [**SWbemServices \_ . Security**](swbemservices-security-.md) .</span><span class="sxs-lookup"><span data-stu-id="99e14-120">Set the impersonation level with a call to the [**SWbemServices.Security\_**](swbemservices-security-.md) method.</span></span>

    ```VB
    objService.Security_.ImpersonationLevel = 3 
    ```

    

    <span data-ttu-id="99e14-121">Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="99e14-121">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

4.  <span data-ttu-id="99e14-122">Implémentez l’objectif de votre script.</span><span class="sxs-lookup"><span data-stu-id="99e14-122">Implement the purpose of your script.</span></span>

    <span data-ttu-id="99e14-123">WMI expose un ensemble d’objets de script qui utilisent pour accéder et manipuler des données sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="99e14-123">WMI exposes a variety of scripting objects that use to access and manipulate data across your network.</span></span> <span data-ttu-id="99e14-124">Pour plus d’informations, consultez [manipulation d’informations de classes et d’instances](manipulating-class-and-instance-information.md) et [API de script pour WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="99e14-124">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    objService.Security_.ImpersonationLevel = 3
    Set Jobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
    i=0
    For each Job in Jobs
        i = i+1   
        WScript.Echo Job.JobId & "  " & Job.Command & VBNewLine
    Next
    If i = 0 Then
        WScript.Echo "No Jobs Scheduled with the AT command were found"
    End If
    ```

    

<span data-ttu-id="99e14-125">La procédure suivante décrit comment se connecter à WMI et récupérer un objet à l’aide d’un moniker.</span><span class="sxs-lookup"><span data-stu-id="99e14-125">The following procedure describes how to connect to WMI and retrieve an object using a moniker.</span></span>

<span data-ttu-id="99e14-126">**Pour se connecter à WMI et récupérer un objet à l’aide d’un moniker**</span><span class="sxs-lookup"><span data-stu-id="99e14-126">**To connect to WMI and retrieve an object using a moniker**</span></span>

1.  <span data-ttu-id="99e14-127">Appelez [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) avec un moniker dans le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="99e14-127">Call [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) with a moniker in the input parameter.</span></span>

    ```VB
    'the simple version
    Set MyObject = GetObject("winMgmts::Win32_scheduledJob")

    'Or the more complex version
    strComputer = "."
    Set MyObject = GetObject("winMgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2:Win32_ScheduledJob")
    ```

    

    <span data-ttu-id="99e14-128">Le moiniker contient un certain nombre d’éléments que vous pouvez utiliser pour vous connecter à WMI :</span><span class="sxs-lookup"><span data-stu-id="99e14-128">The moiniker contains a number of elements that you can use to connect to WMI:</span></span>

    -   <span data-ttu-id="99e14-129">« Winmgmts : » indique à WSH d’utiliser les objets de l' [API de script](scripting-api-objects.md).</span><span class="sxs-lookup"><span data-stu-id="99e14-129">The "winmgmts:" tells WSH to use [Scripting API objects](scripting-api-objects.md).</span></span> <span data-ttu-id="99e14-130">Dans cet exemple, WSH sait qu’il doit retourner un SWbemObject qui décrit le premier \_ ScheduledJob Win32 sur le système.</span><span class="sxs-lookup"><span data-stu-id="99e14-130">In this particular example, the WSH will know that it should return an SWbemObject that describes the first Win32\_scheduledJob on the system.</span></span> <span data-ttu-id="99e14-131">Les autres objets possibles à retourner sont un objet SWbemCollection ou [**SWbemServices**](swbemservices.md) , en fonction de ce que le moniker a décrit.</span><span class="sxs-lookup"><span data-stu-id="99e14-131">Other possible objects to return would be an SWbemCollection or an [**SWbemServices**](swbemservices.md) object, depending on what the moniker described.</span></span>

    -   <span data-ttu-id="99e14-132">Vous pouvez éventuellement définir les niveaux de sécurité pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="99e14-132">You can optionally set the security levels for the connection.</span></span> <span data-ttu-id="99e14-133">Notez cependant que vous ne pouvez pas définir les informations de nom et de mot de passe dans un moniker.</span><span class="sxs-lookup"><span data-stu-id="99e14-133">Note that you cannot set name and password information in a moniker, however.</span></span> <span data-ttu-id="99e14-134">Pour plus d’informations, consultez [sécurisation des scripts pour les clients](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="99e14-134">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

    -   <span data-ttu-id="99e14-135">Vous pouvez éventuellement définir le chemin d’accès à l’objet WMI.</span><span class="sxs-lookup"><span data-stu-id="99e14-135">You can optionally define the path to the WMI object.</span></span> <span data-ttu-id="99e14-136">Cela comprend l’ordinateur local ou distant, l’espace de noms, ainsi que le nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="99e14-136">This includes either the local or remote computer, the namespace, as well as the name of the class.</span></span> <span data-ttu-id="99e14-137">Pour plus d’informations sur l’utilisation de la [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) VBScript dans les scripts WMI, consultez [création d’une instance](creating-an-instance.md) et [récupération d’une instance WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="99e14-137">For more information about using the VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) in WMI scripts, see [Creating an Instance](creating-an-instance.md) and [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="99e14-138">Au lieu de récupérer un seul élément ou une seule collection, vous pouvez également choisir de récupérer l’objet [**SWbemServices**](swbemservices.md) (comme décrit dans l’exemple précédent).</span><span class="sxs-lookup"><span data-stu-id="99e14-138">Instead of retrieving a single item or collection, you can also choose to retrieve the [**SWbemServices**](swbemservices.md) object (as described in the previous example).</span></span> <span data-ttu-id="99e14-139">Ensuite, vous pouvez ensuite appeler des requêtes supplémentaires sur l’objet retourné.</span><span class="sxs-lookup"><span data-stu-id="99e14-139">Afterwards, you can then call additional queries on the returned object.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
    For Each objJob in colScheduledJobs
        Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
    Next
    ```

    

    <span data-ttu-id="99e14-140">Dans l’exemple précédent, Impersonate, ou impersonationLevel = 3, est le niveau de sécurité de processus par défaut.</span><span class="sxs-lookup"><span data-stu-id="99e14-140">In the previous example, impersonate, or impersonationLevel=3, is the default process security level.</span></span> <span data-ttu-id="99e14-141">Dans l’exemple suivant, il n’est pas nécessaire de spécifier ce niveau de sécurité de processus, sauf si vous devez modifier la sécurité du processus en **délégué**.</span><span class="sxs-lookup"><span data-stu-id="99e14-141">In the following example, it is not necessary to specify this process security level unless you need to change the process security to **delegate**.</span></span> <span data-ttu-id="99e14-142">Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="99e14-142">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="99e14-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="99e14-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99e14-144">Scripts dans WMI</span><span class="sxs-lookup"><span data-stu-id="99e14-144">Scripting in WMI</span></span>](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
