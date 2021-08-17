---
title: Références (AD DS)
description: Active Directory Domain Services conserver les données de référence dans les objets crossRef stockés dans le conteneur partitions (crossRefContainer) dans le conteneur de configuration.
ms.assetid: e4d6cc8a-9c2c-4e0f-acca-e9ecdd5e879b
ms.tgt_platform: multiple
keywords:
- PUBLICITÉ sur les références
- Active Directory, références
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ea6773157ce01c7b3d47f127697e5aefec02204f3894c10fe856295538334a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184670"
---
# <a name="referrals-ad-ds"></a>Références (AD DS)

Active Directory Domain Services conserver les données de référence dans les objets [**crossRef**](/windows/desktop/ADSchema/c-crossref) stockés dans le conteneur partitions ([**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer)) dans le conteneur de configuration. Dans la rubrique choix de la [recherche](where-to-search.md) , les références sont discutées dans le contexte d’un domaine dans une arborescence de domaine et de la génération de références aux domaines subordonnés dans une recherche de sous-arborescence.

Active Directory Domain Services créer et gérer des objets [**crossRef**](/windows/desktop/ADSchema/c-crossref) pour tous les domaines de la forêt. En outre, il existe des objets **crossRef** pour les conteneurs de schéma et de configuration. Ces objets **crossRef** sont utilisés pour générer des références en réponse aux requêtes qui demandent des données sur les objets qui existent dans la forêt, mais qui ne sont pas contenus dans le serveur d’annuaire qui gère la demande. Il s’agit de *références croisées internes*, car elles font référence à des domaines, des schémas et des conteneurs de configuration au sein de la forêt.

Si le repérage de références n’est pas activé et qu’une recherche de sous-arborescence est effectuée, la recherche renvoie tous les objets du domaine spécifié qui répondent aux critères de recherche. La recherche retourne également les références à tous les domaines subordonnés qui sont des descendants directs du domaine du serveur d’annuaire. Le client doit résoudre les références en liant le chemin d’accès spécifié par la référence et en envoyant une autre requête.

Si le repérage de références est activé et qu’une recherche de sous-arborescence est effectuée, l’API LDAP sous-jacente tente automatiquement d’établir une liaison avec les références et d’ajouter les résultats de la recherche au jeu de résultats. Dans la plupart des cas, le repérage de références est transparent pour l’appelant. Si la référence est un objet d’un domaine ou d’une forêt différent, l’API LDAP sous-jacente tente d’utiliser les informations d’identification actuelles pour établir une liaison à la cible de la référence. Si cette opération réussit, le repérage de références est transparent. En cas d’échec, la référence et un code d’erreur de référence sont renvoyés.

Pour plus d’informations sur la définition de la préférence de recherche de repérage de références, consultez [spécification d’autres options de recherche](specifying-other-search-options.md).

Outre les propriétés [**dNSRoot**](/windows/desktop/ADSchema/a-dnsroot) (nom DNS du domaine) et [**NCName**](/windows/desktop/ADSchema/a-ncname) (nom unique pour le domaine), l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) contient également le **nETBIOSName** (nom NetBIOS du domaine) et le **trustParent** (nom unique de l’objet **crossRef** qui représente le domaine parent direct du domaine).

Active Directory Domain Services pouvez également faire référence à des *références croisées externes* qui font référence à des objets en dehors de la forêt. Les références croisées externes doivent être ajoutées explicitement par un administrateur. N’oubliez pas que le serveur cible de la référence croisée externe doit avoir une racine DNS ; autrement dit, il doit adhérer à la RFC 2247.

Une référence croisée externe fait référence à un objet sur toute autre forêt, à condition que le nom soit unique dans la forêt cible. Par exemple, les applications clientes LDAP utilisées par votre entreprise peuvent envoyer des opérations à vos serveurs d’annuaire pour Fabrikam.com. Vous créez un objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) pour Fabrikam.com. Maintenant, au lieu de renvoyer une erreur d’objet introuvable, vos serveurs d’annuaire peuvent retourner une référence à un objet dans le domaine Fabrikam.com et les clients peuvent effectuer une recherche dans la référence. Par exemple, si vous avez un objet avec le nom unique suivant :


```C++
CN=SomeObject,OU=SomeOU,DC=Fabrikam,DC=Com
```



Vous pouvez ajouter une référence croisée externe pour un objet portant le nom « ChildOfSomeObject ».


```C++
CN=ChildOfSomeObject,CN=SomeObject,OU=SomeOU,DC=Fabrikam,DC=Com
```



Une recherche de sous-arborescence contenant « SomeObject » renverra également une référence à « ChildOfSomeObject ». N’oubliez pas qu’il doit y avoir un serveur LDAP à l’adresse spécifiée par la référence (l’une des propriétés de l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) ) et que ce serveur LDAP doit servir l’espace de noms identifié par « ChildOfSomeObject ».

Étant donné que les objets [**crossRef**](/windows/desktop/ADSchema/c-crossref) sont stockés dans le conteneur de configuration, chaque contrôleur de domaine (DC) possède une copie de tous les objets **crossRef** . Par conséquent, chaque contrôleur de domaine contient des données relatives à chaque domaine de la forêt, ainsi qu’à leurs relations supérieures/subordonnées. Cela permet à chaque contrôleur de domaine de générer des références à n’importe quel domaine de la forêt et des références pour des conteneurs de domaine, de schéma ou de configuration subordonnés inexplorés dans une recherche de sous-arborescence.

Pour plus d’informations sur les références, consultez :

-   [Quand des références sont générées](when-referrals-are-generated.md)
-   [Création d’une référence externe](creating-an-external-referral.md)

Pour plus d’informations et pour obtenir un exemple de code qui montre comment obtenir le nom unique du conteneur partitions, consultez [l’exemple de code pour localiser le conteneur partitions](example-code-for-locating-the-partitions-container.md).

 

 