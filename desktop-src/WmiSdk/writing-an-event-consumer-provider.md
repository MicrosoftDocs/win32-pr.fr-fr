---
description: Un fournisseur de consommateur d’événements est un composant de l’architecture de consommateur permanente qui détermine quel consommateur d’événements permanent gère un événement donné.
ms.assetid: c5a0d0ec-99af-4815-9ad2-e59db70e04ce
ms.tgt_platform: multiple
title: Écriture d’un fournisseur de consommateur d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c7aeeb9b44b37d887df49cf5049d5a9e59ad72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522058"
---
# <a name="writing-an-event-consumer-provider"></a>Écriture d’un fournisseur de consommateur d’événements

Un fournisseur de consommateur d’événements est un composant de l’architecture de consommateur permanente qui détermine quel consommateur d’événements permanent gère un événement donné. Vous devez créer un fournisseur de consommateur d’événements et vos consommateurs d’événements permanents pour router correctement les événements à partir de WMI.

Un fournisseur de consommateur d’événements lie un fournisseur d’événements à une liste de classes de consommateur. Les instances de ces classes de consommateur reçoivent alors des événements de ce fournisseur. WMI identifie le fournisseur de consommateurs auquel les événements sont remis, en fonction de l’instance [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) , qui associe l’instance [**\_ \_ Win32Provider**](--win32provider.md) du fournisseur de consommateurs à une classe de consommateur logique. Les utilisateurs créent des instances de la classe de consommateur dans le cadre d’un abonnement permanent. Si le fournisseur d’événements n’est pas en cours d’exécution lorsqu’un événement se produit, WMI démarre le fournisseur lorsqu’il doit remettre des événements.

La procédure suivante décrit comment implémenter un fournisseur de consommateur d’événements.

**Pour implémenter un fournisseur de consommateur d’événements**

1.  Concevez des classes de consommateur en format MOF (MOF) et inscrivez-les avec WMI. Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](designing-managed-object-format--mof--classes.md).

    Les fournisseurs de classes s’inscrivent auprès de WMI en créant une instance [**\_ \_ Win32Provider**](--win32provider.md) et une classe [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) . Pour plus d’informations, consultez [inscription d’un fournisseur de consommateur d’événements](registering-an-event-consumer-provider.md).

2.  Implémentez l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour votre fournisseur.

    WMI utilise [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour charger et initialiser un fournisseur. Pour plus d’informations, consultez [initialisation d’un fournisseur](initializing-a-provider.md).

    > [!Note]  
    > Les fournisseurs de consommateur d’événements sont fortement encouragés à utiliser le modèle de multithreading « both ».

     

3.  Implémentez l’interface [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) pour votre fournisseur.

    L’interface [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) est l’interface principale d’un fournisseur de consommateur d’événements.

4.  Fournissez un ou plusieurs consommateurs physiques pour recevoir les messages d’événement de WMI.

    Un consommateur physique est un objet COM qui représente un consommateur d’événements permanent. Tous les consommateurs physiques doivent implémenter l’interface [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) . Pour plus d’informations, consultez [implémentation d’un consommateur physique](implementing-a-physical-consumer.md).

 

 



