---
title: Modèle de réplication du programmeur dans Active Directory Domain Services
description: Vous trouverez ci-dessous une description du modèle de réplication pour Active Directory Domain Services.
ms.assetid: 45baf7ff-9474-4f86-81c8-03336901fec2
ms.tgt_platform: multiple
keywords:
- Modèle de programmeur d’Active Directory de réplication Active Directory
- Modèle de réplication du programmeur dans Active Directory Domain Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ada20bc07411528eaea4b7ff8c773c50ae8b6ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028517"
---
# <a name="a-programmers-model-of-replication-in-active-directory-domain-services"></a>Modèle de réplication du programmeur dans Active Directory Domain Services

Vous trouverez ci-dessous une description du modèle de réplication pour Active Directory Domain Services.

Toutes les mises à jour du contrôleur de domaine Active Directory sont effectuées à l’aide de requêtes LDAP qui créent, modifient ou suppriment un objet pour chaque demande. Une requête unique peut définir ou modifier plusieurs attributs sur un objet.

Une demande de mise à jour est traitée comme une transaction atomique sur un contrôleur de périphérique. Soit la totalité de la mise à jour a lieu, soit aucune ne l’est. Si le demandeur reçoit une réponse correcte à une demande de mise à jour, la totalité de la demande a réussi (validée). C’est ce que l’on appelle une « écriture d’origine ». Plusieurs requêtes LDAP ne peuvent pas être regroupées en une seule transaction plus grande.

Dans une écriture d’origine, un contrôleur de périphérique calcule un « tampon » pour chaque valeur d’attribut nouvelle ou modifiée, et joint ce marqueur à la valeur. ainsi, lorsque la valeur est répliquée, le tampon est également répliqué. Le nouveau tampon est unique et, dans le cas d’une mise à jour, le nouveau tampon est plus grand que l’estampille sur l’ancienne valeur de ce contrôleur de périphérique.

Parfois, un contrôleur de périphérique sélectionne l’ensemble des objets qui ont été modifiés depuis la dernière réplication du contrôleur de l’objet. Ensuite, pour chaque objet, il envoie un seul message à tous les autres contrôleurs de service qui contiennent toutes les valeurs actuelles des attributs modifiés depuis la dernière réplication de l’objet. Les messages de réplication sont fiables et sont remis dans l’ordre, mais ils peuvent nécessiter plus de temps pour être remis.

Lorsqu’un contrôleur de périphérique reçoit un message de réplication d’un autre contrôleur de périphérique, il le traite comme suit : pour chaque attribut modifié, si le tampon sur la valeur dans le message de réplication est plus grand que le marqueur sur la valeur actuelle, le contrôleur de service applique la mise à jour ; dans le cas contraire, le contrôleur de réseau ignore la mise à jour. Chaque message de réplication est appliqué comme une transaction atomique, tout comme une écriture d’origine.

Il s’agit du modèle de réplication Active Directory Domain Services. Les propriétés clés de ce modèle sont les suivantes :

-   Une écriture d’origine dans un objet unique est atomique.
-   Lors de la réplication des modifications, toutes les modifications apportées par une écriture d’origine sont envoyées ou aucune d’entre elles n’est.
-   Une écriture répliquée sur un objet unique est atomique, mais les conflits sont résolus par attribut.

Le modèle ne garantit pas l’ordre de réplication des modifications apportées aux différents objets. N’écrivez pas d’applications qui partent du principe que les modifications sont répliquées dans l’ordre d’origine des écritures. Le modèle ne garantit pas que si un attribut d’un objet est modifié deux fois, les deux valeurs sont répliquées ; La réplication envoie uniquement la valeur actuelle au moment de la réplication.

Le modèle diffère de la réalité de plusieurs façons qui affectent uniquement les performances. Par exemple, le serveur Active Directory envoie des messages de réplication contenant les modifications apportées à plusieurs objets, mais traite le contenu d’un tel message à plusieurs objets comme s’il s’agissait d’une série de messages à un seul objet. Le serveur Active Directory n’effectue pas la réplication point à point comme décrit dans le modèle, mais effectue plutôt une réplication transitive plus complexe et plus efficace qui est fonctionnellement équivalente au modèle.

 

 




