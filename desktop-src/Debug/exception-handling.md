---
description: Les exceptions peuvent être lancées par le matériel ou les logiciels et peuvent se produire en mode noyau et en mode utilisateur. La gestion structurée des exceptions fournit un mécanisme unique pour la gestion des exceptions en mode noyau et en mode utilisateur.
ms.assetid: 760ddcaa-a18c-4fdf-836c-9028a2e4b62e
title: Gestion des exceptions (gestion des erreurs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253776619100095ae1ba9c92fa2caa373bc950bdf6725c6ef5d0239520320bd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260869"
---
# <a name="exception-handling-error-handling"></a>Gestion des exceptions (gestion des erreurs)

Les exceptions peuvent être lancées par le matériel ou les logiciels et peuvent se produire en mode noyau et en mode utilisateur. La gestion structurée des exceptions fournit un mécanisme unique pour la gestion des exceptions en mode noyau et en mode utilisateur.

L’exécution de certaines séquences d’instructions peut entraîner des exceptions qui sont lancées par le matériel. Par exemple, une violation d’accès est générée par le matériel lorsqu’un processus tente de lire ou d’écrire sur une adresse virtuelle pour laquelle il ne dispose pas de l’accès approprié.

Les événements qui requièrent une gestion des exceptions peuvent également se produire pendant l’exécution d’une routine logicielle (par exemple, lorsqu’une valeur de paramètre non valide est spécifiée). Dans ce cas, un thread peut lancer une exception explicitement en appelant la fonction [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) . Cette fonction permet au thread appelant de spécifier des informations qui décrivent l’exception.

Une exception peut être continue ou non continue. Une exception qui ne peut pas être poursuivie se produit lorsque l’événement n’est pas continuable dans le matériel, ou si la continuation n’est pas appropriée. Une exception non continuable ne met pas fin à l’application. Par conséquent, une application peut être en mesure d’intercepter l’exception et de l’exécuter. Toutefois, une exception non viable se produit généralement à la suite d’une pile endommagée ou d’un autre problème sérieux, ce qui rend difficile la récupération à partir de l’exception.

 

 
