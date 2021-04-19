---
description: Le fournisseur Registre système est inscrit dans le cadre du processus d’installation de WMI sur Windows.
ms.assetid: ce5d0785-6e1b-411c-91df-f25767310530
ms.tgt_platform: multiple
title: Inscription du fournisseur de Registre système
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d600872c4efab5560f4fd794cac63beb4365841c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106530848"
---
# <a name="registering-the-system-registry-provider"></a><span data-ttu-id="8a009-103">Inscription du fournisseur de Registre système</span><span class="sxs-lookup"><span data-stu-id="8a009-103">Registering the System Registry Provider</span></span>

<span data-ttu-id="8a009-104">Le fournisseur Registre système est inscrit dans le cadre du processus d’installation de WMI sur Windows.</span><span class="sxs-lookup"><span data-stu-id="8a009-104">The System Registry provider is registered as part of the WMI installation process on Windows.</span></span> <span data-ttu-id="8a009-105">Si vous utilisez une autre plateforme et souhaitez utiliser le fournisseur de Registre système, vous devez d’abord inscrire le fournisseur en suivant les étapes décrites ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="8a009-105">If you are using another platform and want to use the System Registry provider, you must first register the provider yourself following the steps described below.</span></span>

<span data-ttu-id="8a009-106">La procédure suivante décrit comment inscrire le fournisseur de Registre système.</span><span class="sxs-lookup"><span data-stu-id="8a009-106">The following procedure describes how to register the System Registry provider.</span></span>

<span data-ttu-id="8a009-107">**Pour inscrire le fournisseur de Registre système**</span><span class="sxs-lookup"><span data-stu-id="8a009-107">**To register the System Registry provider**</span></span>

1.  <span data-ttu-id="8a009-108">Inscrivez le fournisseur en tant que serveur COM.</span><span class="sxs-lookup"><span data-stu-id="8a009-108">Register the provider as a COM server.</span></span>

    <span data-ttu-id="8a009-109">Si nécessaire, vous devrez peut-être créer des entrées de registre.</span><span class="sxs-lookup"><span data-stu-id="8a009-109">If necessary, you may need to create registry entries.</span></span> <span data-ttu-id="8a009-110">Ce processus s’applique à tous les serveurs COM et n’est pas lié à WMI.</span><span class="sxs-lookup"><span data-stu-id="8a009-110">This process applies to all COM servers and is unrelated to WMI.</span></span> <span data-ttu-id="8a009-111">Pour plus d’informations, consultez la documentation [com](https://msdn.microsoft.com/library/aa139695.aspx) dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8a009-111">For more information, see the [COM](https://msdn.microsoft.com/library/aa139695.aspx) documentation in the Microsoft Windows Software Development Kit (SDK).</span></span>

2.  <span data-ttu-id="8a009-112">Créez une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) pour décrire l’implémentation du fournisseur de Registre système.</span><span class="sxs-lookup"><span data-stu-id="8a009-112">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class to describe the implementation of the System Registry provider.</span></span>

    <span data-ttu-id="8a009-113">L’instance [**\_ \_ Win32Provider**](--win32provider.md) décrit le nom du fournisseur et son identificateur de classe (**CLSID**).</span><span class="sxs-lookup"><span data-stu-id="8a009-113">The [**\_\_Win32Provider**](--win32provider.md) instance describes the name of the provider and its class identifier (**CLSID**).</span></span>

    <span data-ttu-id="8a009-114">L’exemple suivant décrit comment inscrire [**\_ \_ Win32Provider**](--win32provider.md) comme une propriété d’instance, un événement ou un fournisseur de méthode.</span><span class="sxs-lookup"><span data-stu-id="8a009-114">The following example describes how to register [**\_\_Win32Provider**](--win32provider.md) as an instance property, event, or method provider.</span></span>

    ``` syntax
    // Instance provider
    instance of __Win32Provider as $InstProv
    {
        Name    = "RegProv" ;
        ClsId   = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}" ;
    };    
    // Property provider 
    instance of __Win32Provider as $PropProv 
    {
        Name = "RegPropProv"; 
        Clsid = "{72967901-68EC-11d0-B729-00AA0062CBB7}"; 
    }; 
    // Event provider
    instance of __Win32Provider as $RegEvent
    {
        Name = "RegistryEventProvider";
        Clsid = "{fa77a74e-e109-11d0-ad6e-00c04fd8fdff}";
    };
    instance of __Win32Provider as $RegMethod
    {
        Name = "RegistryMethodProvider";
        Clsid = "{44DE513E-60C2-11d3-AF33-00C04F79FEB1}";
    };
    ```

