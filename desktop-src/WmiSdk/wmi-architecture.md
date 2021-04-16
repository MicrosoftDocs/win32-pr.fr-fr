---
description: WMI fournit une interface uniforme pour les applications ou les scripts locaux ou distants qui obtiennent des données de gestion à partir d’un système informatique, d’un réseau ou d’une entreprise.
ms.assetid: 41ba2a64-3322-48b8-a6ea-e468bfac06e2
ms.tgt_platform: multiple
title: Architecture WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b90ee4f81c2afdfc222dd7d5d824f88bda122b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104550767"
---
# <a name="wmi-architecture"></a><span data-ttu-id="91da7-103">Architecture WMI</span><span class="sxs-lookup"><span data-stu-id="91da7-103">WMI Architecture</span></span>

<span data-ttu-id="91da7-104">WMI fournit une interface uniforme pour les applications ou les scripts locaux ou distants qui obtiennent des données de gestion à partir d’un système informatique, d’un réseau ou d’une entreprise.</span><span class="sxs-lookup"><span data-stu-id="91da7-104">WMI provides a uniform interface for any local or remote applications or scripts that obtain management data from a computer system, a network, or an enterprise.</span></span> <span data-ttu-id="91da7-105">L’interface uniforme est conçue de telle sorte que les applications et les scripts du client WMI n’ont pas besoin d’appeler une grande variété d’interfaces de programmation d’applications (API) du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="91da7-105">The uniform interface is designed such that WMI client applications and scripts do not have to call a wide variety of operating system application programming interfaces (APIs).</span></span> <span data-ttu-id="91da7-106">De nombreuses API ne peuvent pas être appelées par des clients Automation, comme des scripts ou des applications Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="91da7-106">Many APIs cannot be called by automation clients like scripts or Visual Basic applications.</span></span> <span data-ttu-id="91da7-107">Les autres API n’effectuent pas d’appels aux ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="91da7-107">Other APIs do not make calls to remote computers.</span></span>

