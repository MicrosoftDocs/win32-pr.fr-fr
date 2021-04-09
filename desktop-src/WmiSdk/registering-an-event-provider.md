---
description: Pour créer un fournisseur d’événements WMI, vous devez inscrire l' \_ \_ instance Win32Provider qui représente votre fournisseur à l’aide d’une instance de \_ \_ EventProviderRegistration.
ms.assetid: 81f2ba3b-a1cb-42f5-b1a7-b1ca65963902
ms.tgt_platform: multiple
title: Inscription d’un fournisseur d’événements
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2a4aa77c5c5936639435844179f259080085e02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115802"
---
# <a name="registering-an-event-provider"></a><span data-ttu-id="9622e-103">Inscription d’un fournisseur d’événements</span><span class="sxs-lookup"><span data-stu-id="9622e-103">Registering an Event Provider</span></span>

<span data-ttu-id="9622e-104">Pour créer un [*fournisseur d’événements*](gloss-e.md) WMI, vous devez inscrire l’instance [**\_ \_ Win32Provider**](--win32provider.md) qui représente votre fournisseur à l’aide d’une instance de [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="9622e-104">To create a WMI [*event provider*](gloss-e.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_EventProviderRegistration**](--eventproviderregistration.md).</span></span> <span data-ttu-id="9622e-105">En tant qu’objet COM, votre fournisseur doit s’inscrire auprès du système d’exploitation et de WMI.</span><span class="sxs-lookup"><span data-stu-id="9622e-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="9622e-106">La procédure suivante suppose que vous avez déjà implémenté le processus d’inscription, comme décrit dans [inscription d’un fournisseur](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9622e-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="9622e-107">La procédure suivante décrit comment inscrire un fournisseur d’événements.</span><span class="sxs-lookup"><span data-stu-id="9622e-107">The following procedure describes how to register an event provider.</span></span>

<span data-ttu-id="9622e-108">**Pour inscrire un fournisseur d’événements**</span><span class="sxs-lookup"><span data-stu-id="9622e-108">**To register an event provider**</span></span>

1.  <span data-ttu-id="9622e-109">Créez une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) qui décrit le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9622e-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="9622e-110">Créez une instance de la classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) qui décrit l’ensemble des fonctionnalités du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9622e-110">Create an instance of the [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="9622e-111">La classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) hérite de nombreuses propriétés de la classe parente [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="9622e-111">The [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class.</span></span> <span data-ttu-id="9622e-112">Les propriétés locales de la classe **\_ \_ EventProviderRegistration** sont le chemin d’accès de l’objet au fournisseur et une liste de requêtes qui décrivent les événements pris en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9622e-112">The properties local to the **\_\_EventProviderRegistration** class are the object path to the provider and a list of queries that describe the events that the provider supports.</span></span> <span data-ttu-id="9622e-113">Pour plus d’informations, consultez [interrogation de WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="9622e-113">For more information, see [Querying WMI](querying-wmi.md).</span></span>

3.  <span data-ttu-id="9622e-114">Chargez votre implémentation des classes [**\_ \_ Win32Provider**](--win32provider.md) et [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) dans l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="9622e-114">Load your implementation of the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventproviderregistration.md) classes into the WMI repository.</span></span>

    <span data-ttu-id="9622e-115">WMI utilise votre définition de classe pour inscrire votre fournisseur d’événements et y accéder.</span><span class="sxs-lookup"><span data-stu-id="9622e-115">WMI uses your class definition to register and access your event provider.</span></span> <span data-ttu-id="9622e-116">Pour plus d’informations, consultez [inscription d’un fournisseur](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9622e-116">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="9622e-117">L’exemple de code suivant décrit une implémentation d’une classe [**\_ \_ Win32Provider**](--win32provider.md) et d’une classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="9622e-117">The following code example describes an implementation of a [**\_\_Win32Provider**](--win32provider.md) class and a [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class.</span></span>

``` syntax
instance of __Win32Provider as $P
{
    ClientLoadableCLSID = NULL;
    CLSID = "{AA7828C5-95F9-11d2-BB0D-00C042424242}";
    DefaultMachineName = NULL;
    ImpersonationLevel = 0;
    InitializationReentrancy = 0;
    InitializeAsAdminFirst = FALSE;
    Name = "FaxEventProvider";
    PerLocaleInitialization = FALSE;
    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};

instance of __EventProviderRegistration
{  
Provider = $P;
EventQueryList = {
         "SELECT * FROM FaxEvent",
         "SELECT * FROM __InstanceCreationEvent WHERE TargetInstance ISA \"Win32_LogicalDisk\""};
};
```

<span data-ttu-id="9622e-118">La première requête indique que le fournisseur génère toutes les notifications d’événements pour la classe d’événements extrinsèque FaxEvent.</span><span class="sxs-lookup"><span data-stu-id="9622e-118">The first query indicates that the provider generates all event notifications for the extrinsic event class FaxEvent.</span></span> <span data-ttu-id="9622e-119">Comme elle utilise l’opérateur ISA, la deuxième requête implique que le fournisseur génère des notifications pour tous les événements de création d’instance pour la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) et toutes ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="9622e-119">Because it uses the ISA operator, the second query implies that the provider generates notifications for all instance creation events for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and all of its subclasses.</span></span>

<span data-ttu-id="9622e-120">Lorsqu’un fournisseur s’inscrit pour fournir un événement intrinsèque, l’événement doit s’appliquer à toutes les instances d’une classe.</span><span class="sxs-lookup"><span data-stu-id="9622e-120">When a provider registers to provide an intrinsic event, the event must apply to all instances of a class.</span></span> <span data-ttu-id="9622e-121">En d’autres termes, il n’est pas possible d’écrire une requête pour fournir des événements de création d’instance uniquement pour certains des lecteurs de disque appartenant à la classe disque [**\_ logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="9622e-121">In other words, a query cannot be written to provide instance creation events for only some of the disk drives that belong to the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

 

 
