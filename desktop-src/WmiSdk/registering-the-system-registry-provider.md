---
description: Le fournisseur de Registre système est inscrit dans le cadre du processus d’installation de WMI sur Windows.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923368"
---
# <a name="registering-the-system-registry-provider"></a>Inscription du fournisseur de Registre système

Le fournisseur de Registre système est inscrit dans le cadre du processus d’installation de WMI sur Windows. Si vous utilisez une autre plateforme et souhaitez utiliser le fournisseur de Registre système, vous devez d’abord inscrire le fournisseur en suivant les étapes décrites ci-dessous.

La procédure suivante décrit comment inscrire le fournisseur de Registre système.

**Pour inscrire le fournisseur de Registre système**

1.  Inscrivez le fournisseur en tant que serveur COM.

    Si nécessaire, vous devrez peut-être créer des entrées de registre. Ce processus s’applique à tous les serveurs COM et n’est pas lié à WMI. pour plus d’informations, consultez la documentation [COM](https://msdn.microsoft.com/library/aa139695.aspx) dans le kit de développement logiciel (SDK) de Microsoft Windows.

2.  Créez une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) pour décrire l’implémentation du fournisseur de Registre système.

    L’instance [**\_ \_ Win32Provider**](--win32provider.md) décrit le nom du fournisseur et son identificateur de classe (**CLSID**).

    L’exemple suivant décrit comment inscrire [**\_ \_ Win32Provider**](--win32provider.md) comme une propriété d’instance, un événement ou un fournisseur de méthode.

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

3.  Créez une ou plusieurs instances de classes dérivées de la classe [**\_ \_ ProviderRegistration**](--providerregistration.md) pour décrire l’implémentation logique du fournisseur de Registre système.

    En fonction de l’objectif pour lequel vous inscrivez le fournisseur de Registre système, vous pouvez créer une ou plusieurs des classes suivantes.

    [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md)

    [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md)

    [**\_\_EventProviderRegistration**](--eventproviderregistration.md)

    [**\_\_MethodProviderRegistration**](--methodproviderregistration.md)

    L’exemple de code MOF suivant décrit comment vous pouvez inscrire le fournisseur de Registre système en tant que fournisseur d’instance, de propriété, d’événement ou de méthode.

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

4.  Compilez le fichier MOF à l’aide du compilateur MOF ou de l’interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

le fichier RegEvent. mof fourni dans la section WMI de l’SDK Windows contient les instances [**\_ \_ Win32Provider**](--win32provider.md) et [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) nécessaires à l’inscription du fournisseur de registre système en tant que fournisseur d’événements. Pour plus d’informations sur l’inscription d’un fournisseur, consultez [inscription d’un fournisseur](registering-a-provider.md) et [réception d’un événement WMI](receiving-a-wmi-event.md).

 

 



