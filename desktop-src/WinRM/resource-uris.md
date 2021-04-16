---
title: URI de ressource
description: Un URI de ressource est un identificateur pour un type distinct d’opération de gestion ou de valeur utilisée par les services de gestion qui implémentent le protocole WS-Management.
ms.assetid: 478a6e5d-0675-462e-b2fd-fd2b5379e298
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 665c73caf5cf636ab7f0a0162f488ff073917984
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507930"
---
# <a name="resource-uris"></a><span data-ttu-id="8a1a6-103">URI de ressource</span><span class="sxs-lookup"><span data-stu-id="8a1a6-103">Resource URIs</span></span>

<span data-ttu-id="8a1a6-104">Un [*URI de ressource*](windows-remote-management-glossary.md) est un identificateur pour un type distinct d’opération de gestion ou de valeur utilisée par les services de gestion qui implémentent le protocole WS-Management.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-104">A [*resource URI*](windows-remote-management-glossary.md) is an identifier for a distinct type of management operation or value used by management services that implement the WS-Management protocol.</span></span> <span data-ttu-id="8a1a6-105">Une valeur de gestion peut être la température à l’intérieur d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-105">A management value could be the temperature inside a computer.</span></span> <span data-ttu-id="8a1a6-106">Un exemple d’opération de gestion est le démarrage d’un service arrêté ou la définition d’un quota d’utilisateur de volume de disque.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-106">An example of a management operation is starting a stopped service or setting a disk volume user quota.</span></span>

## <a name="resource-uri-format"></a><span data-ttu-id="8a1a6-107">Format URI de ressource</span><span class="sxs-lookup"><span data-stu-id="8a1a6-107">Resource URI Format</span></span>

<span data-ttu-id="8a1a6-108">Un URI se compose d’un préfixe et d’un chemin d’accès à une ressource, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="8a1a6-108">A URI consists of a prefix and a path to a resource as is shown in the following example:</span></span>

<span data-ttu-id="8a1a6-109">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"</span><span class="sxs-lookup"><span data-stu-id="8a1a6-109">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"</span></span>

<span data-ttu-id="8a1a6-110">Cette spécification de schéma indique que l’URI est basé sur la version 1 du protocole WS-Management officiel et que la ressource est [**un \_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) dans l' \\ espace de noms « root cimv2 » de l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-110">This schema specification indicates that the URI is based on version 1 of the official WS-Management protocol and that the resource is a [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) in the "root\\cimv2" namespace of the WMI repository.</span></span> <span data-ttu-id="8a1a6-111">Les préfixes d’URI contiennent une spécification de schéma, telle que « schemas.microsoft.com/wbem/wsman/1/wmi » et un type spécifique de ressource, tel que **\_ disque logique Win32**.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-111">URI prefixes contain a schema specification, such as "schemas.microsoft.com/wbem/wsman/1/wmi" and a specific type of resource, such as **Win32\_LogicalDisk**.</span></span> <span data-ttu-id="8a1a6-112">Pour plus d’informations sur l’identification d’une instance spécifique d’une classe WMI, consultez [Windows Remote Management et WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="8a1a6-112">For more information about identifying a specific instance of a WMI class, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="8a1a6-113">Pour plus d’informations, consultez [préfixes d’URI](uri-prefixes.md).</span><span class="sxs-lookup"><span data-stu-id="8a1a6-113">For more information, see [URI Prefixes](uri-prefixes.md).</span></span>

## <a name="types-of-resource-uris"></a><span data-ttu-id="8a1a6-114">Types d’URI de ressource</span><span class="sxs-lookup"><span data-stu-id="8a1a6-114">Types of Resource URIs</span></span>

<span data-ttu-id="8a1a6-115">Bien que [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md) soit la principale source de données de gestion pour les systèmes d’exploitation Windows, d’autres sources de schéma de gestion existent également.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-115">While [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md) is the primary source of management data for Windows-based operating systems, other sources of management schema also exist.</span></span>

