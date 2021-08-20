---
description: L’autorité LSA stocke les informations de stratégie de sécurité locale dans un ensemble d’objets. Votre application peut interroger ou modifier la stratégie de sécurité locale en accédant à ces objets.
ms.assetid: c8ed5cd8-55cf-43e7-92a3-9bd17a1147a9
title: Objets de stratégie LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c6397ffb460585b9a11f03ff397ed567a503c834e3d9ab7dfd6a4e387f319cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969107"
---
# <a name="lsa-policy-objects"></a>Objets de stratégie LSA

L’autorité LSA stocke les informations de stratégie de sécurité locale dans un ensemble d’objets. Votre application peut interroger ou modifier la stratégie de sécurité locale en accédant à ces objets.

L’ensemble se compose des quatre objets suivants :

-   La [stratégie](policy-object.md) contient des informations de stratégie globale.
-   [TrustedDomain](trusteddomain-object.md) contient des informations sur un domaine approuvé.
-   Le [compte](account-object.md) contient des informations sur un compte d’utilisateur, de groupe ou de groupe local.
-   Les [données privées](private-data-object.md) contiennent des informations protégées, telles que des mots de passe de compte de serveur. Ces informations sont stockées sous forme de chaînes chiffrées.

Pour plus d’informations sur l’utilisation des fonctions de stratégie LSA pour gérer les informations stockées dans ces objets, consultez Utilisation de la [stratégie LSA](using-lsa-policy.md).

 

 



