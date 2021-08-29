---
description: Un filtre d’événements est une classe WMI qui décrit les événements que WMI remet à un consommateur physique.
ms.assetid: c0ce26a4-5ff2-44b4-8550-c7d8ad0ba0f0
ms.tgt_platform: multiple
title: Création d’un filtre d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f44f49c9a7f38b23353dc8c6343ca1d72194e3b7f121538c93f545e45c31e3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568829"
---
# <a name="creating-an-event-filter"></a>Création d’un filtre d’événements

Un filtre d’événements est une classe WMI qui décrit les événements que WMI remet à un consommateur physique. Par exemple, un filtre d’événements peut indiquer à WMI de remettre à un consommateur tous les événements de gestion de l’alimentation, ou tous les événements de redémarrage du système. Un filtre d’événements décrit également les conditions dans lesquelles WMI remet les événements. Un filtre d’événements peut spécifier un événement intrinsèque ou extrinsèque ; et le filtre peut faire référence aux événements qui proviennent de l’espace de noms, autrement dit, à l’exception de l’espace de noms du filtre. Le consommateur permanent doit avoir le même [**CreatorSID**](--eventconsumer.md) dans les instances de consommateur, de filtre et de liaison. Pour plus d’informations, consultez [réception d’événements en toute sécurité](receiving-events-securely.md).

La procédure suivante décrit comment créer un filtre d’événements.

**Pour créer un filtre d’événements**

1.  Créez une instance de la classe système [**\_ \_ EventFilter**](--eventfilter.md) WMI.
2.  Créez un identificateur unique pour votre filtre avec la propriété **Name** , de l’une des deux manières suivantes :

    -   Utilisez un schéma privé.

        Le fait de nommer arbitrairement vos filtres d’événements fonctionne tant que vous n’êtes pas en conflit avec d’autres modèles de noms de filtre. Vous devez éviter les conflits de noms, car l’ajout d’une instance avec une valeur de **nom** en double remplace l’ancienne instance.

    -   Utilisez un identificateur global unique (GUID).

        Si vous laissez le **nom** vide, WMI remplit le **nom** avec un GUID.

3.  Décrivez le type d’événement que vous souhaitez filtrer à l’aide de la propriété de **requête** .

    La propriété de **requête** contient la requête langage de requêtes WMI (WQL) (WQL) qui décrit le type d’événement que vous souhaitez filtrer. Vous pouvez obtenir un filtrage précis à l’aide d’un ensemble d’opérateurs et d’extensions pour WQL.

    Un événement de journal NT est généré lorsqu’une requête d’un consommateur d’événements permanent échoue. La source de l’événement est WinMgmt, l’ID d’événement est 10 et le type d’événement est Error.

    WMI est plus efficace pour traiter des requêtes spécifiques et restrictives que les requêtes larges. En créant une requête spécifique, vous pouvez éviter la communication entre processus et le trafic réseau inutiles. Dans les cas d’événements générés par un fournisseur, WMI effectue le filtrage en cours au fournisseur ; Cela garantit que seuls les événements correspondant au filtre entraînent le coût de communication entre processus. Pour plus d’informations, consultez [interrogation de WMI](querying-wmi.md).

4.  Définissez la propriété **QueryLanguage** sur le type de langage de requête que vous utilisez dans la propriété de **requête** .

    Vous allez presque toujours définir **QueryLanguage** sur « WQL ».

L’exemple de code suivant décrit un filtre d’événement qui signale un événement chaque fois que WMI crée une instance de la classe [**\_ \_ TimerEvent**](--timerevent.md) dans l' \\ espace de noms CIMV2 racine.

``` syntax
instance of __EventFilter as $FILTER
{
    Name = "MyFilterName";
    Query = "select * from __TimerEvent where TimerID=\"MyTimer\"";
    QueryLanguage = "WQL";
    EventNamespace = "\root\cimv2";

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

La propriété **EventNamespace** spécifie l’espace de noms à partir duquel les événements proviennent. Vous n’avez pas besoin de créer une instance des filtres dans l’espace de noms où proviennent les événements. Si vous ne spécifiez pas l’espace de noms, WMI crée le filtre dans l’espace de noms par défaut. Les classes d’événements intrinsèques, telles que [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) , sont disponibles dans chaque espace de noms.

Pour inscrire votre consommateur logique pour les notifications d’événements, vous devez lier les filtres d’événements à un consommateur logique. Pour plus d’informations, consultez [liaison d’un filtre d’événements à un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md).

 

 



