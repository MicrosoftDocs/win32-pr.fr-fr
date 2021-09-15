---
description: La longévité de IPv4 a entraîné le codage en dur de nombreuses adresses IPv4 connues, telles que les adresses de bouclage (127. x. x. x), les constantes entières telles que le bouclage inaddr \_ , entre autres.
ms.assetid: adb39f27-c219-43cd-9e86-b2d3b663c79c
title: Utilisation d’adresses IPv4 codées en dur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8205840b1c79afcaf375b81f3223a1c780cc03d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296622"
---
# <a name="use-of-hardcoded-ipv4-addresses"></a>Utilisation d’adresses IPv4 codées en dur

La longévité de IPv4 a entraîné le codage en dur de nombreuses adresses IPv4 connues, telles que les adresses de bouclage (127. x. x. x), les constantes entières telles que le bouclage inaddr \_ , entre autres. La pratique consistant à coder en dur ces adresses présente des problèmes évidents lors de la modification d’une application existante pour prendre en charge IPv6 ou la création de nouveaux programmes indépendants de la version IP.

Bonne pratique

-   La meilleure approche consiste à éviter le codage en dur des adresses.

Code pour éviter

-   Évitez d’utiliser des adresses codées en dur dans le code.

**Pour modifier votre base de code existante de IPv4 en IPv4 et IPv6-interopérabilité**

1.  Acquérir l’utilitaire *Checkv4.exe* . l’utilitaire *Checkv4.exe* est installé dans le cadre du kit de développement logiciel (SDK) de Microsoft Windows commercialisé pour Windows Vista et versions ultérieures. le SDK Windows est disponible via un abonnement MSDN et peut également être téléchargé à partir du site web de Microsoft ( https://msdn.microsoft.com) .
2.  Exécutez l’utilitaire *Checkv4.exe* sur votre code. Découvrez comment exécuter l’utilitaire *Checkv4.exe* sur vos fichiers dans la section relative à l' [utilisation de l’utilitaire Checkv4.exe](using-the-checkv4-exe-utility-2.md).
3.  L’utilitaire *Checkv4.exe* vous avertit de la présence de définitions courantes pour les adresses IPv4, telles que le bouclage inaddr \_ . Modifiez tout code qui utilise des chaînes littérales avec du code qui est indépendant de la version de protocole.
4.  Recherchez dans votre base de code des chaînes littérales potentielles, le cas échéant.

L’utilitaire *Checkv4.exe* peut vous aider à trouver des chaînes littérales courantes, mais il peut y en avoir d’autres spécifiques à votre application. Vous devez effectuer des recherches et des tests approfondis pour vous assurer que votre code base a éliminé des problèmes potentiels associés à des chaînes littérales.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide IPv6 pour les Applications Windows sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Modification des structures de données pour IPv6 Winsock appications](changing-data-structures-2.md)
</dt> <dt>

[Sockets à double pile pour les applications Winsock IPv6](dual-stack-sockets.md)
</dt> <dt>

[Appels de fonction pour les applications Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Problèmes d’interface utilisateur pour les applications Winsock IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocoles sous-jacents pour les applications Winsock IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 



