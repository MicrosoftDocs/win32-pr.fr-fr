---
title: Les fonctionnalités des applications de bureau sont affectées si elles ne sont pas exécutées en mode fenêtre
description: dans Windows 10, les applications Windows ne sont plus en plein écran par défaut. en revanche, elles sont affichées sous la forme d’une fenêtre et les opérations telles que la minimisation, la restauration, l’agrandissement, le redimensionnement (et toute autre opération que vous avez toujours pu effectuer à toute autre fenêtre d’application de Windows classique) sont désormais possibles.
ms.assetid: 435E85DA-008B-437E-92CB-AC105855760A
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aae44fda5847e5b86616b40ab1bf4ab8cbd206b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312801"
---
# <a name="desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode"></a>Les fonctionnalités des applications de bureau sont affectées si elles ne sont pas exécutées en mode fenêtre

dans Windows 10, les applications Windows ne sont plus en plein écran par défaut. en revanche, elles sont affichées sous la forme d’une fenêtre et les opérations telles que la minimisation, la restauration, l’agrandissement, le redimensionnement (et toute autre opération que vous avez toujours pu effectuer à toute autre fenêtre d’application de Windows classique) sont désormais possibles.

## <a name="manifestations"></a>Manifestations

La modification la plus notable est maintenant que vous pouvez atteindre des tailles arbitraires qui ne sont pas simplement la taille de l’écran/la hauteur de l’écran. Un utilisateur peut redimensionner continuellement la fenêtre de l’application à sa convenance (jusqu’à la taille minimale de la fenêtre de l’application). cela est différent de Windows 8.0 ou Windows 8.1, où le fait de redimensionner une fenêtre était une action discrète (les utilisateurs redimensionnent une miniature de la fenêtre, ce qui a entraîné le redimensionnement de la fenêtre une fois que l’utilisateur a validé l’action). Aujourd’hui, à la place, lorsque l’utilisateur fait glisser la fenêtre à l’aide du coin inférieur (ou d’un autre emplacement de bordure), il s’agit d’un redimensionnement continu, et l’application reçoit des messages de redimensionnement dans une ligne, au lieu d’une modification de la taille.

## <a name="mitigations"></a>Corrections

pour atténuer ce risque pour les applications Windows 8.0 et 8,1 :

-   Si la fonctionnalité attendue dans la fonctionnalité de l’application est rompue, l’atténuation de l’utilisateur consiste à placer l’application en mode plein écran (à l’aide du bouton « aller à l’écran complet » dans le coin supérieur droit de la barre de titre).
-   Si le démarrage de l’application est affecté qu’elle ne s’ouvre pas comme prévu, l’utilisateur doit toujours être en mesure de basculer en mode tablette pour forcer l’application à démarrer en mode plein écran sans intervention de l’utilisateur.

La meilleure façon de gérer cela consiste à modifier l’application pour qu’elle soit consciente du fait qu’elle peut être dimensionnée à des emplacements/hauteurs non monitorés (c’est-à-dire qu’elle n’a pas de table de hauteur/largeur codée en dur et qu’elle n’attende que celles-ci). Les développeurs d’applications doivent s’attendre à ce que l’application soit redimensionnée, un autre message de redimensionnement peut se produire juste après la remise du message de redimensionnement actuel. par conséquent, si l’application démarre des animations pendant le redimensionnement, il est possible que l’application puisse recevoir un autre message de redimensionnement juste après (il est donc important de s’assurer que ce type de situation n’entraîne pas le blocage de l’application).

 

 