<span data-ttu-id="91da7-108">Pour obtenir des données à partir de WMI, écrivez un script client ou une application qui accède aux [classes WMI](wmi-classes.md) ou fournissent des données à WMI en écrivant un [*fournisseur WMI*](gloss-p.md).</span><span class="sxs-lookup"><span data-stu-id="91da7-108">To obtain data from WMI, write a client script or application that accesses [WMI Classes](wmi-classes.md) or provide data to WMI by writing a [*WMI provider*](gloss-p.md).</span></span> <span data-ttu-id="91da7-109">Pour plus d’informations, consultez [utilisation de WMI](using-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="91da7-109">For more information, see [Using WMI](using-wmi.md).</span></span>

## <a name="objects-consumers-and-infrastructure-of-wmi"></a><span data-ttu-id="91da7-110">Objets, consommateurs et infrastructure de WMI</span><span class="sxs-lookup"><span data-stu-id="91da7-110">Objects, Consumers, and Infrastructure of WMI</span></span>

<span data-ttu-id="91da7-111">Le diagramme suivant montre la relation entre l’infrastructure WMI et les fournisseurs WMI et les objets gérés, et elle présente également la relation entre l’infrastructure WMI et les consommateurs WMI.</span><span class="sxs-lookup"><span data-stu-id="91da7-111">The following diagram shows the relationship between the WMI infrastructure and the WMI providers and managed objects, and it also shows the relationship between the WMI infrastructure and the WMI consumers.</span></span>

![relation entre l’infrastructure WMI, les fournisseurs WMI et les objets gérés](images/wmi-architecture.png)

## <a name="wmi-components"></a><span data-ttu-id="91da7-113">Composants WMI</span><span class="sxs-lookup"><span data-stu-id="91da7-113">WMI Components</span></span>

<span data-ttu-id="91da7-114">La liste suivante décrit les principaux composants WMI :</span><span class="sxs-lookup"><span data-stu-id="91da7-114">The following list describes the key WMI components:</span></span>

-   <span data-ttu-id="91da7-115">Objets gérés et fournisseurs WMI</span><span class="sxs-lookup"><span data-stu-id="91da7-115">Managed objects and WMI providers</span></span>

    <span data-ttu-id="91da7-116">Un fournisseur WMI est un objet COM qui surveille un ou plusieurs [*objets managés*](gloss-m.md) pour WMI.</span><span class="sxs-lookup"><span data-stu-id="91da7-116">A WMI provider is a COM object that monitors one or more [*managed objects*](gloss-m.md) for WMI.</span></span> <span data-ttu-id="91da7-117">Un objet géré est un composant d’entreprise logique ou physique, tel qu’un lecteur de disque dur, une carte réseau, un système de base de données, un système d’exploitation, un processus ou un service.</span><span class="sxs-lookup"><span data-stu-id="91da7-117">A managed object is a logical or physical enterprise component, such as a hard disk drive, network adapter, database system, operating system, process, or service.</span></span>

    <span data-ttu-id="91da7-118">Semblable à un pilote, un fournisseur fournit WMI avec les données d’un objet géré et gère les messages de WMI à l’objet managé.</span><span class="sxs-lookup"><span data-stu-id="91da7-118">Similar to a driver, a provider supplies WMI with data from a managed object and handles messages from WMI to the managed object.</span></span> <span data-ttu-id="91da7-119">Les fournisseurs WMI se composent d’un fichier DLL et d’un fichier [*format MOF (MOF)*](gloss-m.md) qui définit les classes pour lesquelles le fournisseur retourne des données et effectue des opérations.</span><span class="sxs-lookup"><span data-stu-id="91da7-119">WMI providers consist of a DLL file and a [*Managed Object Format (MOF)*](gloss-m.md) file that defines the classes for which the provider returns data and performs operations.</span></span> <span data-ttu-id="91da7-120">Les fournisseurs, comme les applications WMI C++, utilisent l' [API com pour WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="91da7-120">Providers, like WMI C++ applications, use the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="91da7-121">Pour plus d’informations, consultez [fourniture de données à WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="91da7-121">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

    <span data-ttu-id="91da7-122">Un exemple de fournisseur est le [fournisseur de Registre](/previous-versions/windows/desktop/regprov/system-registry-provider)préinstallé, qui accède aux données dans le registre système.</span><span class="sxs-lookup"><span data-stu-id="91da7-122">An example of a provider is the preinstalled [Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which accesses data in the system registry.</span></span> <span data-ttu-id="91da7-123">Le fournisseur de registre a une [*classe WMI*](gloss-w.md), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), avec de nombreuses méthodes, mais pas de propriétés.</span><span class="sxs-lookup"><span data-stu-id="91da7-123">The Registry provider has one [*WMI class*](gloss-w.md), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), with many methods but no properties.</span></span> <span data-ttu-id="91da7-124">D’autres fournisseurs préinstallés, tels que le [fournisseur Win32](/windows/desktop/CIMWin32Prov/win32-provider), ont généralement des classes avec de nombreuses propriétés, mais peu de méthodes, telles que le [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) ou le [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="91da7-124">Other preinstalled providers, such as the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider), usually have classes with many properties but few methods, such as [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) or [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span> <span data-ttu-id="91da7-125">Le fichier DLL du fournisseur de Registre, Stdprov.dll, contient le code qui retourne dynamiquement les données lorsqu’elles sont demandées par des scripts ou des applications clients.</span><span class="sxs-lookup"><span data-stu-id="91da7-125">The Registry provider DLL file, Stdprov.dll, contains the code that dynamically returns data when requested by client scripts or applications.</span></span>

    <span data-ttu-id="91da7-126">Les fichiers MOF et DLL WMI se trouvent dans% WINDIR \\ % system32 \\ WBEM, avec les [outils de Command-Line WMI](wmi-command-line-tools.md), tels que [**Winmgmt.exe**](winmgmt.md) et [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="91da7-126">WMI MOF and DLL files are located in %WINDIR%\\System32\\Wbem, along with the [WMI Command-Line Tools](wmi-command-line-tools.md), such as [**Winmgmt.exe**](winmgmt.md) and [**Mofcomp.exe**](mofcomp.md).</span></span> <span data-ttu-id="91da7-127">Les classes de fournisseur, telles que [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), sont définies dans les fichiers MOF, puis compilées dans le référentiel WMI au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="91da7-127">Provider classes, such as [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), are defined in MOF files, and then compiled into the WMI repository at system startup.</span></span>

-   [<span data-ttu-id="91da7-128">Infrastructure WMI</span><span class="sxs-lookup"><span data-stu-id="91da7-128">WMI infrastructure</span></span>](wmi-infrastructure.md)

    <span data-ttu-id="91da7-129">L’infrastructure WMI est un composant du système d’exploitation Microsoft Windows qui est connu comme le service WMI (WinMgmt).</span><span class="sxs-lookup"><span data-stu-id="91da7-129">The WMI infrastructure is a Microsoft Windows operating system component know as the WMI service(winmgmt).</span></span> <span data-ttu-id="91da7-130">L’infrastructure WMI a deux composants : le noyau WMI et l' [*espace de stockage WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="91da7-130">The WMI infrastructure has two components: the WMI Core, and the [*WMI repository*](gloss-w.md).</span></span>

    <span data-ttu-id="91da7-131">Le référentiel WMI est organisé par des espaces de [*noms*](gloss-n.md)WMI.</span><span class="sxs-lookup"><span data-stu-id="91da7-131">The WMI repository is organized by WMI [*namespaces*](gloss-n.md).</span></span> <span data-ttu-id="91da7-132">Le service WMI crée des espaces de noms tels que la racine \\ par défaut, le \\ cimv2 racine et l' \\ abonnement racine au démarrage du système, et préinstalle un ensemble par défaut de définitions de classe, y compris les [classes Win32](/windows/desktop/CIMWin32Prov/win32-provider), les [classes système WMI](wmi-system-classes.md)et d’autres.</span><span class="sxs-lookup"><span data-stu-id="91da7-132">The WMI service creates some namespaces such as root\\default, root\\cimv2, and root\\subscription at system startup and preinstalls a default set of class definitions, including the [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider), the [WMI System Classes](wmi-system-classes.md), and others.</span></span> <span data-ttu-id="91da7-133">Les espaces de noms restants trouvés sur votre système sont créés par des fournisseurs pour d’autres parties du système d’exploitation ou des produits.</span><span class="sxs-lookup"><span data-stu-id="91da7-133">The remaining namespaces found on your system are created by providers for other parts of the operating system or products.</span></span> <span data-ttu-id="91da7-134">Pour plus d’informations et pour obtenir la liste des fournisseurs WMI qui se trouvent dans la plupart des versions de système d’exploitation, consultez [fournisseurs WMI](wmi-providers.md).</span><span class="sxs-lookup"><span data-stu-id="91da7-134">For more information and a list of WMI providers found in most operating system versions, see [WMI Providers](wmi-providers.md).</span></span>

    <span data-ttu-id="91da7-135">Le service WMI joue le rôle d’intermédiaire entre les fournisseurs, les applications de gestion et l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="91da7-135">The WMI service acts as an intermediary between the providers, management applications, and the WMI repository.</span></span> <span data-ttu-id="91da7-136">Seules les données statiques relatives aux objets sont stockées dans le référentiel, par exemple les classes définies par les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="91da7-136">Only static data about objects is stored in the repository, such as the classes defined by providers.</span></span> <span data-ttu-id="91da7-137">WMI obtient la plupart des données de manière dynamique à partir du fournisseur lorsqu’un client le demande.</span><span class="sxs-lookup"><span data-stu-id="91da7-137">WMI obtains most data dynamically from the provider when a client requests it.</span></span> <span data-ttu-id="91da7-138">Vous pouvez également configurer des abonnements pour recevoir des notifications d’événements d’un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="91da7-138">You also can set up subscriptions to receive event notifications from a provider.</span></span> <span data-ttu-id="91da7-139">Pour plus d’informations, consultez [surveillance des événements](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="91da7-139">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

-   <span data-ttu-id="91da7-140">Consommateurs WMI</span><span class="sxs-lookup"><span data-stu-id="91da7-140">WMI consumers</span></span>

    <span data-ttu-id="91da7-141">Un consommateur WMI est un script ou une application de gestion qui interagit avec l’infrastructure WMI.</span><span class="sxs-lookup"><span data-stu-id="91da7-141">A WMI consumer is a management application or script that interacts with the WMI infrastructure.</span></span> <span data-ttu-id="91da7-142">Une application de gestion peut interroger, énumérer des données, exécuter des méthodes de fournisseur ou s’abonner à des événements en appelant l' [API com pour WMI](com-api-for-wmi.md) ou l' [API de script pour WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="91da7-142">A management application can query, enumerate data, run provider methods, or subscribe to events by calling either the [COM API for WMI](com-api-for-wmi.md) or the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span> <span data-ttu-id="91da7-143">Les seules données ou actions disponibles pour un objet géré, comme un lecteur de disque ou un service, sont celles fournies par un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="91da7-143">The only data or actions available for a managed object, such as a disk drive or a service, are those that a provider supplies.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91da7-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="91da7-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91da7-145">Utilisation de WMI</span><span class="sxs-lookup"><span data-stu-id="91da7-145">Using WMI</span></span>](using-wmi.md)
</dt> <dt>

[<span data-ttu-id="91da7-146">Fournisseurs WMI</span><span class="sxs-lookup"><span data-stu-id="91da7-146">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="91da7-147">Création d’une application ou d’un script WMI</span><span class="sxs-lookup"><span data-stu-id="91da7-147">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="91da7-148">Tâches WMI pour les scripts et les applications</span><span class="sxs-lookup"><span data-stu-id="91da7-148">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="91da7-149">Fourniture de données à WMI</span><span class="sxs-lookup"><span data-stu-id="91da7-149">Providing Data to WMI</span></span>](providing-data-to-wmi.md)
</dt> <dt>

[<span data-ttu-id="91da7-150">Classes WMI</span><span class="sxs-lookup"><span data-stu-id="91da7-150">WMI Classes</span></span>](wmi-classes.md)
</dt> <dt>

[<span data-ttu-id="91da7-151">Événements d’analyse</span><span class="sxs-lookup"><span data-stu-id="91da7-151">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="91da7-152">Appel d’une méthode</span><span class="sxs-lookup"><span data-stu-id="91da7-152">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
