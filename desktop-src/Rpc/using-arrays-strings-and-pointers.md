---
title: Utilisation de tableaux, de chaînes et de pointeurs
description: Le programme Doctor (consultez \\ exemples \\ \\ du docteur RPC dans le kit de développement logiciel (SDK) de la plateforme) est un bon exemple d’application qui montre les compromis de conception impliqués dans les attributs de tableau et de chaîne.
ms.assetid: 9aea94a1-ae1f-4bd6-9dd3-146edf0b5fec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542a174b9ffd742ecf88de7231449a780be8dca9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011370"
---
# <a name="using-arrays-strings-and-pointers"></a>Utilisation de tableaux, de chaînes et de pointeurs

Le programme Doctor (consultez \\ exemples \\ \\ du docteur RPC dans le kit de développement logiciel (SDK) de la plateforme) est un bon exemple d’application qui montre les compromis de conception impliqués dans les attributs de tableau et de chaîne. Le programme Doctor est un petit exemple de version d’un programme mieux connu, Eliza, développé par l’organiseur d’intelligence artificielle Joseph Weizenbaum au MIT au MIT des années 60. Le programme imite un Therapist à l’aide de la mise en correspondance de modèle simple pour répondre à une entrée en langage naturel.

Le programme Eliza a enregistré la session suivante.



| Utilisateur                                                | Eliza                                                     |
|-----------------------------------------------------|-----------------------------------------------------------|
| Les hommes sont tous similaires.                                  | De quelle manière ?                                              |
| Ils sont toujours en cours de débogage sur un élément ou un autre. | Pouvez-vous penser à un exemple spécifique ?                      |
| Eh bien, mon Boyfriend m’a fait ici.               | Votre Boyfriend vous est venu ici.                        |
| Il me dit que j’ai appuyé sur la plupart du temps.             | Je suis désolé (e) que vous avez appuyé.                |
| C’est vrai, je suis mécontent.                            | Pensez-vous ici, vous aiderez à ne pas être mécontent ? |
| J’ai besoin d’aide ; Cela semble vraiment certain.          | Que feriez-vous pour vous si vous avez de l’aide ?           |
| Peut-être avez-vous pu apprendre à utiliser ma mère.  | En savoir plus sur votre famille.                           |
| Ma mère s’occupe de moi.                         | Qui autre dans votre famille vous prend-t-il en charge ?                |
| Mon père.                                          | Ton père.                                              |
| Vous aimez mon père de quelque manière que ce soit.                | Quelle ressemblance voyez-vous ?                              |



 

Le programme Doctor peut être fractionné en applications côté client et côté serveur. Le côté client invite le patient à entrer des informations et affiche la réponse du médecin. Le côté serveur traite l’entrée du patient et génère la réponse du médecin. Il s’agit d’un exemple classique d’une application client-serveur : le client est responsable de l’interaction de l’utilisateur tandis que le serveur gère la charge de calcul étendue. Peu de données sont passées à la fonction et retournées par celle-ci, mais comme les données peuvent nécessiter une quantité importante de traitement, le serveur les traite.

Le programme Doctor utilise un tableau de caractères pour l’entrée et retourne un autre tableau de caractères en tant que sortie. Le tableau ci-dessous répertorie quatre façons de passer des tableaux de caractères entre le client et le serveur, ainsi que les attributs et les fonctions nécessaires pour implémenter chaque approche.



| Approche                       | Attributs ou fonctions                                                                                                        |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Tableaux de caractères comptés       | \[la [taille \_ est](/windows/desktop/Midl/size-is) \] , la \[ [longueur \_ est](/windows/desktop/Midl/length-is) \] , \[ [ref](/windows/desktop/Midl/ref)\]                                         |
| Chaînes gérées par stub           | \[[chaîne](/windows/desktop/Midl/string) \] , \[ [Réf](/windows/desktop/Midl/ref) \] , [MIDL \_ \_ allouée](/windows/desktop/Midl/midl-user-allocate-1) par l’utilisateur sur le serveur                  |
| Chaînes gérées par stub           | \[[chaîne](/windows/desktop/Midl/string) \] , \[ [unique](/windows/desktop/Midl/unique) \] , [ \_ \_ attribution de l’utilisateur MIDL](/windows/desktop/Midl/midl-user-allocate-1) sur le client et le serveur |
| Fonction qui retourne une chaîne | \[[unique](/windows/desktop/Midl/unique)\]                                                                                                     |



 

Dans les contraintes associées à ces combinaisons d’attributs, il existe d’autres façons d’envoyer un tableau de caractères d’un client à un serveur et de retourner un autre tableau de caractères du serveur au client.

Les rubriques suivantes illustrent les compromis de conception entre les différentes interfaces qui peuvent gérer ces paramètres.

-   [Tableaux de caractères comptés](counted-character-arrays.md)
-   [Chaînes](strings.md)
-   [Plusieurs niveaux de pointeurs](multiple-levels-of-pointers.md)

 

 