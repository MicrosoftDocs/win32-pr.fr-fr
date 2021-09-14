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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923375"
---
# <a name="registering-an-event-provider"></a>Inscription d’un fournisseur d’événements

Pour créer un [*fournisseur d’événements*](gloss-e.md) WMI, vous devez inscrire l’instance [**\_ \_ Win32Provider**](--win32provider.md) qui représente votre fournisseur à l’aide d’une instance de [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md). En tant qu’objet COM, votre fournisseur doit s’inscrire auprès du système d’exploitation et de WMI. La procédure suivante suppose que vous avez déjà implémenté le processus d’inscription, comme décrit dans [inscription d’un fournisseur](registering-a-provider.md).

La procédure suivante décrit comment inscrire un fournisseur d’événements.

**Pour inscrire un fournisseur d’événements**

1.  Créez une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) qui décrit le fournisseur.
2.  Créez une instance de la classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) qui décrit l’ensemble des fonctionnalités du fournisseur.

    La classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) hérite de nombreuses propriétés de la classe parente [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) . Les propriétés locales de la classe **\_ \_ EventProviderRegistration** sont le chemin d’accès de l’objet au fournisseur et une liste de requêtes qui décrivent les événements pris en charge par le fournisseur. Pour plus d’informations, consultez [interrogation de WMI](querying-wmi.md).

3.  Chargez votre implémentation des classes [**\_ \_ Win32Provider**](--win32provider.md) et [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) dans l’espace de stockage WMI.

    WMI utilise votre définition de classe pour inscrire votre fournisseur d’événements et y accéder. Pour plus d’informations, consultez [inscription d’un fournisseur](registering-a-provider.md).

L’exemple de code suivant décrit une implémentation d’une classe [**\_ \_ Win32Provider**](--win32provider.md) et d’une classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) .

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

La première requête indique que le fournisseur génère toutes les notifications d’événements pour la classe d’événements extrinsèque FaxEvent. Comme elle utilise l’opérateur ISA, la deuxième requête implique que le fournisseur génère des notifications pour tous les événements de création d’instance pour la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) et toutes ses sous-classes.

Lorsqu’un fournisseur s’inscrit pour fournir un événement intrinsèque, l’événement doit s’appliquer à toutes les instances d’une classe. En d’autres termes, il n’est pas possible d’écrire une requête pour fournir des événements de création d’instance uniquement pour certains des lecteurs de disque appartenant à la classe disque [**\_ logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .

 

 
