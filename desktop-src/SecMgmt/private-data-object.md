---
description: Un nombre limité d’objets de données privés est disponible sur chaque système dans le but de stocker des informations de façon protégée et chiffrée.
ms.assetid: 927473d7-b5bc-4b6f-b303-8a0f8680731d
title: Objet de données privées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481f3641a7195c68a2955cc2cf302e25aa0b5a48a1ef901bec4e056ee536b375
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118893678"
---
# <a name="private-data-object"></a>Objet de données privées

Un nombre limité d’objets de données privés est disponible sur chaque système dans le but de stocker des informations de façon protégée et chiffrée.

Les objets de données privés sont fournis principalement pour prendre en charge le stockage des mots de passe de compte de serveur. Cela est utile pour les serveurs qui s’exécutent dans un compte spécifique. Le mot de passe du compte de serveur est une donnée privée qui doit être sécurisée, mais qui est nécessaire pour la connexion au serveur.

Les objets de données privés peuvent être à usage général, ou ils peuvent être de l’un des trois types spécialisés suivants : local, global et machine.

Les objets de données privés locaux peuvent uniquement être lus localement à partir de l’ordinateur qui stocke l’objet. Toute tentative de lecture à distance entraîne une erreur d' \_ accès \_ refusé. Les objets de données privées locales ont des noms de clés qui commencent par le préfixe « L $ ». En plus des objets privés locaux que vous créez, le système d’exploitation définit les objets privés locaux suivants : $machine. ACC, SAC, SAI et SANSC.

Les objets de données privés globaux sont globaux dans la mesure où s’ils sont créés sur un contrôleur de domaine, ils seront automatiquement répliqués sur tous les contrôleurs de domaine de ce domaine. En d’autres termes, chaque contrôleur de domaine de ce domaine aura accès aux valeurs contenues dans l’objet de données privées global. En revanche, les objets de données privés globaux créés sur un système qui n’est pas un contrôleur de domaine, ainsi que les objets de données privés non globaux, ne sont pas répliqués. Les objets de données privés globaux ont des noms de clés commençant par « G $ ».

Les objets de données privés de l’ordinateur sont accessibles uniquement par le système d’exploitation. Ces objets ont des noms de clés qui commencent par « M $ ».

**Remarque**  Vous pouvez définir, mais vous ne pouvez pas récupérer, les objets de données privés de machine.

En plus de ces préfixes, les valeurs suivantes indiquent également des objets locaux ou d’ordinateur. Ces valeurs sont prises en charge pour la compatibilité descendante et ne doivent pas être utilisées lorsque vous créez des objets locaux ou d’ordinateur. Le nom de clé des objets de données privés locaux peut également commencer par « RasDialParms » ou « RasCredentials ». Le nom de clé pour les objets ordinateur peut également commencer par « NL $ » ou « \_ SC \_ ».

Les objets de données privés qui ne sont pas l’un des types spécialisés précédents utilisent des noms de clés qui ne commencent pas par un préfixe. Ces objets ne sont pas répliqués et peuvent être lus localement ou à distance par les applications.

 

 



