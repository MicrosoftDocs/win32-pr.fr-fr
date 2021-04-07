---
description: L’autorité LSA stocke les informations de stratégie de sécurité locale dans un ensemble d’objets. Votre application peut interroger ou modifier la stratégie de sécurité locale en accédant à ces objets.
ms.assetid: c8ed5cd8-55cf-43e7-92a3-9bd17a1147a9
title: Objets de stratégie LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1481b6a6f49e973ecc2a2e1b53830bf22c67a77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952109"
---
# <a name="lsa-policy-objects"></a>Objets de stratégie LSA

L’autorité LSA stocke les informations de stratégie de sécurité locale dans un ensemble d’objets. Votre application peut interroger ou modifier la stratégie de sécurité locale en accédant à ces objets.

L’ensemble se compose des quatre objets suivants :

-   La [stratégie](policy-object.md) contient des informations de stratégie globale.
-   [TrustedDomain](trusteddomain-object.md) contient des informations sur un domaine approuvé.
-   Le [compte](account-object.md) contient des informations sur un compte d’utilisateur, de groupe ou de groupe local.
-   Les [données privées](private-data-object.md) contiennent des informations protégées, telles que des mots de passe de compte de serveur. Ces informations sont stockées sous forme de chaînes chiffrées.

Pour plus d’informations sur l’utilisation des fonctions de stratégie LSA pour gérer les informations stockées dans ces objets, consultez Utilisation de la [stratégie LSA](using-lsa-policy.md).

 

 



