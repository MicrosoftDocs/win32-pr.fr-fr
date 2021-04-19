---
title: Windows Remote Management et WMI
description: Windows Remote Management peut être utilisé pour récupérer les données exposées par Windows Management Instrumentation.
ms.assetid: a625440b-a839-487d-b862-e35934f24e1f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6942e89ea2e63ef809f3452e6ce55a493662c938
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106539810"
---
# <a name="windows-remote-management-and-wmi"></a><span data-ttu-id="5ff50-103">Windows Remote Management et WMI</span><span class="sxs-lookup"><span data-stu-id="5ff50-103">Windows Remote Management and WMI</span></span>

<span data-ttu-id="5ff50-104">Windows Remote Management peut être utilisé pour récupérer les données exposées par Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page) et [mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)).</span><span class="sxs-lookup"><span data-stu-id="5ff50-104">Windows Remote Management can be used to retrieve data exposed by Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page) and [MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)).</span></span> <span data-ttu-id="5ff50-105">Vous pouvez obtenir des données WMI avec des scripts ou des applications qui utilisent l' [API de script WinRM](winrm-scripting-api.md) ou via l’outil en ligne de commande **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="5ff50-105">You can obtain WMI data with scripts or applications that use the [WinRM Scripting API](winrm-scripting-api.md) or through the **Winrm** command-line tool.</span></span>

