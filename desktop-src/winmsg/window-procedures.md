---
description: Cette section traite des procédures relatives aux fenêtres. Chaque fenêtre est associée à une procédure de fenêtre qui traite tous les messages envoyés ou publiés dans toutes les fenêtres de la classe.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowprocedures.htm
title: Procédures de fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ae68ba9b64557a6dc70d5c83788b8337648a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523415"
---
# <a name="window-procedures"></a>Procédures de fenêtre

Chaque fenêtre a une procédure de fenêtre associée, c’est-à-dire une fonction qui traite tous les messages envoyés ou publiés dans toutes les fenêtres de la classe. Tous les aspects de l’apparence et du comportement d’une fenêtre dépendent de la réponse de la procédure de fenêtre à ces messages.

### <a name="in-this-section"></a>Dans cette section



| Nom                                                         | Description                                                                                                                                                                                                    |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos des procédures de fenêtre](about-window-procedures.md)       | Traite des procédures de fenêtre. Chaque fenêtre est un membre d’une classe de fenêtre particulière. La classe de fenêtre détermine la procédure de fenêtre par défaut utilisée par une fenêtre individuelle pour traiter ses messages.<br/> |
| [Utilisation des procédures de fenêtre](using-window-procedures.md)       | Explique comment effectuer les tâches suivantes associées aux procédures de fenêtre.<br/>                                                                                                                        |
| [Référence de procédure de fenêtre](window-procedure-reference.md) | Contient la référence de l’API.<br/>                                                                                                                                                                         |



 

### <a name="functions"></a>Fonctions



| Nom                                     | Description                                                                                                                                                                                                                                                                                                   |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) | Transmet les informations de message à la procédure de fenêtre spécifiée. <br/>                                                                                                                                                                                                                                     |
| [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)   | Appelle la procédure de fenêtre par défaut pour fournir le traitement par défaut pour tous les messages de fenêtre qu’une application ne traite pas. Cette fonction garantit que chaque message est traité. [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) est appelé avec les mêmes paramètres que ceux reçus par la procédure de fenêtre. <br/> |
| [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))           | Fonction définie par l’application qui traite les messages envoyés à une fenêtre. Le type **WNDPROC** définit un pointeur vers cette fonction de rappel. [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) est un espace réservé pour le nom de la fonction définie par l’application. <br/>                                                            |



 

 

 
