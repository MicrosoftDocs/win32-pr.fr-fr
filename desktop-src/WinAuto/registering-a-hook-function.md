---
title: Inscription d’une fonction de raccordement
description: Les applications clientes reçoivent WinEvents dans une fonction de rappel WinEventProc. Les actions effectuées par la fonction de rappel sont définies par l’application, mais la syntaxe doit être telle qu’elle est spécifiée dans le prototype.
ms.assetid: 7e999335-6a41-4d22-82ef-1a8dd6cb656e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c444d2ee291cb07386e775a649ba0c3d42486c45b70e4d3f4629b9b67274f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564649"
---
# <a name="registering-a-hook-function"></a>Inscription d’une fonction de raccordement

Les applications clientes reçoivent WinEvents dans une fonction de rappel [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) . Les actions effectuées par la fonction de rappel sont définies par l’application, mais la syntaxe doit être telle qu’elle est spécifiée dans le prototype.

Avant de pouvoir recevoir des événements, la fonction doit être inscrite en appelant [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook). Le client peut appeler **SetWinEventHook** plusieurs fois pour inscrire différentes fonctions de raccordement, ou pour définir des événements supplémentaires pour une fonction de raccordement précédemment enregistrée.

Lors de l’appel de [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) , le client spécifie les événements à recevoir et comment les recevoir. Le client peut choisir d’effectuer les opérations suivantes :

-   Recevoir tous les événements ou un ensemble spécifique d’événements.
-   Recevoir des événements de tous les threads ou d’un thread spécifique.
-   Recevoir des événements de tous les processus ou d’un processus spécifique.
-   Gérer les événements en cours de traitement ou hors processus.

Lors de la génération d’un événement qui correspond aux critères spécifiés, le système appelle la fonction de rappel [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) du client (ou « procédure de Hook »). Les paramètres que la fonction de raccordement reçoit indiquent au client la fenêtre, l’objet et l’élément enfant possible qui a généré l’événement. Un client utilise ces paramètres dans un appel de récupération d’objet, tel que [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

 

 




