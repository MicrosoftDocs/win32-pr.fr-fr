---
description: À l’aide de la classe SMTPEventConsumer, vous pouvez envoyer un e-mail à un utilisateur désigné lorsqu’un événement spécifié se produit. Cette classe est un consommateur d’événements standard fourni par WMI.
ms.assetid: ed10e6f7-8e18-4cde-bd46-a7791547c7da
ms.tgt_platform: multiple
title: Envoi de courrier électronique à partir d’un événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4929b7c8c29d514d73a6e4c9d14049a19f306233
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517894"
---
# <a name="sending-email-based-on-an-event"></a>Envoi de courrier électronique à partir d’un événement

À l’aide de la classe [SMTPEventConsumer](smtpeventconsumer.md) , vous pouvez envoyer un e-mail à un utilisateur désigné lorsqu’un événement spécifié se produit. Cette classe est un [consommateur d’événements standard](standard-consumer-classes.md) fourni par WMI.

La classe [SMTPEventConsumer](smtpeventconsumer.md) nécessite les conditions suivantes pour envoyer un message électronique en réponse à un événement :

-   La classe [SMTPEventConsumer](smtpeventconsumer.md) doit être compilée dans l’espace de noms approprié. Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).
-   Un serveur SMTP doit exister sur le réseau.
-   Le message électronique ne peut pas avoir une pièce jointe.
-   Le message électronique doit être encodé en US-ASCII.

La procédure de base pour l’utilisation de consommateurs standard est toujours la même, et se trouve dans la [surveillance et la réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md). La procédure suivante ajoute à la procédure de base. est spécifique à la classe [SMTPEventConsumer](smtpeventconsumer.md) ; et décrit comment créer un consommateur d’événements qui envoie des messages électroniques.

La procédure suivante décrit comment créer un consommateur d’événements qui envoie des messages électroniques.

**Pour créer un consommateur d’événements qui envoie des messages électroniques**

1.  Installez et inscrivez la classe [SMTPEventConsumer](smtpeventconsumer.md) , si nécessaire.

    La classe [SMTPEventConsumer](smtpeventconsumer.md) est compilée dans l' \\ espace de noms de l’abonnement racine par le programme d’installation de WMI.

2.  Identifiez l’événement que vous souhaitez surveiller et créez la requête d’événement.

    Il peut y avoir un événement intrinsèque existant qui utilise pour surveiller votre événement. La plupart des événements intrinsèques sont associés aux modifications apportées aux instances de classe dans l’espace de noms « root \\ cimv2 ». En analysant les classes de la référence des [classes WMI](wmi-classes.md) , vous pouvez trouver une classe qui identifie l’événement que vous souhaitez analyser. Par exemple, utilisez la classe disque [**\_ logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) pour surveiller les modifications apportées à un lecteur de disque dur.

    S’il n’existe aucun événement intrinsèque existant qui utilise, un fournisseur d’événements extrinsèque peut fonctionner. Par exemple, utilisez la classe [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) du fournisseur Registry pour surveiller les modifications apportées au registre système.

    S’il n’existe pas de classe qui identifie l’événement que vous souhaitez analyser, vous devez créer votre propre fournisseur d’événements et définir de nouvelles classes d’événements extrinsèques. Pour plus d’informations, consultez [écriture d’un fournisseur d’événements](writing-an-event-provider.md).

3.  Dans le fichier format MOF (MOF), créez une instance de [SMTPEventConsumer](smtpeventconsumer.md) pour recevoir des événements.

    Utilisez les propriétés de l’instance pour définir le message électronique à envoyer lorsqu’un événement se produit. Par exemple, la propriété **ToLine** définit l’adresse de messagerie et la propriété **message** définit le texte du message électronique. Vous devez définir l’adresse de messagerie, l’objet et le texte d’un message, mais un message électronique ne peut pas avoir de pièce jointe. Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](designing-managed-object-format--mof--classes.md).

4.  Créez une requête d’événement qui spécifie les événements que vous souhaitez analyser.

    Pour plus d’informations, consultez [interrogation avec WQL](querying-with-wql.md).

5.  Créez une instance de [**\_ \_ EventFilter**](--eventfilter.md) et stockez votre requête dans la propriété de la **requête** .

    Pour plus d’informations, consultez [interrogation avec WQL](querying-with-wql.md).

6.  Créez une instance de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) pour associer le filtre et le consommateur.
7.  Compilez le fichier MOF à l’aide de [**Mofcomp.exe**](mofcomp.md).


## <a name="example"></a>Exemple

L’exemple de cette section se trouve dans le code MOF, mais vous pouvez créer des instances par programme à l’aide [de l’API de script pour WMI](scripting-api-for-wmi.md) ou [de l’API com pour WMI](com-api-for-wmi.md).

La procédure suivante décrit comment utiliser l’exemple.

**Pour utiliser l’exemple**

1.  Copiez le fichier MOF suivant dans un fichier texte et enregistrez-le avec une extension. mof.
2.  Dans une fenêtre d’invite de commandes, compilez le fichier MOF à l’aide de la commande suivante :

    Fichier **mofcomp** ** * *. mof**

> [!Note]  
> Quand le code MOF est compilé dans l' \\ espace de noms de l’abonnement racine, [SMTPEventConsumer](smtpeventconsumer.md) est compilé dans le même espace de noms.

 

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of __EventFilter as $FILTER
{
    Name = "LowDiskspaceFilter";
    
    EventNamespace = "\\\\.\\root\\cimv2";  

    Query = "SELECT * FROM __InstanceModificationEvent WITHIN 10 "
            "WHERE TargetInstance ISA \"Win32_LogicalDisk\" "
            "AND TargetInstance.FreeSpace < 846000000 "
            "AND PreviousInstance.FreeSpace >= 846000000 "
            "AND (TargetInstance.DeviceID = \"C:\" "
            "OR TargetInstance.DeviceID = \"D:\")";
    QueryLanguage = "WQL";
};


instance of SMTPEventConsumer as $CONSUMER
{
    Name = "LowDisk";
    ToLine = "SysAd@MyCompany.com, MyAlias@MyCompany.com";
    CcLine = "MyHome@MyISP.com";
    ReplyToLine = "MyAlias@MyCompany.com";
    SMTPServer = "SmartHost";
    Subject = "WARNING: Low disk space";
    Message = "WARNING: Your %TargetInstance.DeviceID% is"
        " getting dangerously low.";
};

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER ;
    Filter = $FILTER ;
};
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