<span data-ttu-id="5ff50-106">WinRM prend en charge la plupart des opérations et classes WMI familières, y compris les objets incorporés.</span><span class="sxs-lookup"><span data-stu-id="5ff50-106">WinRM supports most of the familiar WMI classes and operations, including embedded objects.</span></span> <span data-ttu-id="5ff50-107">WinRM peut tirer parti de WMI pour collecter des données sur les [*ressources*](windows-remote-management-glossary.md) ou pour gérer les ressources sur un système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="5ff50-107">WinRM can leverage WMI to collect data about [*resources*](windows-remote-management-glossary.md) or to manage resources on a Windows-based operating system.</span></span> <span data-ttu-id="5ff50-108">Cela signifie que vous pouvez obtenir des données sur des objets tels que des disques, des cartes réseau, des services ou des processus de votre entreprise par le biais de l’ensemble existant de [classes WMI](/windows/desktop/WmiSdk/wmi-classes).</span><span class="sxs-lookup"><span data-stu-id="5ff50-108">That means that you can obtain data about objects such as disks, network adapters, services, or processes in your enterprise through the existing set of [WMI classes](/windows/desktop/WmiSdk/wmi-classes).</span></span> <span data-ttu-id="5ff50-109">Vous pouvez également accéder aux données matérielles disponibles à partir du [fournisseur IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI standard.</span><span class="sxs-lookup"><span data-stu-id="5ff50-109">You can also access the hardware data that is available from the standard WMI [IPMI provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

## <a name="identifying-a-wmi-resource"></a><span data-ttu-id="5ff50-110">Identification d’une ressource WMI</span><span class="sxs-lookup"><span data-stu-id="5ff50-110">Identifying a WMI Resource</span></span>

<span data-ttu-id="5ff50-111">Vous pouvez référencer une classe WMI en tant que [*ressource*](windows-remote-management-glossary.md) dans WinRM et dans le protocole WS-Management : un type d’entité gérée, comme un service ou un disque.</span><span class="sxs-lookup"><span data-stu-id="5ff50-111">You can reference a WMI class as a [*resource*](windows-remote-management-glossary.md) in WinRM and in the WS-Management protocol: a type of managed entity, like a service or a disk.</span></span>

<span data-ttu-id="5ff50-112">Une classe ou une méthode WMI est identifiée par un [*URI*](windows-remote-management-glossary.md), tout comme n’importe quelle autre ressource lorsque vous utilisez le protocole WS-Management.</span><span class="sxs-lookup"><span data-stu-id="5ff50-112">A WMI class or method is identified by a [*URI*](windows-remote-management-glossary.md), just as any other resource is when using the WS-Management protocol.</span></span> <span data-ttu-id="5ff50-113">L’URI peut spécifier une ressource WMI (classe), une action WMI (méthode) ou identifier une instance spécifique d’une classe dans [*les messages*](windows-remote-management-glossary.md) envoyés sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="5ff50-113">The URI can specify a WMI resource (class), a WMI action (method), or identify a specific instance of a class in [*messages*](windows-remote-management-glossary.md) sent over a network.</span></span> <span data-ttu-id="5ff50-114">Pour plus d’informations, consultez [URI de ressource](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="5ff50-114">For more information, see [Resource URIs](resource-uris.md).</span></span>

## <a name="constructing-the-uri-prefix-for-wmi-classes"></a><span data-ttu-id="5ff50-115">Construction du préfixe URI pour les classes WMI</span><span class="sxs-lookup"><span data-stu-id="5ff50-115">Constructing the URI Prefix for WMI Classes</span></span>

<span data-ttu-id="5ff50-116">Le préfixe URI contient une partie fixe et l’espace de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="5ff50-116">The URI prefix contains a fixed part and the WMI namespace.</span></span> <span data-ttu-id="5ff50-117">Par exemple, le préfixe URI dans Windows Server qui contient la partie fixe du préfixe est : `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>` .</span><span class="sxs-lookup"><span data-stu-id="5ff50-117">For example, the URI prefix in Windows Server that contains the fixed part of the prefix is: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>`.</span></span> <span data-ttu-id="5ff50-118">Cela permet de générer le préfixe URI pour n’importe quel espace de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="5ff50-118">This allows the URI prefix to be generated for any WMI namespace.</span></span> <span data-ttu-id="5ff50-119">Par exemple, pour accéder à l’espace de noms WMI **\\ par défaut racine** , utilisez le préfixe URI suivant : `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/` .</span><span class="sxs-lookup"><span data-stu-id="5ff50-119">For example, to access the **root\\default** WMI namespace, use the following URI prefix: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/`.</span></span>

<span data-ttu-id="5ff50-120">La majorité des classes WMI pour la gestion se trouvent dans l’espace de noms **\\ cimv2 racine** .</span><span class="sxs-lookup"><span data-stu-id="5ff50-120">The majority of the WMI classes for management are in the **root\\cimv2** namespace.</span></span> <span data-ttu-id="5ff50-121">Pour accéder aux classes et aux instances dans l’espace de noms **\\ cimv2 racine** , utilisez le préfixe URI : `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` .</span><span class="sxs-lookup"><span data-stu-id="5ff50-121">To access classes and instances in **root\\cimv2** namespace, use the URI prefix: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`.</span></span> <span data-ttu-id="5ff50-122">Pour plus d’informations, consultez [URI de ressource](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="5ff50-122">For more information, see [Resource URIs](resource-uris.md).</span></span>

## <a name="generating-a-complete-uri-for-wmi-classes"></a><span data-ttu-id="5ff50-123">Génération d’un URI complet pour les classes WMI</span><span class="sxs-lookup"><span data-stu-id="5ff50-123">Generating a Complete URI for WMI Classes</span></span>

<span data-ttu-id="5ff50-124">L’URI que vous fournissez, soit à l’outil de ligne de commande **WinRM** , soit à un script, se compose du préfixe et de la spécification de ressource.</span><span class="sxs-lookup"><span data-stu-id="5ff50-124">The URI that you supply, either to the **Winrm** command-line tool or to a script, consists of the prefix plus the resource specification.</span></span>

<span data-ttu-id="5ff50-125">La procédure suivante décrit comment générer un URI de ressource pour obtenir une classe WMI ou pour l’utiliser dans une opération d’énumération.</span><span class="sxs-lookup"><span data-stu-id="5ff50-125">The following procedure describes how to generate a resource URI either to get a WMI class or to use in an enumerate operation.</span></span>

<span data-ttu-id="5ff50-126">**Pour générer un URI de ressource pour une classe WMI**</span><span class="sxs-lookup"><span data-stu-id="5ff50-126">**To generate a resource URI for a WMI class**</span></span>

1.  <span data-ttu-id="5ff50-127">Commencez par le préfixe qui indique que le schéma de protocole WS-Management doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="5ff50-127">Start with the prefix that indicates the WS-Management protocol schema should be used.</span></span>

    https://schemas.microsoft.com/wbem/wsman/1

    <span data-ttu-id="5ff50-128">Le préfixe URI de ressource pour les classes WMI est toujours identique.</span><span class="sxs-lookup"><span data-stu-id="5ff50-128">The resource URI prefix for WMI classes is always the same.</span></span> <span data-ttu-id="5ff50-129">Pour plus d’informations, consultez [préfixes d’URI](uri-prefixes.md).</span><span class="sxs-lookup"><span data-stu-id="5ff50-129">For more information, see [URI Prefixes](uri-prefixes.md).</span></span>

2.  <span data-ttu-id="5ff50-130">Ajoutez l’espace de noms WMI au préfixe.</span><span class="sxs-lookup"><span data-stu-id="5ff50-130">Add the WMI namespace to the prefix.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`

3.  <span data-ttu-id="5ff50-131">Ajoutez le nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="5ff50-131">Add the class name.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service`

4.  <span data-ttu-id="5ff50-132">Pour définir la valeur d’une propriété, ou pour appeler une méthode spécifique, ajoutez la ou les valeurs de clé requises pour la classe.</span><span class="sxs-lookup"><span data-stu-id="5ff50-132">To set the value of a property, or to invoke a specific method, add the required key value or values for the class.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Name=Winmgmt`

    <span data-ttu-id="5ff50-133">Si vous laissez la valeur de clé vide, vous ne modifierez pas la valeur de la propriété d’origine.</span><span class="sxs-lookup"><span data-stu-id="5ff50-133">If you leave the key value blank, you will not alter the original property value.</span></span>

    > [!Note]  
    > <span data-ttu-id="5ff50-134">Si vous laissez la valeur de clé vide, la valeur de la propriété est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="5ff50-134">Leaving the key value blank sets the property value to **NULL**.</span></span>

     

## <a name="locating-a-wmi-resource-with-winrm"></a><span data-ttu-id="5ff50-135">Recherche d’une ressource WMI avec WinRM</span><span class="sxs-lookup"><span data-stu-id="5ff50-135">Locating a WMI Resource with WinRM</span></span>

<span data-ttu-id="5ff50-136">Vous pouvez obtenir des données WMI via l’outil en ligne de commande, **WinRM** ou via un script Visual Basic qui utilise l' [API de script WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5ff50-136">You can obtain WMI data either through the command-line tool, **Winrm**, or through a Visual Basic script that uses the [WinRM Scripting API](winrm-scripting-api.md).</span></span> <span data-ttu-id="5ff50-137">Vous n’utilisez pas de [chemin d’accès WMI](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) pour rechercher une ressource.</span><span class="sxs-lookup"><span data-stu-id="5ff50-137">You do not use a [WMI path](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) to locate a resource.</span></span> <span data-ttu-id="5ff50-138">Au lieu de cela, vous convertissez l’espace de noms WMI et la hiérarchie en un [*URI*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5ff50-138">Instead, you convert the WMI namespace and hierarchy to a [*URI*](windows-remote-management-glossary.md).</span></span>

<span data-ttu-id="5ff50-139">L’URI WinRM pour une classe WMI contient deux parties : le [préfixe URI](uri-prefixes.md) et la classe à laquelle vous souhaitez accéder.</span><span class="sxs-lookup"><span data-stu-id="5ff50-139">The WinRM URI for a WMI class contains two parts: the [URI prefix](uri-prefixes.md) and the class that you want to access.</span></span>

<span data-ttu-id="5ff50-140">Par exemple, l’URI suivant peut être fourni à la méthode [**session. Enumerate**](session-enumerate.md) pour répertorier tous les services sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5ff50-140">For example, the following URI can be supplied to the [**Session.Enumerate**](session-enumerate.md) method to list all the services on a computer.</span></span> <span data-ttu-id="5ff50-141">Le préfixe URI est `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` , et la classe [**est \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="5ff50-141">The URI prefix is `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`, and the class is [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

`strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"`

<span data-ttu-id="5ff50-142">Dans WMI, répertoriez les données de toutes les instances d’une ressource ou d’une classe de plusieurs façons :</span><span class="sxs-lookup"><span data-stu-id="5ff50-142">In WMI, list the data for all of the instances of a resource or class in several ways:</span></span>

-   <span data-ttu-id="5ff50-143">Une requête pour toutes les instances de cette ressource.</span><span class="sxs-lookup"><span data-stu-id="5ff50-143">A query for all the instances of that resource.</span></span>

    `Set colServices = objWMIService.ExecQuery("Select * from Win32_Service")`

-   <span data-ttu-id="5ff50-144">Un appel à [**SWbemServices. InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) ou [**SWbemObject. instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span><span class="sxs-lookup"><span data-stu-id="5ff50-144">A call to [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) or [**SWbemObject.Instances\_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span></span>

    `Set colServices = InstancesOf("Win32_Service")`

<span data-ttu-id="5ff50-145">Dans WinRM, il existe une méthode pour répertorier toutes les instances d’une ressource : [**session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="5ff50-145">In WinRM, there is one way to list all of the instances of a resource: [**Session.Enumerate**](session-enumerate.md).</span></span>


```VB
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
Set colServices = objSession.Enumerate( strResource )
```



## <a name="locating-a-specific-instance-of-a-wmi-resource"></a><span data-ttu-id="5ff50-146">Recherche d’une instance spécifique d’une ressource WMI</span><span class="sxs-lookup"><span data-stu-id="5ff50-146">Locating a Specific Instance of a WMI Resource</span></span>

<span data-ttu-id="5ff50-147">Dans WMI, vous pouvez désigner une instance particulière d’une classe en spécifiant des valeurs pour les propriétés de clé ou en interrogeant une instance qui correspond à une liste de valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="5ff50-147">In WMI, you can designate a particular instance of a class either by specifying values for the key properties or by querying for an instance that matches a list of property values.</span></span> <span data-ttu-id="5ff50-148">Les propriétés de clé ont le [**qualificateur de clé**](/windows/desktop/WmiSdk/key-qualifier)WMI.</span><span class="sxs-lookup"><span data-stu-id="5ff50-148">Key properties have the WMI [**Key qualifier**](/windows/desktop/WmiSdk/key-qualifier).</span></span>

<span data-ttu-id="5ff50-149">Vous pouvez obtenir une instance spécifique d’une classe de plusieurs façons :</span><span class="sxs-lookup"><span data-stu-id="5ff50-149">You can obtain a specific instance of a class in several ways:</span></span>

-   <span data-ttu-id="5ff50-150">Un appel à [**session. Enumerate**](session-enumerate.md) avec les paramètres de *filtre* et de *dialecte* pour créer une requête.</span><span class="sxs-lookup"><span data-stu-id="5ff50-150">A call to [**Session.Enumerate**](session-enumerate.md) with the *filter* and *dialect* parameters to create a query.</span></span>

    ```VB
    RemoteComputer = "servername.domain.com"
    strDialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

    strFilter = "SELECT * FROM Win32_Share WHERE Name='Admin$'"
    Set objResultSet = objSession.Enumerate(strResource, strFilter, strDialect)
    ```

    

-   <span data-ttu-id="5ff50-151">Un appel à [**SWbemServices. obtenir**](/windows/desktop/WmiSdk/swbemservices-get).</span><span class="sxs-lookup"><span data-stu-id="5ff50-151">A call to [**SWbemServices.Get**](/windows/desktop/WmiSdk/swbemservices-get).</span></span> <span data-ttu-id="5ff50-152">Pour [**session. obtenir**](session-get.md), vous devez fournir une ou plusieurs valeurs de clés spécifiques, précédées d’un point d’interrogation ( ?).</span><span class="sxs-lookup"><span data-stu-id="5ff50-152">For [**Session.Get**](session-get.md), you must supply one or more specific key values, preceded by a question mark (?).</span></span>

    <span data-ttu-id="5ff50-153">Le format de l’URI pour une instance spécifique est `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value` .</span><span class="sxs-lookup"><span data-stu-id="5ff50-153">The format of the URI for a specific instance is `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

    <span data-ttu-id="5ff50-154">Une classe WMI peut avoir plusieurs clés.</span><span class="sxs-lookup"><span data-stu-id="5ff50-154">A WMI class may have more than one key.</span></span> <span data-ttu-id="5ff50-155">Les paires nom-valeur de clé sont séparées par un signe « + ».</span><span class="sxs-lookup"><span data-stu-id="5ff50-155">Key name-value pairs are separated by a "+" sign.</span></span> <span data-ttu-id="5ff50-156">Dans ce cas, le format est : `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2` .</span><span class="sxs-lookup"><span data-stu-id="5ff50-156">In that case, the format is: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2`.</span></span>

    <span data-ttu-id="5ff50-157">La syntaxe WinRM pour obtenir un objet WMI Singleton est différente de WMI.</span><span class="sxs-lookup"><span data-stu-id="5ff50-157">The WinRM syntax to obtain a singleton WMI object is different from WMI.</span></span> <span data-ttu-id="5ff50-158">Un singleton est une classe WMI définie de sorte qu’une seule instance est autorisée.</span><span class="sxs-lookup"><span data-stu-id="5ff50-158">A singleton is a WMI class defined so that only one instance is allowed.</span></span> <span data-ttu-id="5ff50-159">[**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) ou [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) sont des exemples de classe singleton WMI.</span><span class="sxs-lookup"><span data-stu-id="5ff50-159">[**Win32\_CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) or [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) are examples of a WMI singleton class.</span></span>

    <span data-ttu-id="5ff50-160">La syntaxe WMI pour les singletons est présentée dans l’exemple de code VBScript suivant.</span><span class="sxs-lookup"><span data-stu-id="5ff50-160">The WMI syntax for singletons is shown in the following VBScript code example.</span></span>

    ```VB
    Set TimeObject = objWMIService.Get("Win32_CurrentTime=@")
    ```

    

    <span data-ttu-id="5ff50-161">L’exemple suivant illustre la syntaxe du singleton WinRM qui n’utilise pas « @ ».</span><span class="sxs-lookup"><span data-stu-id="5ff50-161">The following example shows the WinRM singleton syntax which does not use "@".</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"
    ```

    

-   <span data-ttu-id="5ff50-162">Ajout d’un [*Sélecteur*](windows-remote-management-glossary.md) à un objet [**ResourceLocator**](resourcelocator.md) ou [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) .</span><span class="sxs-lookup"><span data-stu-id="5ff50-162">Adding a [*selector*](windows-remote-management-glossary.md) to a [**ResourceLocator**](resourcelocator.md) or [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) object.</span></span>

    <span data-ttu-id="5ff50-163">L’exemple de code VBScript suivant montre comment utiliser un sélecteur pour obtenir une instance spécifique du [**\_ processeur Win32**](/windows/desktop/CIMWin32Prov/win32-processor).</span><span class="sxs-lookup"><span data-stu-id="5ff50-163">The following VBScript code example shows how to use a selector to get a specific instance of [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor).</span></span>

    ```VB
    strUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Processor"
    Set objWsman = CreateObject("Wsman.Automation")
    Set Session = objWsman.CreateSession
    Set Locator = objWsman.CreateResourceLocator(strUri)
    Locator.AddSelector "DeviceID", "CPU0"
    ```

    

## <a name="related-topics"></a><span data-ttu-id="5ff50-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ff50-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ff50-165">À propos de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="5ff50-165">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="5ff50-166">Préfixes d’URI</span><span class="sxs-lookup"><span data-stu-id="5ff50-166">URI Prefixes</span></span>](uri-prefixes.md)
</dt> <dt>

[<span data-ttu-id="5ff50-167">URI de ressource</span><span class="sxs-lookup"><span data-stu-id="5ff50-167">Resource URIs</span></span>](resource-uris.md)
</dt> <dt>

[<span data-ttu-id="5ff50-168">Scripts dans Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="5ff50-168">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>
