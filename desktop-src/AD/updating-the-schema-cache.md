---
title: Mise à jour du cache de schéma
description: Toutes les informations écrites sur un serveur Active Directory sont validées par rapport au schéma.
ms.assetid: 948f8ec5-7207-4566-bd79-60cdd54231bf
ms.tgt_platform: multiple
keywords:
- Mise à jour de la publicité du cache de schéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bf915d00b463b81a331ffe39b342f620a50417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671210"
---
# <a name="updating-the-schema-cache"></a>Mise à jour du cache de schéma

Toutes les informations écrites sur un serveur Active Directory sont validées par rapport au schéma. Le schéma est conservé en mémoire sur les serveurs d’annuaire (contrôleurs de domaine) pour des raisons de performances. La version en mémoire est mise à jour automatiquement après la mise à jour de la version sur disque. La mise à jour automatique se produit cinq minutes après l’application de la dernière modification. l’application d’une autre modification au schéma dans la fenêtre de 5 minutes réinitialise la minuterie pendant 5 minutes. Ce comportement garantit la cohérence du cache, mais peut prêter à confusion, car les modifications n’apparaissent pas dans le schéma tant que le cache n’est pas mis à jour, même s’ils ont été appliqués sur le disque.

Pour mettre à jour le cache de schéma Active Directory après une mise à jour du schéma, ou si vous souhaitez utiliser immédiatement la mise à jour du schéma pour les opérations sans schéma, ajoutez l’attribut **schemaUpdateNow** (il s’agit d’un attribut opérationnel) au DSE racine (nom de domaine vide) avec la valeur 1. Une mise à jour du cache de schéma démarrera immédiatement. L’appel est bloquant. Si l’appel retourne sans erreur, le cache est mis à jour et toutes les mises à jour de schéma sont prêtes à être utilisées. Un retour d’erreur indique que la mise à jour du cache a échoué. Les applications qui doivent utiliser cette fonctionnalité doivent être conçues pour prendre en charge l’écriture de blocage, en particulier pour donner des commentaires à l’utilisateur, si le programme ou le script s’exécute de manière interactive.

L’exemple de code suivant est un exemple de script LDIFDE qui montre comment déclencher un rechargement du cache.

``` syntax
dn:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

Pour plus d’informations sur la mise à jour du cache de schéma par programme, consultez [l’exemple de code pour la mise à jour du cache de schéma](example-code-for-updating-the-schema-cache.md).

 

 




