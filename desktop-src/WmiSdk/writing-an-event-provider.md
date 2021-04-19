---
description: Un fournisseur d’événements est un objet COM qui fournit à WMI des notifications d’événements intrinsèques et extrinsèques.
ms.assetid: 075bdc65-4ea3-4f91-9823-1d2d0dc13423
ms.tgt_platform: multiple
title: Écriture d’un fournisseur d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb118d89f214e9fc651c1c9d93abfcfe43f49fc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538875"
---
# <a name="writing-an-event-provider"></a>Écriture d’un fournisseur d’événements

Un fournisseur d’événements est un objet COM qui fournit à WMI des notifications d’événements intrinsèques et extrinsèques. Un événement intrinsèque signale une modification de données interne à WMI, tandis qu’un événement extrinsèque signale un événement défini par l’utilisateur qui n’est pas décrit par un événement intrinsèque. Par exemple, un événement en réponse à des modifications, à la création ou à la suppression de la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) est classifié comme un événement intrinsèque. Un événement qui est généré sur la base d’autres éléments que la modification, la création ou la suppression d’un objet WMI existant est un événement extrinsèque. Quelle que soit la classe prise en charge, vous pouvez implémenter tous les fournisseurs d’événements de la même manière.

La procédure suivante décrit comment implémenter un fournisseur d’événements.

**Pour implémenter un fournisseur d’événements**

1.  Concevez et inscrivez votre fournisseur de classes avec WMI.

    Les fournisseurs de classes s’inscrivent auprès de WMI en créant une instance [**\_ \_ Win32Provider**](--win32provider.md) et une classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) . Pour plus d’informations, consultez [inscription d’un fournisseur d’événements](registering-an-event-provider.md).

2.  Implémentez l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour votre fournisseur.

    L’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) est une interface couramment utilisée par WMI pour charger et initialiser tous les fournisseurs. Pour plus d’informations, consultez [initialisation d’un fournisseur](initializing-a-provider.md).

3.  Implémentez [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) comme interface principale pour votre fournisseur.

    L’interface [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) utilise la méthode **ProviderEvents** pour fournir des événements à WMI. Pour plus d’informations, consultez [implémentation de l’interface principale pour un fournisseur d’événements](implementing-the-primary-interface-for-an-event-provider.md).

    > [!Note]  
    > Les fournisseurs d’événements doivent utiliser le modèle de multithread « both ».

     

4.  Si vous le souhaitez, vous pouvez également implémenter l’interface [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) pour augmenter les performances de votre fournisseur d’événements.

    L’interface [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) permet au fournisseur d’optimiser les requêtes avant d’envoyer une réponse à WMI et est particulièrement utile pour un fournisseur qui fournit des événements de plusieurs types et qui doit effectuer autant d’optimisations internes que possible. Pour plus d’informations, consultez [optimisation d’un fournisseur d’événements](optimizing-an-event-provider.md).

5.  Implémentez l’interface [**IWbemEventProviderSecurity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) pour limiter les consommateurs à certains identificateurs de sécurité (SID) ou implémentez [**IWbemEventSink :: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) pour sécuriser le récepteur lui-même. Le fournisseur peut également définir la **propriété \_ descripteur de sécurité** dans la classe d’événements pour sécuriser les événements individuels dans le code MOF. Pour plus d’informations, consultez [sécurisation des événements WMI](securing-wmi-events.md).
6.  Ajoutez tout code supplémentaire nécessaire pour votre fournisseur.

    Lorsque vous concevez votre fournisseur, vous devez probablement appeler des interfaces WMI. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

    Lorsque vous récupérez des informations pour un client, vous devrez peut-être accéder aux niveaux de sécurité de ce client. Pour plus d’informations, consultez [emprunt d’identité d’un client](impersonating-a-client.md).

7.  Remplacez le fournisseur préexistant par votre nouveau code.

    Vous n’avez pas besoin d’effectuer cette étape si vous n’avez pas de fournisseur préexistant à copier. Pour plus d’informations, consultez [mise à jour d’un fournisseur](updating-a-provider.md).

Une application cliente peut demander un événement en s’inscrivant auprès de WMI en tant que consommateur d’événements. Pour plus d’informations, consultez [réception d’un événement WMI](receiving-a-wmi-event.md).

 

 
