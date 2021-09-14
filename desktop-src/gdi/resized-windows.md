---
description: Le système modifie la taille d’une fenêtre lorsque l’utilisateur choisit des commandes de menu fenêtre, telles que taille et agrandissement, ou lorsque l’application appelle des fonctions, telles que la fonction SetWindowPos.
ms.assetid: 6f997cba-e4c9-4e27-8309-42b9892ec620
title: Windows redimensionné
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f740191f8b85038f17a687ebc547305f882383
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012463"
---
# <a name="resized-windows"></a>Windows redimensionné

Le système modifie la taille d’une fenêtre lorsque l’utilisateur choisit des commandes de menu fenêtre, telles que taille et agrandissement, ou lorsque l’application appelle des fonctions, telles que la fonction [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) . Quand une fenêtre change de taille, le système suppose que le contenu de la partie exposée précédemment dans la fenêtre n’est pas affecté et n’a pas besoin d’être redessiné. Le système invalide uniquement la partie récemment exposée de la fenêtre, ce qui permet de gagner du temps lorsque le message de [**\_ peinture WM**](wm-paint.md) éventuel est traité par l’application. Dans ce cas, **la \_ peinture WM** n’est pas générée lorsque la taille de la fenêtre est réduite.

Pour certaines fenêtres, toute modification apportée à la taille de la fenêtre invalide le contenu. Par exemple, une application Clock qui adapte la face de l’horloge pour qu’elle s’ajuste bien au sein de sa fenêtre doit redessiner l’horloge chaque fois que la fenêtre change de taille. Pour forcer le système à invalider la totalité de la zone cliente de la fenêtre lorsqu’une modification verticale, horizontale ou verticale et horizontale est effectuée, une application doit spécifier le \_ style cs VREDRAW ou cs \_ HREDRAW, ou les deux, lors de l’inscription de la classe de fenêtre. Toute fenêtre appartenant à une classe de fenêtre ayant ces styles est invalidée chaque fois que l’utilisateur ou l’application modifie la taille de la fenêtre.

 

 
