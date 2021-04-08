---
description: L’authentification non interactive ne peut être utilisée qu’une fois l’authentification interactive effectuée. Pendant l’authentification non interactive, l’utilisateur n’entre pas les données d’ouverture de session, au lieu de cela, les informations d’identification précédemment établies sont utilisées.
ms.assetid: 1539cbfa-d84f-4989-8380-6cfc7c496310
title: Authentification non interactive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 658cba212403da2f970e056d7bacc1bc1bcaa559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951120"
---
# <a name="noninteractive-authentication"></a>Authentification non interactive

L’authentification non interactive ne peut être utilisée qu’une fois [l’authentification interactive](interactive-authentication.md) effectuée. Pendant l’authentification non interactive, l’utilisateur n’entre pas les [*données d’ouverture de session*](../secgloss/l-gly.md), au lieu de cela, les [*informations d’identification*](../secgloss/c-gly.md) précédemment établies sont utilisées.

L’authentification non interactive est effectuée quand une application utilise l’interface SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) et un package de sécurité pour établir une connexion réseau sécurisée. L’authentification non interactive est le mécanisme au travail quand un utilisateur se connecte à plusieurs ordinateurs sur un réseau sans avoir à entrer à nouveau les informations d’ouverture de session pour chaque ordinateur. Par exemple, si une application doit ouvrir un dossier sécurisé sur une machine distante et que l’utilisateur de l’application est déjà connecté de manière interactive à un compte de domaine, l’application ne demande pas à l’utilisateur de refournir les données de connexion. Au lieu de cela, l’application peut demander une authentification non interactive à l’aide de SSPI pour transmettre les informations de sécurité précédemment établies à un package de sécurité. Le package de sécurité utilise ensuite les fonctions LSA pour vérifier les [*informations d’identification*](../secgloss/c-gly.md). Le diagramme suivant illustre cette procédure.

![authentification non interactive](images/lsasspi2.png)

Dans le diagramme précédent, l’application cliente lance un appel à SSPI pour demander une connexion réseau authentifiée. SSPI transmet la demande du client à un package de sécurité pour traitement. Le package de sécurité authentifie l’utilisateur en appelant l' [*autorité de sécurité locale*](../secgloss/l-gly.md) (LSA) et en spécifiant un [*package d’authentification*](../secgloss/a-gly.md) et en fournissant les informations d’identification existantes de l’utilisateur.

Le résultat de l’authentification est passé du [*package d’authentification*](../secgloss/a-gly.md), du LSA au [*package de sécurité*](../secgloss/s-gly.md), et enfin à SSPI. SSPI notifie l’application cliente du résultat de la requête.

Pour plus d’informations sur SSPI, consultez [Security Support Provider Interface](sspi.md).

 

 
