---
description: Une opération qui se termine de façon asynchrone effectue une partie de son traitement dans l’appel de fonction effectué par l’application et le reste de celle-ci dans un thread d’exécution indépendant après que TAPI 2. x a retourné l’appel de fonction.
ms.assetid: 37b544e4-6413-4741-b8b6-ec676ce4ca97
title: Fonctions asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 135e792a4b1d6a25a4f49fbb2abe2c19ce3071ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521830"
---
# <a name="asynchronous-functions"></a>Fonctions asynchrones

Une opération qui se termine de façon asynchrone effectue une partie de son traitement dans l’appel de fonction effectué par l’application et le reste de celle-ci dans un thread d’exécution indépendant après que TAPI 2. x a retourné l’appel de fonction. Pour garantir l’achèvement du traitement de l’appel, le fournisseur de services Vector la requête vers une autre entité active du système (par exemple, un serveur LAN, un matériel de complément, un commutateur ou un réseau), puis retourne à l’application. À ce stade, un résultat d’erreur négatif ou un identificateur de demande positif est retourné à l’application.

Au moment de la saisie semi-automatique asynchrone (le fournisseur de services a reçu une interruption du matériel, ce qui signifie qu’un message doit être remis), le fournisseur de services appelle TAPISRV et signale que «l’événement *X* vient de se produire. Remettre un message approprié à toutes les applications concernées.» Quand TAPISRV reçoit ce message, il transfère le message à la bibliothèque de liens dynamiques TAPI, dans le processus de l’application, qui à son tour publie un message de fenêtre, signale un handle d’événement ou publie sur un port de terminaison d’e/s, en fonction du schéma de notification de message sélectionné par l’application dans [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) ou [**phoneInitializeEx**](/windows/win32/api/tapi/nf-tapi-phoneinitializeexa).

Lorsque la partie asynchrone de l’opération est terminée, un message de [**\_ réponse**](./line-reply.md) à la ligne (ou à la [**\_ réponse du téléphone**](./phone-reply.md)) est envoyé à l’application. Ce message contient, comme l’un de ses paramètres, l’identificateur de demande retourné par l’appel de fonction. Cet identificateur de demande permet à l’application de déterminer la demande d’origine qui est terminée. (Les applications doivent mémoriser les identificateurs de demande de toutes leurs demandes en cours afin que les messages de réponse puissent être gérés correctement.) Un deuxième paramètre du message de réponse à la ligne \_ (ou de la \_ réponse du téléphone) est la valeur de retour asynchrone. Il s’agit d’une valeur négative (pour une erreur) ou de zéro si l’opération s’est terminée correctement. Pour les opérations asynchrones, toutes les valeurs de retour peuvent être retournées dans le cadre du retour de la fonction ou en tant que paramètre *dwParam2* dans le message de réponse de ligne \_ ou de \_ réponse téléphonique. La valeur 0, qui indique une réussite, est retournée uniquement dans le \_ message de réponse de ligne, et jamais comme valeur de retour de la fonction.

Les fonctions Initialize ( [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) et [**phoneInitializeEx**](/windows/win32/api/tapi/nf-tapi-phoneinitializeexa)) indiquent à TAPI comment envoyer ces messages à l’application.

> [!Note]  
> Dans certains cas, si une application multithread appelle une fonction asynchrone à partir d’un thread autre que le thread à partir duquel l’application a initialisé la ligne ou le périphérique téléphonique, l’application peut recevoir le message de [**\_ réponse de ligne**](./line-reply.md) ou de [**\_ réponse téléphonique**](./phone-reply.md) avant le retour de la fonction asynchrone. Dans ce cas, l’application doit enregistrer les paramètres du message et attendre le retour de la fonction asynchrone et l’identificateur de la demande est connu avant le traitement du message.

 

 

 
