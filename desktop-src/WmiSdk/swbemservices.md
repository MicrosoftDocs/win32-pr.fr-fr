---
description: Vous pouvez utiliser les méthodes d’un objet SWbemServices pour effectuer des opérations sur un espace de noms sur un hôte local ou un hôte distant. Cet objet ne peut pas être créé par l’appel VBScript CreateObject.
ms.assetid: 7fcfa404-2fe6-42e5-85ac-64536f6d2a44
ms.tgt_platform: multiple
title: Objet SWbemServices (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices
- ISWbemServices
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4303b3226acc6d773ed35e77176e05e3a58c567d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403573"
---
# <a name="swbemservices-object"></a>Objet SWbemServices

Vous pouvez utiliser les méthodes d’un objet **SWbemServices** pour effectuer des opérations sur un espace de noms sur un hôte local ou un hôte distant. Cet objet ne peut pas être créé par l’appel VBScript **CreateObject** .

## <a name="members"></a>Membres

L’objet **SWbemServices** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SWbemServices** possède ces méthodes.



| Méthode                                                                         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssociatorsOf**](swbemservices-associatorsof.md)                           | Récupère les instances des ressources managées associées à une ressource spécifiée par le biais d’une ou plusieurs classes d’association. Vous fournissez le chemin d’accès de l’objet pour le point de terminaison d’origine, et [**AssociatorsOf**](swbemservices-associatorsof.md) retourne les ressources managées au point de terminaison opposé. La méthode **AssociatorsOf** effectue la même fonction que celle que la requête WQL « associateurs de » effectue.<br/>                                                                           |
| [**AssociatorsOfAsync**](swbemservices-associatorsofasync.md)                 | Retourne de façon asynchrone une collection d’objets (classes ou instances) associés à un objet spécifié.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| [**Supprimer**](swbemservices-delete.md)                                         | Supprime une instance d’une ressource managée (ou une définition de classe de l’espace de stockage CIM).<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**DeleteAsync**](swbemservices-deleteasync.md)                               | Supprime de façon asynchrone la classe ou l’instance spécifiée dans le chemin d’accès de l’objet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ExecMethod**](swbemservices-execmethod.md)                                 | Fournit une autre façon d’exécuter une méthode définie par une définition de classe de ressource managée. Principalement utilisé dans les situations où le langage de script ne prend pas en charge les paramètres de sortie. par exemple, JScript ne prend pas en charge les paramètres out.<br/>                                                                                                                                                                                                                                            |
| [**ExecMethodAsync**](swbemservices-execmethodasync.md)                       | Exécute de façon asynchrone une méthode qui est exportée par un fournisseur de méthode.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ExecNotificationQuery**](swbemservices-execnotificationquery.md)           | Exécute une requête d’abonnement aux événements pour recevoir des événements. Une requête d’abonnement aux événements est une requête qui définit une modification de l’environnement géré que vous souhaitez analyser. Lorsque la modification se produit, l’infrastructure WMI remet un événement décrivant la modification apportée au script appelant.<br/>                                                                                                                                                                                                        |
| [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) | Exécute de façon asynchrone une requête pour recevoir des événements.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ExecQuery**](swbemservices-execquery.md)                                   | Exécute une requête pour récupérer une collection d’instances de ressources gérées par WMI (ou définitions de classe). [**ExecQuery**](swbemservices-execquery.md) peut être utilisé pour récupérer une collection filtrée d’instances qui correspondent aux critères que vous définissez dans la requête transmise à **ExecQuery**.<br/>                                                                                                                                                                                                           |
| [**ExecQueryAsync**](swbemservices-execqueryasync.md)                         | Exécute de façon asynchrone une requête pour récupérer des objets.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Télécharger**](swbemservices-get.md)                                               | Récupère une instance unique d’une ressource managée (ou une définition de classe) en fonction d’un chemin d’accès d’objet.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**GetAsync**](swbemservices-getasync.md)                                     | Récupère de manière asynchrone un objet, qui est soit une définition de classe, soit une instance, en fonction du chemin d’accès de l’objet.<br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**InstancesOf**](swbemservices-instancesof.md)                               | Récupère toutes les instances d’une ressource managée en fonction d’un nom de classe. Par défaut, [**InstancesOf**](swbemservices-instancesof.md) effectue une récupération complète. Autrement dit, la méthode **InstancesOf** récupère les instances de la ressource identifiée par le nom de classe passé à la méthode et récupère également toutes les instances de toutes les ressources qui sont des sous-classes (définies sous) de la classe cible.<br/>                                                                                       |
| [**InstancesOfAsync**](swbemservices-instancesofasync.md)                     | Retourne de façon asynchrone les instances d’une classe spécifiée en fonction des critères de sélection spécifiés par l’utilisateur.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| [**ReferencesTo**](swbemservices-referencesto.md)                             | Retourne toutes les associations qui font référence à une ressource spécifiée. La meilleure façon de comprendre [**ReferencesTo**](swbemservices-referencesto.md) est de le comparer à la méthode [**AssociatorsOf**](swbemservices-associatorsof.md) . **AssociatorsOf** retourne les ressources dynamiques qui se trouvent à l’extrémité opposée d’une association. **ReferencesTo** retourne l’Association elle-même. La méthode **ReferencesTo** effectue la même fonction que celle exécutée par la requête WQL « références de ».<br/> |
| [**ReferencesToAsync**](swbemservices-referencesto.md)                        | Retourne de façon asynchrone une collection de toutes les classes d’association ou instances qui font référence à une classe ou une instance spécifique.<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**SubclassesOf**](swbemservices-subclassesof.md)                             | Récupère toutes les sous-classes d’une classe spécifiée à partir du référentiel CIM.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**SubclassesOfAsync**](swbemservices-subclassesofasync.md)                   | Retourne de façon asynchrone une collection de sous-classes pour une classe spécifiée.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

