---
description: Explique les considérations relatives à l’implémentation des fonctions d’exportation du filtre de mot de passe.
ms.assetid: ec7c1e7e-844a-43d4-b756-02bc1062d7b8
title: Considérations sur la programmation du filtre de mot de passe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9270a08c51b4b3e6b07923ad9461dc2e2dd418c3be1f1a181c07f940d71ba7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005087"
---
# <a name="password-filter-programming-considerations"></a>Considérations sur la programmation du filtre de mot de passe

Lorsque vous implémentez des fonctions d’exportation du [*filtre de mot de passe*](/windows/desktop/SecGloss/p-gly) , gardez à l’esprit les points suivants :

-   Soyez très prudent lorsque vous utilisez des mots de passe en [*texte clair*](/windows/desktop/SecGloss/p-gly) . L’envoi de mots de passe en texte clair sur des réseaux peut compromettre la sécurité. Le réseau « renifleurs » peut facilement surveiller le trafic de mot de passe en texte clair.
-   Effacez toute la mémoire utilisée pour stocker les mots de passe en appelant la fonction [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) avant de libérer de la mémoire.
-   Toutes les mémoires tampons transmises dans la notification de mot de passe et les routines de filtre doivent être traitées en lecture seule. L’écriture de données dans ces mémoires tampons peut provoquer un comportement instable.
-   Toutes les routines de filtrage et de notification de mot de passe doivent être thread-safe. Utilisez des sections critiques ou d’autres techniques de programmation synchrones pour protéger les données le cas échéant.
-   La notification et le filtrage de mot de passe s’effectuent uniquement sur l’ordinateur qui héberge le compte.
-   Tous les contrôleurs de domaine sont accessibles en écriture. par conséquent, les packages de filtre de mot de passe doivent être présents sur tous les contrôleurs de domaine.

    **Windows les domaines NT 4,0 :** La notification sur les comptes de domaine s’effectue uniquement sur le contrôleur de domaine principal. En plus du contrôleur de domaine principal, les packages de filtre de mot de passe doivent être installés sur tous les contrôleurs de domaine de sauvegarde pour permettre aux notifications de continuer en cas de modification du rôle de serveur.

-   Toutes les dll de filtre de mot de passe s’exécutent dans le [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) du compte système local.



| Pour obtenir des informations sur                                                                                                                     | Consultez                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Comment installer et inscrire votre propre dll [*de filtre de mots de passe*](/windows/desktop/SecGloss/p-gly) . | [Installation et inscription d’une DLL de filtre de mot de passe](installing-and-registering-a-password-filter-dll.md) |
| DLL de filtre de mots de passe fournie par Microsoft.                                                                                            | [Mise en œuvre des mots de passe forts et Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)         |
| Fonctions d’exportation implémentées par une DLL de filtre de mot de passe.                                                                                    | [Fonctions de filtre de mot de passe](management-functions.md)                          |



 

 

 
