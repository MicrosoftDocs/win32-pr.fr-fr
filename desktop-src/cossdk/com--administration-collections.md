---
description: Les collections d’administration COM+ servent à conserver et organiser les données de configuration stockées dans le catalogue COM+.
ms.assetid: eed8ca97-39ad-4188-afc6-8670b5073fad
title: Regroupements d’administration COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceb49ecd382e5a5a570e3e479714ad905a5eaf5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403558"
---
# <a name="com-administration-collections"></a>Regroupements d’administration COM+

Les collections d’administration COM+ servent à conserver et organiser les données de configuration stockées dans le catalogue COM+. Les regroupements correspondent aux dossiers de l’arborescence de la console de l’outil d’administration Services de composants. Vous pouvez accéder à ces regroupements à l’aide des objets et des interfaces d’administration COM+.

Vous lancez l’administration par programme à l’aide d’objets créés à partir de la classe [**COMAdminCatalog**](comadmincatalog.md) , vous représentez toutes les collections du catalogue à l’aide d’objets créés à partir de la classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , et vous représentez des éléments dans des collections à l’aide d’objets créés à partir de la classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .

Les éléments d’une collection donnée exposent un jeu de propriétés cohérent. Par exemple, chaque élément de la collection [**Components**](components.md) représente un composant et les éléments de la collection **Components** exposent les mêmes propriétés que celles utilisées pour configurer un composant. Ces propriétés sont accessibles à l’aide de la classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .

> [!Note]  
> Les propriétés avec accès WriteOnce sont ReadWrite lors de l’utilisation de la méthode [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) avant d’utiliser [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) et sont en lecture seule par la suite.

 

Pour une introduction à l’administration par programme de COM+, consultez automatisation de l' [administration com+](automating-com--administration.md).

## <a name="collection-hierarchy"></a>Hiérarchie de collection

La figure suivante illustre les relations entre les collections. Les collections à l’extrême gauche (zones blanches et grises) sont des collections de niveau supérieur, accessibles en appelant la méthode [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) d’un objet créé à partir de la classe [**COMAdminCatalog**](comadmincatalog.md) . Les collections restantes (dans les zones jaunes) sont accessibles uniquement via leur collection parente, en appelant la méthode [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) qui représente leur parent. Les flèches pointent d’une collection parent vers ses collections enfants.

![Diagramme qui montre les relations entre les collections.](images/ab61b0ab-2368-4bd8-9cfc-b7adc5beaca3.png)

Les quatre regroupements suivants ne sont pas illustrés dans la figure : [**errorInfo**](errorinfo.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md)et [**root**](root.md). La collection **errorInfo** est un enfant de chaque collection de la figure, à l’exception de [**InprocServers**](inprocservers.md) et [**WOWInprocServers**](wowinprocservers.md) (dans les zones grises). Les collections **PropertyInfo** et **RelatedCollectionInfo** sont des enfants de chaque collection. La collection **racine** est une collection de niveau supérieur qui est le parent de toutes les autres collections de niveau supérieur. Toutefois, il n’est pas nécessaire d’accéder à la collection **racine** avant d’accéder à d’autres collections de niveau supérieur.

## <a name="comadmin-library"></a>Bibliothèque comadmin

Les regroupements suivants sont pris en charge par la bibliothèque comadmin.



