---
description: les besoins en performances des utilisateurs et administrateurs avec les applications de sockets de Windows (Winsock).
ms.assetid: 6c4365c6-a406-497b-a313-1faeb3e3b7f5
title: 'Besoins en matière de performances : utilisateurs et administrateurs'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c74f4ec6f0a545a98a890f0bc8ff954fe43a3f79fc04fd2c2d92e68ea9f646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097669"
---
# <a name="performance-needs-users-and-administrators"></a>Besoins en matière de performances : utilisateurs et administrateurs

Les utilisateurs jugent les performances des applications en fonction de leur expérience :

-   L’application est-elle rapide à répondre ?
-   Une icône de sablier s’affiche-t-elle pendant les opérations d’arrière-plan ?
-   L’application démarre-t-elle et se ferme rapidement ?
-   Les erreurs sont-elles gérées de façon compréhensible ?

Pour résumer, les utilisateurs veulent que les applications soient rapides et prévisibles.

En revanche, les administrateurs jugent souvent les performances d’une application sur la manière dont elle utilise les ressources réseau. Les administrateurs peuvent poser les questions suivantes :

-   L’application a-t-elle une faible surcharge et une utilisation efficace du réseau ?
-   Le nombre minimal de connexions est-il utilisé pour que mon serveur puisse traiter autant d’utilisateurs à la fois que possible ?
-   Suis-je constamment appelant le support technique ?

En bref, les administrateurs veulent que les applications soient mises à l’échelle.

## <a name="best-practices-for-performance-needs"></a>Meilleures pratiques en matière de besoins en matière de performances

lors du développement d’une application Windows sockets, ces exigences en matière de performances traduisent en règles utiles.

-   Les applications réseau s’initialisent rapidement.

    L’interface utilisateur ne doit pas avoir à attendre les réponses réseau. Certaines tâches peuvent être effectuées avant que le réseau soit disponible ou sans réseau. Si le réseau ne répond pas, l’utilisateur peut avoir besoin de l’interface utilisateur pour des opérations simples, telles que la fermeture de l’application.

-   N’attendez pas que le réseau soit arrêté.

    Les applications client-serveur écrites correctement gèrent les déconnexions abandonnées de façon appropriée. N’initialisez pas une opération potentiellement longue, telle que la synchronisation de fichiers ou de dossiers avec un serveur, qui ne peut pas être interrompue lors de l’arrêt. Les réseaux ne sont pas constamment réactifs, de sorte que même les petites opérations peuvent prendre du temps. Fournir des commentaires positifs aux utilisateurs, y compris des indications de progression et des temps d’achèvement estimés.

-   Garantir une interface utilisateur réactive.

    La réactivité des applications permet d’éliminer les appels au support technique inutiles. Une bonne indication pour une réponse interactive est de 500 millisecondes. Les utilisateurs perçoivent des pauses de plus de 500 millisecondes comme un décalage des performances. Les applications doivent être suffisamment réactives pour fournir l’utilisateur en toute confiance à l’application.

-   Examinez les erreurs réseau.

    Toutes les erreurs réseau ne sont pas critiques. Par exemple, une application qui a reçu ou publié toutes ses données peut ignorer des erreurs lors de la fermeture de la connexion. Ne supposez pas que le réseau ou l’utilisateur est disponible. Gérez les erreurs sans intervention de l’utilisateur ou ignorez-les si les erreurs ne sont pas critiques.

-   Une application doit définir ses propres délais d’expiration raisonnables.

    par exemple, une demande Windows sockets connect () peut être bloquée dans certaines conditions jusqu’à 21 secondes. Les applications peuvent avoir besoin d’introduire leur propre délai d’expiration en fonction de leurs utilisateurs.

-   Réduire la charge de protocole.

    La préservation de la bande passante réseau est partiellement liée à la réduction de la charge de protocole générée par votre application. Il s’agit également d’éliminer le trafic réseau inutile. Les protocoles avec une surcharge d’en-tête inférieure peuvent être utilisés pour transférer des données d’application. Par exemple, lors de l’envoi de petites quantités de données non critiques ou reproductibles, utilisez UDP au lieu de TCP pour réduire la surcharge associée à l’établissement et à la maintenance de la connexion. Si les mêmes données doivent être envoyées à plusieurs destinataires, envisagez la multidiffusion. Sachez que les applications UDP ne sont pas contrôlées par le biais de la bande passante, ce qui peut entraîner une défaillance catastrophique du réseau. L’utilitaire Netstat peut être utilisé avec ses options **-e** et **-s** pour afficher les statistiques de différents protocoles.

-   Conserver les ressources système.

    Les ressources système peuvent être utilisées rapidement si une contrainte appropriée n’est pas utilisée. Par exemple, les sockets et les connexions TCP consomment des ressources. N’utilisez pas plusieurs connexions TCP par client où l’une d’elles servira à l’application.

Pour les applications transactionnelles, une expérience utilisateur correcte et une faible utilisation du réseau ne sont pas des objectifs conflictuels. Le réseau est un goulot d’étranglement. Les applications nécessitant beaucoup de ressources réseau consacrent plus de temps à attendre, et les applications réseau bien écrites sont conçues pour réduire le temps d’attente inutile, à la fois pour l’interface utilisateur et pour la transmission réseau.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications de sockets Windows hautes performances](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensions de performances](performance-dimensions-2.md)
</dt> </dl>

 

 



