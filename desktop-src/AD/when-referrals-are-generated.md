---
title: Quand des références sont générées
description: Une référence est la façon dont un serveur d’annuaire communique qu’il ne contient pas les données requises pour exécuter une requête, mais possède une référence à un serveur qui peut contenir les données requises.
ms.assetid: 2c11a52a-26e2-4a50-a0a3-5463a0852b27
ms.tgt_platform: multiple
keywords:
- Active Directory de génération de référence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1eb05d1495e1f6884d6ce6123356ed29235da421839042909fc05aaa4d9d67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182162"
---
# <a name="when-referrals-are-generated"></a>Quand des références sont générées

Une référence est la façon dont un serveur d’annuaire communique qu’il ne contient pas les données requises pour exécuter une requête, mais possède une référence à un serveur qui peut contenir les données requises. N’oubliez pas que les références ne sont pas générées uniquement par les demandes de requête.

Les opérations suivantes peuvent aboutir à une ou plusieurs références :

-   Liaison à un serveur qui ne contient pas l’objet spécifié par le nom unique demandé mais contient des données sur un serveur ou un domaine qui peut contenir cet objet. Pour ADSI, cela peut se produire si l’application appelle [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) ou [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) pour établir une liaison à un objet qui existe dans un autre domaine de la forêt (référence interne) ou un contexte de nommage complètement distinct de la forêt (référence externe). Pour l’API LDAP, cela peut se produire lors de l’exécution d’opérations d’ajout, de modification, de suppression ou de recherche qui spécifient un objet qui existe dans un autre domaine de la forêt (référence interne) ou un contexte de nommage complètement distinct de la forêt (référence externe).

    Si la résolution de noms ne parvient pas à trouver un objet localement et qu’il n’y a pas d’objets **crossRef** pour cette partie de l’espace de noms, le contrôleur de domaine tente de construire une référence externe en fonction des composants de domaine du nom unique. Par exemple, si une recherche est basée sur « CN = a, CN = b, DC = c, DC = d, DC = e », le contrôleur de domaine crée une référence au serveur LDAP à l’adresse DNS « c. d. e ».

    tous les contrôleurs de domaine Windows 2000 (qui prennent uniquement en charge DC = naming pour les composants supérieurs) se reconnaissent mutuellement, et aucune référence croisée externe n’est requise pour qu’un client se lie d’une forêt à une autre. si d’autres serveurs d’annuaire non-Windows 2000, tels qu’un serveur Netscape, utilisent DC = naming et possède un enregistrement de ressource SRV approprié enregistré dans DNS, il bénéficiera également des références automatiques. Si ce n’est pas le cas, un objet **crossRef** externe doit être ajouté manuellement.

-   Exécution d’une recherche de sous-arborescence sur un domaine qui contient des domaines subordonnés dans la forêt ou dans des conteneurs de domaines, de schémas ou de configurations secondaires subordonnés. Une référence au domaine subordonné, au domaine externe, au schéma ou au conteneur de configuration sera créée. Si le repérage de références est activé, la référence est transparente pour l’appelant.

 

 