### <a name="properties"></a>Propriétés

L’objet **SWbemServices** possède ces propriétés.



| Propriété                                                 | Type d’accès          | Description                                                                          |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------|
| [**Sécurité\_**](swbemservices-security-.md)<br/> | Lecture seule<br/> | Utilisé pour obtenir ou définir les paramètres de sécurité d’un objet **SWbemServices** .<br/> |



 

## <a name="remarks"></a>Remarques

Les méthodes peuvent être appelées en mode synchrone, en mode asynchrone ou en mode semi-synchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

**Vue d'ensemble**

**SWbemServices** dessert deux rôles principaux. Tout d’abord, l’objet **SWbemServices** représente une connexion authentifiée à un espace de noms WMI sur un ordinateur cible. Ensuite, **SWbemServices** est l’objet Automation que vous utilisez pour récupérer des ressources gérées par WMI. Vous pouvez obtenir une référence à un objet **SWbemServices** de l’une des deux manières suivantes :

-   Comme illustré dans la plupart des scripts WMI présentés jusqu’à présent, vous pouvez utiliser la fonction VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) en association avec le moniker WMI « winmgmts : ». L’exemple suivant est la forme la plus simple d’une connexion WMI. L’exemple se connecte à l’espace de noms par défaut (généralement « root \\ cimv2 ») sur l’ordinateur local :

    `Set objSWbemServices = GetObject("winmgmts:")`

-   Vous pouvez également utiliser la méthode [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) de l’objet [**SWbemLocator**](swbemlocator.md) pour obtenir une référence à un objet **SWbemServices** .

Une fois que vous avez obtenu une référence à un objet **SWbemServices** , vous utilisez la référence d’objet pour appeler 1 des 18 méthodes disponibles à l’aide de **SWbemServices**. **SWbemServices** peut retourner l’un des trois objets de bibliothèque de script WMI différents ([**SWbemObjectSet**](swbemobjectset.md), [**SWbemObject**](swbemobject.md)ou [**SWbemEventSource**](swbemeventsource.md)), selon la méthode que vous appelez. Si vous connaissez le type d’objet retourné par la méthode, vous pourrez déterminer l’étape suivante que votre script doit effectuer. Par exemple, si vous récupérez une collection **SWbemObjectSet**, vous devez énumérer la collection pour accéder à chaque **SWbemObject** de la collection. Si vous récupérez un **SWbemObject**, vous pouvez immédiatement accéder aux méthodes et propriétés de l’objet sans énumérer la collection en premier.

**Modes de fonctionnement**

**SWbemServices** prend en charge trois modes de fonctionnement : synchrone, asynchrone et semi-synchrone.

