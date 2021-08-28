---
title: Liaison sans serveur et RootDSE
description: Si possible, ne codez pas en dur un nom de serveur.
ms.assetid: 24cfd8ce-18e6-42f1-8bc5-2c6dee82d133
ms.tgt_platform: multiple
keywords:
- Liaison sans serveur et RootDSE AD
- PUBLICITÉ de liaison sans serveur
- RootDSE Active Directory
- Active Directory, utilisation de, liaison, liaison sans serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a2b567ebfae52a316dce59c3bc6ab442780e61
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881227"
---
# <a name="serverless-binding-and-rootdse"></a>Liaison sans serveur et RootDSE

Si possible, ne codez pas en dur un nom de serveur. En outre, dans la plupart des cas, la liaison ne doit pas être inutilement liée à un serveur unique. Active Directory Domain Services prendre en charge la liaison sans serveur, ce qui signifie que Active Directory peut être lié à sur le domaine par défaut sans spécifier le nom d’un contrôleur de domaine. Pour les applications ordinaires, il s’agit généralement du domaine de l’utilisateur connecté. Pour les applications de service, il s’agit soit du domaine du compte d’ouverture de session du service, soit de celui du client emprunté par le service.

Dans LDAP 3,0, rootDSE est défini comme la racine de l’arborescence de données de l’annuaire sur un serveur d’annuaire. RootDSE ne fait partie d’aucun espace de noms. L’objectif de rootDSE est de fournir des données sur le serveur d’annuaire. Voici la chaîne de liaison utilisée pour effectuer une liaison à rootDSE.


```C++
LDAP://<servername>/rootDSE
```



&lt;ServerName &gt; est le nom DNS d’un serveur. Le &lt; nom de serveur &gt; est facultatif, comme indiqué dans le format suivant.


```C++
LDAP://rootDSE
```



Dans ce cas, un contrôleur de domaine par défaut du domaine dans lequel se trouve le contexte de sécurité du thread appelant sera utilisé. Si un contrôleur de domaine n’est pas accessible à l’intérieur du site, le premier contrôleur de domaine qui peut être trouvé sera utilisé.

Le rootDSE est un emplacement bien connu et fiable sur chaque serveur d’annuaire pour obtenir les noms uniques des conteneurs de domaine, de schéma et de configuration, ainsi que d’autres données sur le serveur et le contenu de l’arborescence de données de l’annuaire. Ces propriétés changent rarement sur un serveur particulier. Une application peut lire ces propriétés au démarrage et les utiliser tout au long de la session.

En résumé, une application doit utiliser une liaison sans serveur pour effectuer la liaison au répertoire sur le domaine actuel, utiliser rootDSE pour obtenir le nom unique d’un espace de noms et utiliser ce nom unique pour effectuer une liaison à des objets dans l’espace de noms.

Pour plus d’informations sur les attributs pris en charge par rootDSE, consultez [rootDSE](/windows/desktop/ADSchema/rootdse) dans la documentation du schéma Active Directory.

Pour plus d’informations et pour obtenir un exemple de code qui montre comment utiliser une liaison sans serveur et rootDSE, consultez [l’exemple de code permettant d’obtenir le nom unique du domaine](example-code-for-getting-the-distinguished-name-of-the-domain.md).

 

 