3.  <span data-ttu-id="8a009-115">Créez une ou plusieurs instances de classes dérivées de la classe [**\_ \_ ProviderRegistration**](--providerregistration.md) pour décrire l’implémentation logique du fournisseur de Registre système.</span><span class="sxs-lookup"><span data-stu-id="8a009-115">Create one or more instances of classes derived from the [**\_\_ProviderRegistration**](--providerregistration.md) class to describe the logical implementation of the System Registry provider.</span></span>

    <span data-ttu-id="8a009-116">En fonction de l’objectif pour lequel vous inscrivez le fournisseur de Registre système, vous pouvez créer une ou plusieurs des classes suivantes.</span><span class="sxs-lookup"><span data-stu-id="8a009-116">Depending on the purpose for which you are registering the System Registry provider, you can create one or more of the following classes.</span></span>

    [<span data-ttu-id="8a009-117">**\_\_InstanceProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="8a009-117">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)

    [<span data-ttu-id="8a009-118">**\_\_PropertyProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="8a009-118">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)

    [<span data-ttu-id="8a009-119">**\_\_EventProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="8a009-119">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)

    [<span data-ttu-id="8a009-120">**\_\_MethodProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="8a009-120">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)

    <span data-ttu-id="8a009-121">L’exemple de code MOF suivant décrit comment vous pouvez inscrire le fournisseur de Registre système en tant que fournisseur d’instance, de propriété, d’événement ou de méthode.</span><span class="sxs-lookup"><span data-stu-id="8a009-121">The following MOF code example describes how you can register the System Registry provider as an instance, property, event, or method provider.</span></span>

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $InstProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
        SupportsDelete = FALSE;
        SupportsEnumeration = TRUE;
    };
    instance of __PropertyProviderRegistration
    {
        Provider = $PropProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
    }; 
    instance of __EventProviderRegistration
    {
        Provider = $RegEvent;
        EventQueryList = {
                "select * from RegistryKeyChangeEvent",
                "select * from RegistryValueChangeEvent",
                "select * from RegistryTreeChangeEvent"};
    };
    // Method provider
    instance of __MethodProviderRegistration
    {
        Provider = $RegMethod;
    };
    ```

4.  <span data-ttu-id="8a009-122">Compilez le fichier MOF à l’aide du compilateur MOF ou de l’interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="8a009-122">Compile the MOF file using the MOF compiler or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

<span data-ttu-id="8a009-123">Le fichier RegEvent. mof fourni dans la section WMI de l’SDK Windows contient les instances [**\_ \_ Win32Provider**](--win32provider.md) et [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) nécessaires à l’inscription du fournisseur de Registre système en tant que fournisseur d’événements.</span><span class="sxs-lookup"><span data-stu-id="8a009-123">The RegEvent.mof file provided in the WMI section of the Windows SDK contains the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventproviderregistration.md) instances necessary to register the System Registry provider as an event provider.</span></span> <span data-ttu-id="8a009-124">Pour plus d’informations sur l’inscription d’un fournisseur, consultez [inscription d’un fournisseur](registering-a-provider.md) et [réception d’un événement WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="8a009-124">For more information about registering a provider, see [Registering a Provider](registering-a-provider.md) and [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

 

 



