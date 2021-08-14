---
description: Microsoft fournit le \_ package d’authentification MSV1 0 pour les ouvertures de session d’ordinateur local qui ne nécessitent pas d’authentification personnalisée.
ms.assetid: 8b85588d-0a79-43af-b526-7a5fc8248f99
title: Package d’authentification MSV1_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12366ecf2ce213b1221fe310e77f9f019c859c038a47d332c8b702639662bc53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921748"
---
# <a name="msv1_0-authentication-package"></a>\_Package d’authentification MSV1 0

Microsoft fournit le \_ [*package d’authentification*](../secgloss/a-gly.md) MSV1 0 pour les ouvertures de session d’ordinateur local qui ne nécessitent pas d’authentification personnalisée. L' [*autorité de sécurité locale*](../secgloss/l-gly.md) (LSA) appelle le \_ package d’authentification MSV1 0 pour traiter les données d’ouverture de session collectées par le [*Gina*](../secgloss/g-gly.md) pour le processus d’ouverture de session [*Winlogon*](../secgloss/w-gly.md) . Le \_ package MSV1 0 vérifie la base de données Sam (Security Accounts Manager) locale pour déterminer si les données de connexion appartiennent à un [*principal de sécurité*](../secgloss/s-gly.md) valide, puis retourne le résultat de la tentative d’ouverture de session à l’autorité LSA.

MSV1 \_ 0 prend également en charge les ouvertures de session de domaine. MSV1 \_ 0 traite les ouvertures de session de domaine à l’aide de l’authentification directe, comme illustré dans le diagramme suivant.

![\-package d’authentification msv1 0](images/lsaint4.png)

Dans l’authentification directe, l’instance locale de MSV1 \_ 0 utilise le service Netlogon pour appeler l’instance de MSV1 \_ 0 en cours d’exécution sur le contrôleur de domaine. L’instance du contrôleur de domaine MSV1 \_ 0 vérifie ensuite la base de données SAM du contrôleur de domaine et retourne le résultat de l’ouverture de session à l’instance de MSV1 \_ 0 sur l’ordinateur local. La version locale de MSV1 \_ 0 transmet le résultat de l’ouverture de session à l’instance du LSA sur l’ordinateur local.

Si le contrôleur de domaine n’est pas disponible et que le LSA contient des [*informations d’identification*](../secgloss/c-gly.md) mises en cache pour l’utilisateur, l’instance locale de MSV1 \_ 0 peut authentifier l’utilisateur à l’aide des données de connexion mises en cache.

Le \_ package d’authentification MSV1 0 prend également en charge les [packages](subauthentication-packages.md)de sous-authentification. Un package de sous-authentification est une DLL qui peut remplacer une partie des critères d’authentification et de validation utilisés par le \_ package d’authentification MSV1 0.

Le \_ package d’authentification MSV1 0 définit une paire clé/valeur de chaîne [*d’informations d’identification principales*](../secgloss/p-gly.md) . La chaîne d’informations d’identification principales contient les informations d’identification dérivées des données fournies au moment de l’ouverture de session. Il comprend le nom d’utilisateur et les formes qui respectent la casse et qui ne respectent pas la casse du mot de passe de l’utilisateur.

 

 
