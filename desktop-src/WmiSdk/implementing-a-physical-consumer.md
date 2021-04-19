---
description: Un consommateur physique est un objet COM qui implémente l’interface IWbemUnboundObjectSink.
ms.assetid: 497457dc-61ca-4527-89fd-2af0383de5e9
ms.tgt_platform: multiple
title: Implémentation d’un consommateur physique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0a9530ed7a98ce19b3b39f2f5a1fe52f3b0631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521851"
---
# <a name="implementing-a-physical-consumer"></a>Implémentation d’un consommateur physique

Un consommateur physique est un objet COM qui implémente l’interface [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) . WMI charge votre consommateur physique et passe des événements via **IWbemUnboundObjectSink** en réponse à un ou plusieurs événements, comme défini par le consommateur logique associé. Les consommateurs permanents ont des exigences particulières en matière de sécurité. Pour plus d’informations, consultez [sécurisation des événements WMI](securing-wmi-events.md).

La procédure suivante décrit comment implémenter un consommateur physique pour un consommateur d’événements permanent.

**Pour implémenter un consommateur physique pour un consommateur d’événements permanent**

1.  Créez un objet COM.

    Vous devez implémenter un consommateur physique en tant que serveur local ou distant à l’aide du protocole COM.

2.  Déterminez si vous souhaitez prendre en charge la notification d’événements synchrones ou asynchrones.

    Avec la notification d’événement asynchrone, le thread d’envoi n’est pas lié au thread de réception. Par conséquent, ni WMI ni le fournisseur d’événements ne sont bloqués alors que WMI envoie une notification à tout consommateur inscrit pour recevoir l’événement. L’inconvénient de la remise asynchrone est qu’un changement de contexte se produit entre le moment où le fournisseur produit l’événement et le moment où le consommateur reçoit l’événement. Pour plus d’informations sur le travail de façon asynchrone, consultez la rubrique [notions de base de com](../com/guide.md) dans la section com du kit de développement logiciel (SDK) Microsoft Windows. Pour plus d’informations sur les changements de contexte, consultez la rubrique [changements de contexte](../procthread/context-switches.md) dans la section dll, processus et threads de la SDK Windows.

    > [!Note]  
    > Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

     

    Avec la notification synchrone, WMI remet la notification sur le même thread que celui utilisé par le fournisseur d’événements pour remettre l’événement à WMI. Dans ce cas, lorsqu’un fournisseur d’événements envoie une notification, le fournisseur d’événements est bloqué par WMI jusqu’à ce que WMI remette la notification. Uniquement si votre consommateur est extrêmement rapide et peut traiter un événement en microsecondes de 100 ou moins, si vous envisagez de prendre en charge la notification synchrone. Les consommateurs synchrones qui prennent trop de temps pour traiter les événements peuvent gravement ralentir la remise des événements à tous les autres consommateurs. En outre, ils peuvent bloquer le fournisseur par inadvertance. Pour plus d’informations, consultez [liaison d’un filtre d’événements à un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md).

3.  Implémentez la fonction [**IWbemUnboundObjectSink :: IndicateToConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemunboundobjectsink-indicatetoconsumer) .

    WMI utilise la fonction [**IndicateToConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemunboundobjectsink-indicatetoconsumer) pour passer les pointeurs et les événements nécessaires à votre consommateur physique pour les communications synchrones et asynchrones. Votre implémentation de **IndicateToConsumer** doit contenir l’ensemble du code nécessaire pour répondre à un événement.

    Contrairement à un consommateur d’événements temporaire, vous n’avez pas besoin d’appeler l’interface [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) pour contacter WMI. Au lieu de cela, WMI localise un pointeur vers votre consommateur par le biais du fournisseur de consommateur d’événements. Pour plus d’informations, consultez [écriture d’un fournisseur de consommateur d’événements](writing-an-event-consumer-provider.md).

    Toutefois, si vous souhaitez rappeler WMI, utilisez les interfaces [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) et [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . La méthode traditionnelle pour la connexion à WMI est pendant le processus d’initialisation de votre objet COM. Pour plus d’informations, consultez [création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md).

    Si vous implémentez votre consommateur physique en tant que serveur COM in-process et que vous vous connectez à WMI séparément du processus d’initialisation, vous devez utiliser l’identificateur de classe **CLSID \_ WbemAdministrativeLocator** pour accéder à l’interface [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) dans l’appel à [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    L’exemple suivant montre comment utiliser l’identificateur de classe **\_ WbemAdministrativeLocator CLSID** pour accéder à l’interface [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) .

    ```C++
    IWbemLocator *pLoc = 0;

    DWORD dwRes = CoCreateInstance(CLSID_WbemAdministrativeLocator, 0, 
        CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
    ```

    

    L’interface [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) obtient le pointeur d’espace de noms initial vers WMI sur un ordinateur hôte particulier. Si vous n’utilisez pas l’identificateur **\_ WbemAdministrativeLocator CLSID** dans l’appel [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , une erreur « Accès refusé » est générée.

    Dans des circonstances habituelles, WMI fournit des événements asynchrones au client, l’un après l’autre. Toutefois, si un client ne peut pas recevoir de notifications d’événements asynchrones aussi rapidement que les événements arrivent, WMI commence à traiter automatiquement les événements en un seul appel. Le traitement automatique vous aide si les temps d’aller-retour sont un problème, comme c’est souvent le cas dans les scénarios à débit élevé. Toutefois, le traitement par lot n’améliore pas les performances du système si le client ou la bande passante réseau est défaillant.

 

 
