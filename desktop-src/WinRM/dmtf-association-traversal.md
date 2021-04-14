---
title: Découverte de profil DMTF par traversée d’association
description: Un composant clé de l’infrastructure Windows Management Instrumentation (WMI) est un modèle orienté objet des entités gérables dans un système.
ms.assetid: 21e03d78-bce1-471e-a826-e676d32990ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776b3f5883075ddf549330c422efec558195c8fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383075"
---
# <a name="dmtf-profile-discovery-through-association-traversal"></a><span data-ttu-id="faf27-103">Découverte de profil DMTF par traversée d’association</span><span class="sxs-lookup"><span data-stu-id="faf27-103">DMTF Profile Discovery Through Association Traversal</span></span>

<span data-ttu-id="faf27-104">Un composant clé de l’infrastructure Windows Management Instrumentation (WMI) est un modèle orienté objet des entités gérables dans un système.</span><span class="sxs-lookup"><span data-stu-id="faf27-104">A key component of the Windows Management Instrumentation (WMI) infrastructure is an object-oriented model of the manageable entities in a system.</span></span> <span data-ttu-id="faf27-105">Le modèle est conforme à un standard géré par la[DMTF](https://www.dmtf.org/standards/wsman)(Desktop Management Task Force) et est connu comme le Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="faf27-105">The model conforms to a standard maintained by the Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) and is known as the Common Information Model (CIM).</span></span> <span data-ttu-id="faf27-106">Certaines classes du modèle, telles que le [ \_ fichier de fichier CIM](../cimwin32prov/cim-datafile.md) ou le [ \_ processus Win32](../cimwin32prov/win32-process.md), correspondent directement aux entités gérables.</span><span class="sxs-lookup"><span data-stu-id="faf27-106">Some classes in the model, such as [CIM\_DataFile](../cimwin32prov/cim-datafile.md) or [Win32\_Process](../cimwin32prov/win32-process.md), correspond directly to manageable entities.</span></span> <span data-ttu-id="faf27-107">D’autres classes du modèle, telles que [Win32 \_ SystemServices](../cimwin32prov/win32-systemservices.md), représentent les relations entre les entités gérables.</span><span class="sxs-lookup"><span data-stu-id="faf27-107">Other classes in the model, such as [Win32\_SystemServices](../cimwin32prov/win32-systemservices.md), represent relationships between manageable entities.</span></span> <span data-ttu-id="faf27-108">Ces classes de modélisation des relations sont appelées des classes d’association.</span><span class="sxs-lookup"><span data-stu-id="faf27-108">These relationship-modeling classes are known as Association classes.</span></span>

<span data-ttu-id="faf27-109">À l’aide du langage de requête spécifique à WMI, WQL, vous pouvez récupérer des instances de classes qui représentent des entités gérables ou des instances de classes d’association.</span><span class="sxs-lookup"><span data-stu-id="faf27-109">Using the WMI-specific query language, WQL, you can retrieve instances of classes that represent manageable entities or instances of Association classes.</span></span> <span data-ttu-id="faf27-110">Toutefois, WQL est spécifique à l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="faf27-110">But WQL is implementation specific.</span></span> <span data-ttu-id="faf27-111">Il fonctionne uniquement avec l’implémentation Windows de la norme DMTF (WMI).</span><span class="sxs-lookup"><span data-stu-id="faf27-111">It works only with the Windows implementation of the DMTF standard (WMI).</span></span> <span data-ttu-id="faf27-112">En outre, la syntaxe WQL pour la récupération des classes d’association est plutôt compliquée.</span><span class="sxs-lookup"><span data-stu-id="faf27-112">In addition, the WQL syntax for retrieving Association classes is rather complicated.</span></span>

<span data-ttu-id="faf27-113">L’infrastructure Windows Remote Management (WinRM) offre un excellent moyen de tirer parti des fonctionnalités de WMI.</span><span class="sxs-lookup"><span data-stu-id="faf27-113">The Windows Remote Management (WinRM) infrastructure provides an excellent way to leverage the functionality of WMI.</span></span> <span data-ttu-id="faf27-114">Les premières versions de WinRM devaient utiliser WQL pour extraire des instances de classes d’association.</span><span class="sxs-lookup"><span data-stu-id="faf27-114">Early versions of WinRM had to use WQL to retrieve instances of Association classes.</span></span> <span data-ttu-id="faf27-115">WinRM 2,0 intègre une nouvelle fonctionnalité appelée détection de profil DMTF par traversée d’association.</span><span class="sxs-lookup"><span data-stu-id="faf27-115">WinRM 2.0 includes a new feature known as DMTF profile discovery through association traversal.</span></span> <span data-ttu-id="faf27-116">La traversée d’association permet à un utilisateur de WinRM de récupérer des instances de classes d’association à l’aide d’un mécanisme de filtrage standard, le dialecte AssociationFilter, défini dans la spécification de liaison CIM DMTF.</span><span class="sxs-lookup"><span data-stu-id="faf27-116">Association traversal enables a user of WinRM to retrieve instances of Association classes by using a standard filtering mechanism, the AssociationFilter dialect, defined in the DMTF CIM binding specification.</span></span> <span data-ttu-id="faf27-117">Pour plus d’informations sur le parcours d’association, consultez la spécification de liaison CIM WS-Management ( [https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man) ).</span><span class="sxs-lookup"><span data-stu-id="faf27-117">For more information on association traversal, see the WS-Management CIM Binding specification ([https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man)).</span></span>

<span data-ttu-id="faf27-118">L’utilitaire WinRM fournit un mécanisme simple pour parcourir l’Association appropriée et récupérer un profil d’appareil.</span><span class="sxs-lookup"><span data-stu-id="faf27-118">The winrm utility provides a simple mechanism to traverse through the appropriate association and retrieve a device profile.</span></span>

## <a name="configuration-implementation-details"></a><span data-ttu-id="faf27-119">Détails de l’implémentation de la configuration</span><span class="sxs-lookup"><span data-stu-id="faf27-119">Configuration Implementation Details</span></span>

<span data-ttu-id="faf27-120">L’utilitaire WinRM prend désormais en charge un dialecte pour la demande d’association.</span><span class="sxs-lookup"><span data-stu-id="faf27-120">The winrm utility now supports a dialect for the association request.</span></span> <span data-ttu-id="faf27-121">L’URI ou l’alias peut être spécifié à l’aide de l’utilitaire WinRM.</span><span class="sxs-lookup"><span data-stu-id="faf27-121">Either the URI or the alias can be specified using the winrm utility.</span></span>



| <span data-ttu-id="faf27-122">Alias</span><span class="sxs-lookup"><span data-stu-id="faf27-122">Alias</span></span>       | <span data-ttu-id="faf27-123">URI</span><span class="sxs-lookup"><span data-stu-id="faf27-123">URI</span></span>                                                               |
|-------------|-------------------------------------------------------------------|
| <span data-ttu-id="faf27-124">association</span><span class="sxs-lookup"><span data-stu-id="faf27-124">association</span></span> | https://www.dmtf.org/sites/default/files/standards/documents/DSP0227_1.0.0.pdf |



 

## <a name="retrieving-instances-of-an-association-class-by-using-the-associationfilter-dialect"></a><span data-ttu-id="faf27-125">Récupération des instances d’une classe d’association à l’aide du dialecte AssociationFilter</span><span class="sxs-lookup"><span data-stu-id="faf27-125">Retrieving Instances of an Association Class by Using the AssociationFilter Dialect</span></span>

<span data-ttu-id="faf27-126">L’utilitaire WinRM peut récupérer les instances de classe d’association WMI d’une instance source particulière.</span><span class="sxs-lookup"><span data-stu-id="faf27-126">The winrm utility can retrieve WMI association class instances of a particular source instance.</span></span> <span data-ttu-id="faf27-127">La commande suivante montre comment utiliser l’utilitaire WinRM pour récupérer des instances de classes d’association de [ \_ service Win32](../cimwin32prov/win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="faf27-127">The following command demonstrates how to use the winrm utility to retrieve instances of [Win32\_Service](../cimwin32prov/win32-service.md) association classes.</span></span> <span data-ttu-id="faf27-128">Le commutateur « -associations » doit être utilisé pour retourner des classes d’association.</span><span class="sxs-lookup"><span data-stu-id="faf27-128">The switch "-associations" must be used to return association classes.</span></span>

<span data-ttu-id="faf27-129">**WinRM Enumerate wmicimv2/ \* -Dialect : Association-associations-filtre : {Object = Win32 \_ Service ? Name = WinRM ; resultclassname = Win32 \_ dependentservice ; Role = dependent}**</span><span class="sxs-lookup"><span data-stu-id="faf27-129">**winrm enumerate wmicimv2/\* -dialect:association -associations -filter:{object=win32\_service?name=winrm;resultclassname=win32\_dependentservice;role=dependent}**</span></span>

<span data-ttu-id="faf27-130">L’extrait de code textuel suivant est la sortie de la commande ci-dessus :</span><span class="sxs-lookup"><span data-stu-id="faf27-130">The following text-based snippet is the output of the above command:</span></span>

``` syntax
Win32_DependentService
    Antecedent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = RpcSs
    Dependent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = WinRM
    TypeOfDependency = null

Win32_DependentService
    Antecedent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_SystemDriver
            SelectorSet
                Selector: Name = HTTP
    Dependent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = WinRM
    TypeOfDependency = null
```

## <a name="retrieving-instances-of-an-associated-class-by-using-the-associationfilter-dialect"></a><span data-ttu-id="faf27-131">Récupération des instances d’une classe associée à l’aide du dialecte AssociationFilter</span><span class="sxs-lookup"><span data-stu-id="faf27-131">Retrieving Instances of an Associated Class by Using the AssociationFilter Dialect</span></span>

<span data-ttu-id="faf27-132">L’utilitaire WinRM peut récupérer les instances de classe WMI associées à une instance source particulière.</span><span class="sxs-lookup"><span data-stu-id="faf27-132">The winrm utility can retrieve WMI class instances that are associated with a particular source instance.</span></span> <span data-ttu-id="faf27-133">La commande suivante montre comment utiliser l’utilitaire WinRM pour récupérer les instances des classes associées au [ \_ service Win32](../cimwin32prov/win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="faf27-133">The following command demonstrates how to use the winrm utility to retrieve instances of [Win32\_Service](../cimwin32prov/win32-service.md) associated classes.</span></span>

<span data-ttu-id="faf27-134">**WinRM Enumerate wmicimv2/ \* -Dialect : Association-filtre : {Object = Win32 \_ Service ? Name = WinRM ; associationclassname = Win32 \_ dependentservice ; resultclassname = Win32 \_ service ; ResultRole = Antecedent ; Role = dependent}**</span><span class="sxs-lookup"><span data-stu-id="faf27-134">**winrm enumerate wmicimv2/\* -dialect:association -filter:{object=win32\_service?name=winrm;associationclassname=win32\_dependentservice;resultclassname=win32\_service;resultrole=antecedent;role=dependent}**</span></span>

<span data-ttu-id="faf27-135">L’extrait de code textuel suivant est la sortie de la commande ci-dessus :</span><span class="sxs-lookup"><span data-stu-id="faf27-135">The following text-based snippet is the output of the above command:</span></span>

``` syntax
Win32_Service
    AcceptPause = false
    AcceptStop = false
    Caption = Remote Procedure Call (RPC)
    CheckPoint = 0
    CreationClassName = Win32_Service
    Description = The RPCSS service is the Service Control Manager for COM and DCOM servers. It performs object activations requests, object exporter resolutions and distributed garbage collection for COM and DCOM servers. If this service is stopped or disabled, programs using COM or DCOM will not function properly. It is strongly recommended that you have the RPCSS service running DesktopInteract = false
    DisplayName = Remote Procedure Call (RPC)
    ErrorControl = Normal
    ExitCode = 0
    InstallDate = null
    Name = RpcSs
    PathName = C:\Windows\system32\svchost.exe -k rpcss
    ProcessId = 716
    ServiceSpecificExitCode = 0
    ServiceType = Share Process
    Started = true
    StartMode = Auto
    StartName = NT AUTHORITY\NetworkService
    State = Running
    Status = OK
    SystemCreationClassName = Win32_ComputerSystem
    SystemName = myComputer
    TagId = 0
    WaitHint = 0
```

 

 