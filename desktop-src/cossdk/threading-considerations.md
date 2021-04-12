---
description: Considérations relatives aux threads
ms.assetid: 4d27f0b3-3e30-4e88-b2b2-d57218da4ffa
title: Considérations relatives aux threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acde9a06802a867cb6a93e7c52be8066ad483c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033774"
---
# <a name="threading-considerations"></a>Considérations relatives aux threads

L’enregistreur de composants en file d’attente COM+ peut s’exécuter dans le cloisonnement multithread (MTA) du processus ou dans un thread cloisonné (STA). Lorsque l’enregistreur est exécuté dans le STA, COM+ requiert que chaque cloisonnement contenant des objets doive avoir une file d’attente [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) pour gérer les appels d’autres processus et Apartments au sein du même processus. Cela signifie que la fonction de travail du thread doit avoir une boucle de message. Quand un composant mis en file d’attente est instancié, le pointeur d’interface retourné est toujours un pointeur d’interface proxy plutôt qu’un pointeur d’interface directe. Le pointeur est en fait une référence à une instance de l’enregistreur. Si cette référence d’interface d’enregistreur est passée à un autre thread, le thread d’origine doit toujours exécuter la boucle de message Windows pour que le thread de réception puisse démarshaler l’interface. Si ce n’est pas le cas, le thread de réception se bloque lors d’un appel à [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).

Si vous utilisez des primitives pour synchroniser les threads, envisagez d’utiliser [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) au lieu d’autres fonctions de synchronisation. Cela recherche les messages dans la file d’attente, ainsi que l’état de l’objet de synchronisation.

 

 