<span data-ttu-id="8a1a6-116">La liste suivante décrit plusieurs types d’URI de ressource utilisés par Windows Remote Management :</span><span class="sxs-lookup"><span data-stu-id="8a1a6-116">The following list describes several types of resource URIs used by Windows Remote Management:</span></span>

-   <span data-ttu-id="8a1a6-117">URI WMI</span><span class="sxs-lookup"><span data-stu-id="8a1a6-117">WMI URIs</span></span>

    <span data-ttu-id="8a1a6-118">Ce groupe d’URI représente un [*Common Information Model*](/windows/desktop/WmiSdk/gloss-c) chemin de classe qui comprend l’espace de noms et la classe.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-118">This group of URIs represent a [*Common Information Model*](/windows/desktop/WmiSdk/gloss-c) class path which includes namespace and class.</span></span>

    <span data-ttu-id="8a1a6-119">Les URI WMI peuvent être utilisés dans :</span><span class="sxs-lookup"><span data-stu-id="8a1a6-119">WMI URIs can be used in:</span></span>

    -   <span data-ttu-id="8a1a6-120">Méthodes de [**session**](session.md)</span><span class="sxs-lookup"><span data-stu-id="8a1a6-120">[**Session**](session.md) methods</span></span>
    -   <span data-ttu-id="8a1a6-121">Méthodes [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span><span class="sxs-lookup"><span data-stu-id="8a1a6-121">[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) methods</span></span>
    -   <span data-ttu-id="8a1a6-122">Méthodes [**WSMan. CreateResourceLocator**](wsman-createresourcelocator.md) ou [**IWSMan. CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator)</span><span class="sxs-lookup"><span data-stu-id="8a1a6-122">[**WSMan.CreateResourceLocator**](wsman-createresourcelocator.md) or [**IWSMan.CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator) methods</span></span>
    -   <span data-ttu-id="8a1a6-123">Méthodes [**ResourceLocator**](resourcelocator.md) ou [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span><span class="sxs-lookup"><span data-stu-id="8a1a6-123">[**ResourceLocator**](resourcelocator.md) or [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) methods</span></span>

-   <span data-ttu-id="8a1a6-124">URI IPMI</span><span class="sxs-lookup"><span data-stu-id="8a1a6-124">IPMI URIs</span></span>

    <span data-ttu-id="8a1a6-125">Ce groupe d’URI représente des URI standard basés sur la version 2,9 de CIM.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-125">This group of URIs represent industry standard URIs based upon CIM version 2.9.</span></span> <span data-ttu-id="8a1a6-126">Les URI IPMI peuvent être utilisés dans les méthodes de [**session**](session.md) [**, d'**](session-put.md) [**extraction**](session-get.md), d' [**énumération**](session-enumerate.md) et d' [**appel**](session-invoke.md).</span><span class="sxs-lookup"><span data-stu-id="8a1a6-126">IPMI URIs can be used in [**Session**](session.md) methods [**Get**](session-get.md), [**Put**](session-put.md), [**Enumerate**](session-enumerate.md) , and [**Invoke**](session-invoke.md).</span></span>

    <span data-ttu-id="8a1a6-127">par exemple https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-127">An example is https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd.</span></span> <span data-ttu-id="8a1a6-128">Cette ressource est définie selon le schéma CIM [DMTF.org](https://www.dmtf.org/home) .</span><span class="sxs-lookup"><span data-stu-id="8a1a6-128">This resource is defined according to the [DMTF.org](https://www.dmtf.org/home) CIM schema.</span></span>

-   <span data-ttu-id="8a1a6-129">URI de configuration WinRM</span><span class="sxs-lookup"><span data-stu-id="8a1a6-129">WinRM configuration URIs</span></span>

    <span data-ttu-id="8a1a6-130">Ce groupe d’URI sont des opérations de configuration pour la configuration de l'[*écouteur*](windows-remote-management-glossary.md) WinRM.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-130">This group of URIs are configuration operations for the WinRM [*listener*](windows-remote-management-glossary.md) configuration.</span></span>

    <span data-ttu-id="8a1a6-131"> https://schemas.microsoft.com/wbem/wsman/1/config/listenerpeut être utilisé dans [](session.md) les méthodes de session [**, d'**](session-put.md) [**extraction**](session-get.md), de [**création**](session-create.md), de [**suppression**](session-delete.md)et d' [**énumération**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="8a1a6-131">https://schemas.microsoft.com/wbem/wsman/1/config/listener can be used in [**Session**](session.md) methods [**Get**](session-get.md), [**Put**](session-put.md), [**Create**](session-create.md), [**Delete**](session-delete.md), and [**Enumerate**](session-enumerate.md).</span></span>

-   <span data-ttu-id="8a1a6-132">URI du [*Journal des événements système*](windows-remote-management-glossary.md) (sel)</span><span class="sxs-lookup"><span data-stu-id="8a1a6-132">[*System Event Log*](windows-remote-management-glossary.md) (SEL) URIs</span></span>

    <span data-ttu-id="8a1a6-133">Ce groupe d’URI s’abonne aux événements du collecteur d’événements à partir du BMC.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-133">This group of URIs subscribes to Event Collector events from the BMC.</span></span> <span data-ttu-id="8a1a6-134">Vous pouvez vous abonner à ces événements à l’aide de l’outil en ligne de commande **wevtutil** .</span><span class="sxs-lookup"><span data-stu-id="8a1a6-134">You can subscribe to these events using the **Wevtutil** command-line tool.</span></span> <span data-ttu-id="8a1a6-135">Pour plus d’informations, consultez https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-135">For more information, see https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.</span></span>

## <a name="case-sensitivity"></a><span data-ttu-id="8a1a6-136">Respect de la casse</span><span class="sxs-lookup"><span data-stu-id="8a1a6-136">Case Sensitivity</span></span>

<span data-ttu-id="8a1a6-137">Le [*plug-in WMI*](windows-remote-management-glossary.md) conserve la casse de l’URI de ressource reçu dans une demande.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-137">The [*WMI plug-in*](windows-remote-management-glossary.md) preserves the case of the resource URI received in a request.</span></span> <span data-ttu-id="8a1a6-138">Toutefois, pour garantir l’interopérabilité avec d’autres implémentations de WS-Management protocole, utilisez la casse correcte pour la ressource demandée dans URI de ressource.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-138">However, to ensure interoperability with other implementations of WS-Management protocol, use the correct case for the requested resource in resource URI.</span></span> <span data-ttu-id="8a1a6-139">La casse correcte est l’orthographe définie par le fournisseur de ressources.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-139">The correct case is the spelling defined by the resource provider.</span></span>

<span data-ttu-id="8a1a6-140">Si les URI de ressource ne nécessitent pas de respect de la casse, le XML de [*fragments*](windows-remote-management-glossary.md) ne le fait pas.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-140">While resource URIs do not require case-sensitivity, [*fragment*](windows-remote-management-glossary.md) XML does.</span></span> <span data-ttu-id="8a1a6-141">Un fragment spécifie une seule propriété, plutôt que l’ensemble des propriétés d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-141">A fragment specifies just one property, rather than the entire set of properties for a resource.</span></span> <span data-ttu-id="8a1a6-142">Dans le cas des ressources WMI, la syntaxe de fragment obtient une propriété à partir d’une instance de ressource.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-142">In the case of WMI resources, fragment syntax gets one property from a resource instance.</span></span> <span data-ttu-id="8a1a6-143">Par exemple, l’obtention de la propriété de **version** de [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) requiert l’utilisation d’un fragment.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-143">For example, getting only the **Version** property from [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) requires using a fragment.</span></span> <span data-ttu-id="8a1a6-144">Pour plus d’informations sur les fragments, consultez « Ajout d’un sélecteur à un objet ResourceLocator ou IWSManResourceLocator » dans [Windows Remote Management et WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="8a1a6-144">For more information about fragments, see "Adding a selector to a ResourceLocator or IWSManResourceLocator object" in [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="8a1a6-145">Conformément aux normes XML et [*XPath*](windows-remote-management-glossary.md) , le [*plug-in WMI*](windows-remote-management-glossary.md) applique le respect de la casse pour les fragments et le XML qui définit les paramètres d’entrée d’une méthode.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-145">Following XML and [*XPath*](windows-remote-management-glossary.md) standards, the [*WMI plug-in*](windows-remote-management-glossary.md) enforces case-sensitivity for fragments and XML that defines the input parameters for a method.</span></span> <span data-ttu-id="8a1a6-146">Le respect de la casse est requis pour prendre en charge la norme XPath 1.0/niveau 1.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-146">Case-sensitivity is required to support the XPath 1.0/Level 1 standard.</span></span> <span data-ttu-id="8a1a6-147">Pour recevoir des données WMI via WinRM, le respect de la casse signifie que les noms des classes, propriétés et méthodes WMI doivent correspondre à la casse du nom trouvé dans le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-147">To get WMI data through WinRM, case-sensitivity means that the names of WMI classes, properties, and methods must match the case of the name found in the WMI repository.</span></span>

<span data-ttu-id="8a1a6-148">Pour plus d’informations, consultez [syntaxe XPath](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="8a1a6-148">For more information, see [XPath Syntax](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).</span></span>

## <a name="case-sensitivity-examples"></a><span data-ttu-id="8a1a6-149">Exemples de respect de la casse</span><span class="sxs-lookup"><span data-stu-id="8a1a6-149">Case Sensitivity Examples</span></span>

<span data-ttu-id="8a1a6-150">Par exemple, un script qui obtient la propriété **du \_ descripteur de sécurité** à partir d’une instance de la classe de [**\_ service WMI Win32**](/windows/desktop/CIMWin32Prov/win32-service) ne peut pas utiliser les majuscules pour les noms du chemin d’accès du fragment, mais uniquement l’URI.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-150">For example, a script that obtains the **SECURITY\_DESCRIPTOR** property from an instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class cannot use upper-case for the names in the fragment path, only the URI.</span></span> <span data-ttu-id="8a1a6-151">Le [*plug-in WMI*](windows-remote-management-glossary.md) WinRM retourne une erreur pour l’exemple VBScript suivant, car le XML XPath fourni pour **FragmentPath** n’utilise pas la casse correcte.</span><span class="sxs-lookup"><span data-stu-id="8a1a6-151">The WinRM [*WMI plug-in*](windows-remote-management-glossary.md) returns an error for the following VBScript example because the XPath XML supplied for the **FragmentPath** does not use the correct case.</span></span> <span data-ttu-id="8a1a6-152">Dans le référentiel WMI, la classe est orthographiée « Win32 \_ service ».</span><span class="sxs-lookup"><span data-stu-id="8a1a6-152">In the WMI repository, the class is spelled "Win32\_Service".</span></span>


```VB
RResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_& "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_SERVICE/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



<span data-ttu-id="8a1a6-153">La version suivante du même exemple illustre l’utilisation correcte de case pour la classe [**de \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) et la propriété de **\_ descripteur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="8a1a6-153">The following version of the same example shows the correct use of case for the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class and **SECURITY\_DESCRIPTOR** property.</span></span>


```VB
ResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_Service/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



## <a name="related-topics"></a><span data-ttu-id="8a1a6-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8a1a6-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a1a6-155">À propos de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="8a1a6-155">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="8a1a6-156">Gestion matérielle à distance</span><span class="sxs-lookup"><span data-stu-id="8a1a6-156">Remote Hardware Management</span></span>](remote-hardware-management.md)
</dt> <dt>

[<span data-ttu-id="8a1a6-157">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="8a1a6-157">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 