| Collection                                                             | Description                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationCluster**](applicationcluster.md)                       | Contient une liste des serveurs dans le cluster d’applications.                                                                                            |
| [**ApplicationInstances**](applicationinstances.md)                   | Contient un objet pour chaque instance d’une application COM+ en cours d’exécution.                                                                                   |
| [**Applications**](applications.md)                                   | Contient un objet pour chaque application COM+ installée sur l’ordinateur local.                                                                         |
| [**Composants**](components.md)                                       | Contient un objet pour chaque composant de l’application à laquelle il est associé.                                                                      |
| [**ComputerList**](computerlist.md)                                   | Contient la liste des ordinateurs figurant dans le dossier **ordinateurs** de l’outil d’administration Services de composants.                                     |
| [**DCOMProtocols**](dcomprotocols.md)                                 | Contient une liste des protocoles à utiliser par DCOM. Elle contient un objet pour chaque protocole.                                                         |
| [**ErrorInfo**](errorinfo.md)                                         | Récupère des informations d’erreur étendues concernant les méthodes qui traitent plusieurs objets.                                                               |
| [**EventClassesForIID**](eventclassesforiid.md)                       | Récupère des informations sur les classes d’événements.                                                                                                        |
| [**FilesForImport**](filesforimport.md)                               | Récupère des informations de son fichier MSI sur une application qui peut être importée.                                                                    |
| [**InprocServers**](inprocservers.md)                                 | Contient la liste des serveurs in-process inscrits auprès du système. Elle contient un objet pour chaque composant.                                       |
| [**InterfacesForComponent**](interfacesforcomponent.md)               | Contient un objet pour chaque interface exposée par le composant auquel la collection est associée.                                                    |
| [**LegacyComponents**](legacycomponents.md)                           | Contient un objet pour chaque composant non configuré dans l’application à laquelle il est associé.                                                         |
| [**LegacyServers**](legacyservers.md)                                 | Identique à la collection [**InprocServers**](inprocservers.md) , à ceci près que cette collection comprend également des serveurs locaux.                           |
| [**LocalComputer**](localcomputer.md)                                 | Contient un objet unique qui contient les informations de paramètres au niveau de l’ordinateur pour l’ordinateur dont vous accédez au catalogue.                             |
| [**MethodsForInterface**](methodsforinterface.md)                     | Contient un objet pour chaque méthode sur l’interface à laquelle la collection est associée.                                                               |
| [**Partitions**](partitions.md)                                       | Utilisé pour spécifier les applications contenues dans chaque partition.                                                                                         |
| [**PartitionUsers**](partitionusers.md)                               | Utilisé pour spécifier les utilisateurs contenus dans chaque partition.                                                                                                |
| [**PropertyInfo**](propertyinfo.md)                                   | Récupère des informations sur les propriétés prises en charge par une collection spécifiée.                                                                      |
| [**PublisherProperties**](publisherproperties.md)                     | Contient un objet pour chaque propriété de serveur de publication pour la collection [**SubscriptionsForComponent**](subscriptionsforcomponent.md) parente.              |
| [**RelatedCollectionInfo**](relatedcollectioninfo.md)                 | Récupère des informations sur d’autres collections relatives à la collection à partir de laquelle elle est appelée.                                                      |
| [**Rôles**](roles.md)                                                 | Contient un objet pour chaque rôle affecté à l’application à laquelle il est associé.                                                                  |
| [**RolesForComponent**](rolesforcomponent.md)                         | Contient un objet pour chaque rôle assigné au composant auquel la collection est associée.                                                        |
| [**RolesForInterface**](rolesforinterface.md)                         | Contient un objet pour chaque rôle assigné à l’interface à laquelle la collection est associée.                                                        |
| [**RolesForMethod**](rolesformethod.md)                               | Contient un objet pour chaque rôle assigné à la méthode à laquelle la collection est associée.                                                           |
| [**RolesForPartition**](rolesforpartition.md)                         | Contient un objet pour chaque rôle affecté à la partition à laquelle la collection est associée.                                                        |
| [**Causes**](root.md)                                                   | Contient les collections de niveau supérieur sur le catalogue.                                                                                                    |
| [**SubscriberProperties**](subscriberproperties.md)                   | Contient un objet pour chaque propriété d’abonné de la collection [**SubscriptionsForComponent**](subscriptionsforcomponent.md) parente.             |
| [**SubscriptionsForComponent**](subscriptionsforcomponent.md)         | Contient un objet pour chaque abonnement de la collection de [**composants**](components.md) parents.                                                  |
| [**TransientPublisherProperties**](transientpublisherproperties.md)   | Contient un objet pour chaque propriété de serveur de publication pour la collection [**TransientSubscriptions**](transientsubscriptions.md) parente.                    |
| [**TransientSubscriberProperties**](transientsubscriberproperties.md) | Contient un objet pour chaque propriété d’abonné de la collection [**TransientSubscriptions**](transientsubscriptions.md) parente.                   |
| [**TransientSubscriptions**](transientsubscriptions.md)               | Contient un objet pour chaque abonnement temporaire.                                                                                                   |
| [**UsersInPartitionRole**](usersinpartitionrole.md)                   | Contient un objet pour chaque utilisateur dans le rôle de partition auquel la collection est associée.                                                            |
| [**UsersInRole**](usersinrole.md)                                     | Contient un objet pour chaque utilisateur du rôle auquel la collection est associée.                                                                      |
| [**WOWInprocServers**](wowinprocservers.md)                           | Contient la liste des serveurs in-process inscrits auprès du système pour les composants 32 bits sur les ordinateurs 64 bits.                                       |
| [**WOWLegacyServers**](wowlegacyservers.md)                           | Identique à la collection [**LegacyServers**](legacyservers.md) , hormis le fait que cette collection est extraite du Registre 32 bits sur les ordinateurs 64 bits. |



 

 

 



