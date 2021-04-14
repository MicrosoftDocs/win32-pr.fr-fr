---
description: La gestion par le système des exceptions du mode utilisateur prend en charge les débogueurs sophistiqués.
ms.assetid: c45a7dc6-e6b2-4fc4-9522-12d96893f4c7
title: Gestion des exceptions du débogueur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6aff6d566e8798aaf4f3113ce6d8f44a3bc71ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482744"
---
# <a name="debugger-exception-handling"></a>Gestion des exceptions du débogueur

La gestion par le système des exceptions du mode utilisateur prend en charge les débogueurs sophistiqués. Si le processus dans lequel une exception se produit est débogué, le système génère un événement de débogage. Si le débogueur utilise la fonction [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) , l’événement de débogage provoque le retour de cette fonction avec un pointeur vers une structure d' [**\_ événement de débogage**](/windows/win32/api/minwinbase/ns-minwinbase-debug_event) . Cette structure contient les identificateurs de processus et de thread que le débogueur peut utiliser pour accéder à l’enregistrement de contexte du thread. La structure contient également une structure d' [**\_ \_ informations de débogage d’exception**](/windows/win32/api/minwinbase/ns-minwinbase-exception_debug_info) qui inclut une copie de l’enregistrement de l’exception.

Lorsque le système recherche un gestionnaire d’exceptions, il effectue deux tentatives pour notifier le débogueur d’un processus. La première tentative de notification fournit au débogueur la possibilité de gérer les exceptions de point d’arrêt ou d’une seule étape. C’est ce que l’on appelle *une notification de première chance*. L’utilisateur peut ensuite émettre des commandes de débogueur pour manipuler l’environnement du processus avant l’exécution des gestionnaires d’exceptions. La deuxième tentative de notification du débogueur se produit uniquement si le système ne parvient pas à trouver un gestionnaire d’exceptions basé sur des trames qui gère l’exception. C’est ce que l’on appelle la « *notification de dernière chance »*. Si le débogueur ne gère pas l’exception après la dernière notification de chance, le système met fin au processus en cours de débogage.

À chaque tentative de notification, le débogueur utilise la fonction [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) pour retourner le contrôle au système. Avant de retourner le contrôle, le débogueur peut gérer l’exception et modifier l’état du thread selon le cas, ou il peut choisir de ne pas gérer l’exception. À l’aide de **ContinueDebugEvent**, le débogueur peut indiquer qu’il a géré l’exception, auquel cas l’état de l’ordinateur est restauré et l’exécution du thread se poursuit au point où l’exception s’est produite. Le débogueur peut également indiquer qu’il n’a pas géré l’exception, ce qui amène le système à poursuivre la recherche d’un gestionnaire d’exceptions.

 

 
