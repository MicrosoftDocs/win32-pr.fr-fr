---
title: Recherche dans le catalogue global
description: Active Directory Domain Services également avoir un catalogue global (GC), qui contient un réplica partiel de tous les objets de l’annuaire.
ms.assetid: 83970563-1a56-4671-b264-56e29939e369
ms.tgt_platform: multiple
keywords:
- recherche dans le catalogue global Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a057330309c12df6d18a209fc3d2adaf42b03005
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671238"
---
# <a name="searching-the-global-catalog"></a>Recherche dans le catalogue global

Active Directory Domain Services également avoir un catalogue global (GC), qui contient un réplica partiel de tous les objets de l’annuaire. Il contient également des réplicas partiels des conteneurs de schéma et de configuration. Un ou plusieurs contrôleurs de domaine dans un domaine peuvent contenir une copie du catalogue global. Pour plus d’informations sur la liaison à un catalogue global, consultez [liaison au catalogue global](binding-to-the-global-catalog.md).

Le catalogue global contient un réplica de chaque objet dans Active Directory Domain Services, mais avec seulement un petit nombre de leurs attributs. Les attributs du catalogue global sont ceux qui sont utilisés le plus fréquemment dans les opérations de recherche, comme le prénom et le nom d’un utilisateur, les noms de connexion, etc. Les attributs de catalogue global incluent également ceux qui sont requis pour localiser un réplica complet de l’objet. Le catalogue global permet aux utilisateurs de trouver rapidement des objets intéressants sans savoir quel domaine les détient et sans avoir besoin d’un espace de noms étendu contigu dans l’entreprise. autrement dit, vous pouvez effectuer une recherche dans l’ensemble de la forêt.

Par conséquent, si vous établissez une liaison à un objet dans le catalogue global, vous allez Rechercher cet objet et la hiérarchie entière en dessous, sans avoir à accéder à un autre serveur. Toutefois, la recherche ne peut utiliser qu’un filtre de requête contenant des propriétés dans le catalogue global et ne peut récupérer que des propriétés dans le catalogue global.

La recherche dans le catalogue global présente les avantages suivants :

-   Le catalogue global vous permet d’effectuer une recherche dans l’ensemble de la forêt ou dans une partie de la forêt, ainsi que dans les conteneurs de schéma et de configuration.
-   Le catalogue global vous permet d’effectuer une recherche complète sur un serveur unique. Aucune référence ou aucun repérage de références n’est requis.

La recherche dans le catalogue global présente les inconvénients suivants :

-   Le catalogue global contient un petit sous-ensemble des propriétés de chaque objet. Si votre filtre de requête comprend des propriétés qui ne se trouvent pas dans le catalogue global, la requête évaluera les expressions contenant ces propriétés comme fausses. Si vous spécifiez des propriétés de catalogue non global dans la liste des propriétés à retourner, ces propriétés ne sont pas récupérées.
-   Pour effectuer une recherche dans le catalogue global, vous devez disposer d’un contrôleur de domaine qui contient un catalogue global. Si aucun n’est disponible, vous ne pouvez pas effectuer une recherche dans le catalogue global.
-   Le catalogue global est en lecture seule. Cela signifie que vous ne pouvez pas effectuer une liaison à un objet dans le catalogue global pour créer, modifier ou supprimer des objets.

 

 




