---
description: Avant d’implémenter le code qui protège les mots de passe, il est préférable d’analyser votre environnement particulier pour les raisons pour lesquelles un attaquant peut tenter de pénétrer dans les défenses logicielles.
ms.assetid: 4ebf7185-0179-4754-80da-63b0002c883f
title: Évaluation des menaces par mot de passe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9042efa524b0503a648a195e77669b19231fec0445c4b0c8347b802b323076
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977149"
---
# <a name="password-threat-assessment"></a>Évaluation des menaces par mot de passe

Avant d’implémenter le code qui protège les mots de passe, il est préférable d’analyser votre environnement particulier pour les raisons pour lesquelles un attaquant peut tenter de pénétrer dans les défenses logicielles.

Commencez par analyser l’architecture de votre réseau ou de votre système. Voici quelques exemples :

-   Le nombre de mots de passe qui doivent être protégés. Un mot de passe est-il requis pour ouvrir une session sur l’ordinateur local ? Le mot de passe utilisé pour se connecter au réseau est-il le même ? Les mots de passe sont-ils propagés à plusieurs serveurs sur le réseau ? Combien de mots de passe doivent être pris en charge ?
-   Type de réseau (le cas échéant) qui sera utilisé. Le réseau est-il implémenté à l’aide d’un système d’annuaire d’entreprise (par exemple, LDAP) et l’architecture de son mot de passe est-elle utilisée ? Tout objet stocke-t-il des mots de passe non chiffrés ?
-   Réseau ouvert et fermé. Le réseau est-il autonome ou est-il ouvert à l’extérieur ? Dans ce cas, est-il protégé par un pare-feu ?
-   Accès à distance. Les utilisateurs auront-ils besoin d’accéder au réseau à partir d’un emplacement distant ?

Après avoir analysé votre architecture système ou réseau, vous pouvez commencer à analyser la manière dont une personne malveillante peut tenter de l’attaquer. Voici quelques possibilités :

-   Lecture d’un mot de passe non chiffré à partir du registre d’un ordinateur.
-   Lire un mot de passe non chiffré qui est codé en dur dans le logiciel.
-   Lire un mot de passe non chiffré à partir de la page de codes de permutation d’un ordinateur.
-   Lire un mot de passe dans le journal des événements d’un programme.
-   Lire un mot de passe à partir d’un schéma de service d’annuaire Microsoft Active Directory étendu qui contient des objets qui contiennent un mot de passe en texte clair.
-   Exécutez un débogueur sur un programme qui requiert un mot de passe.
-   Deviner un mot de passe. L’une des différentes techniques peut être utilisée. Par exemple, l’attaquant peut connaître certaines informations personnelles sur un utilisateur et tenter de deviner un mot de passe à partir de ces informations (par exemple, le nom d’un conjoint, d’un partenaire ou d’un enfant). Ou bien, une méthode de force brute peut être tentée, où toutes les combinaisons de lettres, de chiffres et de signes de ponctuation sont essayées (uniquement possible lorsque des mots de passe courts sont utilisés).

La comparaison des méthodes d’attaque possibles avec l’architecture système ou réseau révélera probablement des risques de sécurité. À ce stade, un facteur de risque peut être établi pour chaque risque, et les facteurs de risque peuvent être utilisés pour trier les correctifs.

 

 



