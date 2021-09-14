---
description: Les fonctions SetNamedSecurityInfo et SetSecurityInfo prennent en charge la propagation automatique des entrées de contrôle d’accès (ACE) pouvant être héritées.
ms.assetid: 0aa49b9b-13e3-4ef9-921d-ea47a013e5a1
title: Propagation automatique des ACE pouvant être héritées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fab03c73a1c926468e46a0d0492e512dab42af6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118930"
---
# <a name="automatic-propagation-of-inheritable-aces"></a>Propagation automatique des ACE pouvant être héritées

Les fonctions [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) et [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) prennent en charge la propagation automatique des [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) pouvant être héritées. Par exemple, si vous utilisez ces fonctions pour ajouter une entrée du contrôle d’accès (ACE) héritable à un répertoire dans un système de fichiers NTFS, le système applique l’ACE en fonction des [*listes de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL) des sous-répertoires ou des fichiers existants.

Les ACE directement appliquées ont priorité sur les ACE héritées. Le système implémente cette priorité en plaçant les entrées de contrôle d’accès appliquées directement à l’avance dans une liste de contrôle d’accès discrétionnaire (DACL, [*Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ). Quand vous appelez les fonctions [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) et [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) pour définir les informations de sécurité d’un objet, le système impose le modèle d’héritage actuel sur les listes de contrôle d’accès de tous les objets de la hiérarchie sous l’objet cible. pour les objets qui ont été convertis dans le modèle d’héritage actuel, les SE \_ liste \_ \_ de contrôle d’accès discrétionnaire automatique héritée et SE \_ \_ \_ bits hérités automatiquement sont définis dans le champ de contrôle du [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) de l’objet.

Quand vous générez un nouveau descripteur de sécurité qui reflète le modèle d’héritage actuel, il est pris soin de ne pas modifier la sémantique du descripteur de sécurité. Par conséquent, les ACE allow et Deny ne sont jamais déplacées les unes par rapport aux autres. Si un tel mouvement est nécessaire (par exemple, pour placer toutes les entrées de contrôle d’accès non héritées au début d’une liste de contrôle d’accès), la liste de contrôle d’accès est marquée comme protégée pour empêcher la modification sémantique.

Le système utilise les règles suivantes lors de la propagation des ACE héritées aux objets enfants :

-   Si un objet enfant sans DACL hérite d’un ACE, le résultat est un objet enfant avec une liste DACL qui contient uniquement l’entrée du contrôle d’accès hérité.
-   Si un objet enfant avec une liste DACL vide hérite d’un ACE, le résultat est un objet enfant avec une liste DACL qui contient uniquement l’entrée du contrôle d’accès héritée.
-   Si vous supprimez une entrée du contrôle d’accès héritée d’un objet parent, l’héritage automatique supprime toutes les copies de l’entrée du contrôle d’accès héritées par les objets enfants.
-   Si l’héritage automatique entraîne la suppression de toutes les entrées de requête de la liste DACL d’un objet enfant, l’objet enfant a une DACL vide plutôt qu’aucune liste DACL.

Ces règles peuvent entraîner le résultat inattendu de la conversion d’un objet sans DACL en objet avec une liste DACL vide. Un objet sans DACL autorise un accès complet, mais un objet avec une liste DACL vide n’autorise aucun accès. En guise d’exemple de la façon dont ces règles peuvent créer une liste DACL vide, supposez que vous ajoutez une entrée de contrôle d’accès héritable à l’objet racine d’une arborescence d’objets. L’héritage automatique propage l’entrée du contrôle d’accès héritable à tous les objets de l’arborescence. Les objets enfants démarrés sans DACL disposent désormais d’une liste DACL avec l’entrée du contrôle d’accès hérité. Si vous supprimez l’entrée du contrôle d’accès héritable de l’objet racine, le système propage automatiquement la modification aux objets enfants. Les objets enfants qui ont démarré sans DACL (autorisant l’accès complet) disposent désormais d’une liste DACL vide (n’autorisant aucun accès).

pour garantir qu’un objet enfant sans dacl n’est pas affecté par les ace pouvant être héritées, définissez le SE \_ \_ indicateur dacl protected dans le descripteur de sécurité de l’objet.

Pour plus d’informations sur la création correcte d’une liste DACL, consultez [création d’une liste DACL](/windows/desktop/SecBP/creating-a-dacl).

 

 
