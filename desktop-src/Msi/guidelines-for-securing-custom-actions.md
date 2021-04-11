---
description: Pour aider à maintenir une installation logicielle sécurisée, respectez ces instructions lors de la création d’une action personnalisée Windows Installer.
ms.assetid: f7081b0c-bfa2-47a1-840b-28881ad97071
title: Instructions pour la sécurisation des actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119c045833b165222756702244cf65bb2225a8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203587"
---
# <a name="guidelines-for-securing-custom-actions"></a>Instructions pour la sécurisation des actions personnalisées

Le respect des indications suivantes lors de la création d’un package de Windows Installer avec des actions personnalisées vous aide à maintenir un environnement sécurisé lors de l’installation :

-   Sécurisez tous les fichiers supplémentaires écrits par votre action personnalisée.
-   Vérifiez les longueurs de mémoire tampon et la validité de toutes les données lues par votre action personnalisée. Cela comprend des propriétés qui peuvent fournir des données à votre action personnalisée, en particulier celles qui utilisent des propriétés publiques fournies par un utilisateur.
-   Ne vous fiez pas aux dll externes qui ne sont pas approuvées par le système sur toutes les plateformes sur lesquelles votre package d’installation est destiné à être exécuté.
-   Déterminez avec soin s’il faut utiliser des actions personnalisées qui utilisent des privilèges [*élevés*](e-gly.md) ou l’emprunt d’identité. Les actions personnalisées telles que « ouvrir une URL une fois l’installation terminée », « lancer le logiciel une fois l’installation terminée » ou « lancer le fichier Lisez-moi une fois l’installation terminée » ne nécessitent généralement pas de privilèges élevés pour fonctionner. Si votre action personnalisée doit s’exécuter avec des privilèges *élevés* , assurez-vous que le code d’action personnalisé protège contre les dépassements de mémoire tampon et le chargement par inadvertance de code non sécurisé. Notez que pendant la phase d’exécution de l’installation, le programme d’installation transmet les informations à un processus avec des privilèges *élevés* et exécute le script. Toutes les actions personnalisées qui s’exécutent pendant la phase d’exécution peuvent s’exécuter avec des privilèges *élevés* .
-   Rassemblez toutes les informations fournies par l’utilisateur pendant la séquence d’interface utilisateur. Ne pas inviter l’utilisateur à fournir des informations qui ne peuvent pas être définies à l’aide d’une propriété publique.
-   Si votre action personnalisée de script développe des propriétés, prenez des précautions que l’action personnalisée est sécurisée par rapport à la possibilité d’injection de script. Le script peut être enregistré en texte clair.

Voir aussi [sécurité des actions personnalisées](custom-action-security.md).

 

 



