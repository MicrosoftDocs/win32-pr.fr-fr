---
title: Recherche de contenu de domaine
description: Avant de discuter de l’emplacement de la liaison pour commencer une recherche d’objets dans un domaine, il est utile de comprendre comment les données sont stockées dans Active Directory Domain Services.
ms.assetid: fd0b4556-465b-4338-87cb-375450590c44
ms.tgt_platform: multiple
keywords:
- contenu du domaine Active Directory
- recherche de contenu de domaine Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51f775e199cd269eec8a67054ca26bcd69e11eacaa6436781f4481083d11e60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183867"
---
# <a name="searching-domain-contents"></a>Recherche de contenu de domaine

Avant de discuter de l’emplacement de la liaison pour commencer une recherche d’objets dans un domaine, il est utile de comprendre comment les données sont stockées dans Active Directory Domain Services.

Si vous avez une forêt avec plusieurs domaines, Active Directory Domain Services ne stocke pas toutes les données d’objet sur un seul contrôleur de domaine, pour des raisons de performances, d’évolutivité et de fiabilité. Un contrôleur de domaine contient toutes les informations sur le domaine dont il est membre (il dispose d’un réplica complet du domaine). Toutefois, un contrôleur de domaine ne contient pas d’informations complètes sur les autres domaines.

Si vous établissez une liaison à l’objet de domaine avec l’option de repérage de références désactivée, vous pouvez rechercher n’importe quel objet dans ce domaine et uniquement ce domaine. Pour plus d’informations sur le repérage de références, consultez [références](referrals.md). Une recherche peut récupérer n’importe quelle propriété et peut utiliser un filtre de requête contenant n’importe quelle propriété.

Dans une forêt, les domaines sont organisés hiérarchiquement comme des arborescences de domaine. Une arborescence de domaine peut être un domaine unique ou un domaine avec un ou plusieurs domaines enfants. Ces domaines enfants, à leur tour, peuvent avoir des domaines enfants sous eux. Une arborescence de domaine est également un espace de noms contigu. Un espace de noms contigu signifie que les domaines enfants sont une continuation de la hiérarchie d’attribution de noms. Par exemple, un domaine fabrikam.com (ou DC = fabrikam, DC = COM) peut avoir un domaine enfant nommé mydivision (mydivision.fabrikam.com ou DC = mydivision, DC = fabrikam, DC = COM), qui peut à son tour avoir un domaine enfant nommé MyDev (mydev.mydivision.fabrikam.com ou DC = MyDev, DC = mydivision, DC = fabrikam, DC = COM).

Si vous établissez une liaison à un objet de domaine (avec le repérage de références activé) pour un domaine dans une arborescence de domaine, vous allez Rechercher ce domaine et la hiérarchie entière qu’il contient. La recherche peut récupérer n’importe quelle propriété et peut utiliser un filtre de requête contenant n’importe quelle propriété.

Si un contrôleur de domaine contient un réplica complet de uniquement son propre domaine, vous pouvez effectuer une recherche de sous-arborescence sur une arborescence de domaine. Un domaine contient des références à ses domaines enfants. Lorsqu’un contrôleur de domaine traite une demande de recherche de sous-arborescence par rapport à son propre domaine, le contrôleur de domaine recherche ce domaine, puis renvoie les références à chacun de ses domaines enfants au client. Une référence est la façon dont un serveur d’annuaire communique qu’il ne contient pas les informations requises pour effectuer une requête (par exemple, une requête) mais possède une référence à un serveur qui peut contenir les informations requises. Dans le cas d’une recherche de sous-arborescence d’une arborescence de domaine, une référence est retournée pour chaque domaine enfant direct afin que la recherche puisse être poursuivie sur un contrôleur de domaine dans chaque domaine enfant. Si le repérage de références est activé, la bibliothèque cliente LDAP (Wldap32.dll) utilise ces références pour établir une liaison à un contrôleur de domaine dans chaque domaine enfant et poursuivre la recherche. Si le repérage de références est désactivé, le client LDAP ne résout pas les références et la recherche est terminée.

Une recherche de sous-arborescence sur une arborescence de domaine avec le repérage de références activé peut prendre du temps s’il existe une connexion lente aux contrôleurs de domaine pour les domaines enfants. Si vous ne souhaitez rechercher qu’un seul domaine, vous devez désactiver le repérage des références pour éviter d’avoir à rechercher les domaines enfants inutilement.

 

 