-   **Synchronous**. En mode synchrone, votre script bloque (interrompt) jusqu’à la fin de la méthode **SWbemServices** . Non seulement votre script est en attente, mais dans les cas où WMI récupère des instances de ressources managées, WMI génère la totalité de la base de données [**SWbemObjectSet**](swbemobjectset.md) en mémoire avant que le premier octet de données ne soit renvoyé au script appelant. Cela peut avoir un effet néfaste sur les performances du script et sur l’ordinateur exécutant le script. par exemple, la récupération synchrone de milliers d’événements à partir des journaux d’événements Windows peut prendre beaucoup de temps et utiliser beaucoup de mémoire. Pour ces raisons, les opérations synchrones ne sont pas recommandées, sauf pour les trois méthodes ([**Delete**](swbemservices-delete.md), [**ExecMethod**](swbemservices-execmethod.md)et [**obtenir**](swbemservices-get.md)) qui sont synchrones par défaut. Ces méthodes ne retournent pas de jeux de données volumineux, de sorte que l’opération semi-synchrone n’est pas nécessaire.
-   **Asynchrone**. En mode asynchrone, votre script appelle l’une des neuf méthodes asynchrones et est retourné immédiatement. Autrement dit, dès que la méthode asynchrone est appelée, votre script reprend l’exécution de la ligne de code suivante. Pour utiliser une méthode asynchrone, votre script doit d’abord créer un objet [**SWbemSink**](swbemsink.md) et une sous-routine spéciale appelée gestionnaire d’événements. WMI exécute l’opération asynchrone et notifie le script en appelant la sous-routine du gestionnaire d’événements lorsque l’opération est terminée.
-   **Semi-synchrone**. Le mode semi-synchrone est un compromis entre synchrone et asynchrone. Les opérations semi-synchrones offrent de meilleures performances que les opérations synchrones, mais elles ne nécessitent pas les connaissances supplémentaires et les étapes de script nécessaires pour gérer les opérations asynchrones. Il s’agit du type d’opération par défaut pour la plupart des requêtes WMI.

    En mode semi-synchrone, votre script appelle l’une des six méthodes de récupération de données et retourne immédiatement. WMI récupère les ressources managées en arrière-plan à mesure que votre script continue de s’exécuter. À mesure que les ressources sont récupérées, elles sont immédiatement retournées à votre script par le biais d’une SWbemObjectSet. Vous pouvez commencer à accéder aux ressources managées sans attendre que l’ensemble de la collection soit assemblé.

    Il y a un inconvénient pour les opérations semi-synchrones lorsque vous travaillez avec des ressources managées qui ont de nombreuses instances (une signification supérieure à 1 000), telles que le [**\_ fichier de fichier CIM**](/windows/desktop/CIMWin32Prov/cim-datafile) et [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). L’inconvénient est le résultat de la façon dont WMI gère les instances des ressources managées. Pour chaque instance d’une ressource managée, WMI crée et met en cache un objet [**SWbemObject**](swbemobject.md) . Lorsqu’il existe un grand nombre d’instances pour une ressource managée, la récupération de l’instance peut monopoliser les ressources disponibles, ce qui réduit les performances du script et de l’ordinateur.

    Pour contourner le problème, vous pouvez optimiser les appels de méthode semi-synchrone à l’aide de l’indicateur **wbemFlagForwardOnly** . L’indicateur **wbemFlagForwardOnly** , combiné avec l’indicateur **wbemFlagReturnImmediately** (l’indicateur semi-synchrone par défaut), indique à WMI de retourner une [**SWbemObjectSet**](swbemobjectset.md)avant uniquement, ce qui élimine le problème de performances du jeu de données volumineux. Toutefois, l’utilisation de l’indicateur **wbemFlagForwardOnly** est un coût. Une **SWbemObjectSet** avant uniquement ne peut être énumérée qu’une seule fois. Une fois que vous avez accédé à chaque [**SWbemObject**](swbemobject.md) dans une instance de la version **avant uniquement,** la mémoire allouée à l’instance est libérée.

À l’exception des méthodes asynchrones [**Delete**](swbemservices-delete.md), [**ExecMethod**](swbemservices-execmethod.md), [**obten**](swbemservices-get.md)et neuf, semi-synchrone est le mode de fonctionnement par défaut et recommandé.

**Méthodes couramment utilisées**

Les méthodes les plus souvent utilisées dans les scripts d’administration de système sont [**InstancesOf**](swbemservices-instancesof.md), [**ExecQuery**](swbemservices-execquery.md), [**obten**](swbemservices-get.md)et [**ExecNotificationQuery**](swbemservices-execnotificationquery.md). Bien que souvent utilisé, **InstancesOf** n’est pas nécessairement la méthode recommandée pour récupérer des informations (même si c’est sans aucun doute le moyen le plus simple).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> <dt>

[Appel d’une méthode](calling-a-method.md)
</dt> </dl>

 

