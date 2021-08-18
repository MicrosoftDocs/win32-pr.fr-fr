---
title: Mise à jour du cache de schéma
description: Toutes les informations écrites sur un serveur Active Directory sont validées par rapport au schéma.
ms.assetid: 948f8ec5-7207-4566-bd79-60cdd54231bf
ms.tgt_platform: multiple
keywords:
- Mise à jour de la publicité du cache de schéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff477ce97aab2e0e49522309d386a7e1c37b31e3b8171ef20c626fdaaa5b53a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024527"
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

 

 




