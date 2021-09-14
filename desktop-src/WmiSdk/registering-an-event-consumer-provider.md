---
description: Pour créer un fournisseur de consommateur d’événements WMI, vous devez inscrire l' \_ \_ instance Win32Provider qui représente votre fournisseur à l’aide d’une instance de \_ \_ EventConsumerProviderRegistration.
ms.assetid: d1aa035c-f9ee-46b5-9fa5-8af77156f904
ms.tgt_platform: multiple
title: Inscription d’un fournisseur de consommateur d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df6bf47e11b1b9df072f9efbca0ba0f620e96d78
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923383"
---
# <a name="registering-an-event-consumer-provider"></a>Inscription d’un fournisseur de consommateur d’événements

Pour créer un [*fournisseur de consommateur d’événements*](gloss-e.md) WMI, vous devez inscrire l’instance [**\_ \_ Win32Provider**](--win32provider.md) qui représente votre fournisseur à l’aide d’une instance de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md). En tant qu’objet COM, votre fournisseur doit s’inscrire auprès du système d’exploitation et de WMI. La procédure suivante suppose que vous avez déjà implémenté le processus d’inscription, comme décrit dans [inscription d’un fournisseur](registering-a-provider.md).

La procédure suivante décrit comment inscrire un fournisseur de consommateur d’événements.

**Pour inscrire un fournisseur de consommateur d’événements**

1.  Créez une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) qui décrit le fournisseur.
2.  Créez une instance de la classe [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) qui décrit l’ensemble des fonctionnalités du fournisseur.

    Les propriétés définies par [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) incluent le chemin d’accès de l’objet au fournisseur et les noms des classes de consommateur logiques prises en charge par le fournisseur de consommateur d’événements.

    Veillez à baliser la classe avec les qualificateurs **Dynamic** et [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) . Le qualificateur **dynamique** indique que WMI doit utiliser un fournisseur pour récupérer les instances de classe. Le qualificateur du **fournisseur** spécifie le nom du fournisseur que WMI doit utiliser.

L’exemple de code suivant montre comment inscrire un fournisseur de consommateur d’événements.

``` syntax
// Provider registration.
// ======================

instance of __Win32Provider as $P
{
    Name  = "MyEventConsumer";
    CLSID = "{4916157B-FBE7-11d1-AEC4-00C04FB68820}";

    DefaultMachineName = NULL;
    ClientLoadableCLSID = NULL;
    ImpersonationLevel = 0;

    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};


instance of __EventConsumerProviderRegistration
{
    Provider = $P;
    ConsumerClassNames = { "MyConsumer" };
};
```

 

 



