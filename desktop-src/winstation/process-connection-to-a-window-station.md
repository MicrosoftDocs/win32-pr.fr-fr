---
title: Traiter la connexion à une station Windows
description: Un processus établit automatiquement une connexion à une station de travail et à un bureau lorsqu’il appelle pour la première fois une fonction USER32 ou GDI32 (autre que la station de travail et les fonctions de bureau).
ms.assetid: 280f69e7-5c99-41a7-94e3-da13deaac9f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a87e97b19ac1210b04447652268c5f53b7e2a6d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382376"
---
# <a name="process-connection-to-a-window-station"></a>Traiter la connexion à une station Windows

Un processus établit automatiquement une connexion à une station de travail et à un bureau lorsqu’il appelle pour la première fois une fonction USER32 ou GDI32 (autre que la station de travail et les fonctions de bureau). Le système détermine la station de fenêtre à laquelle un processus se connecte conformément aux règles suivantes :

1.  Si le processus a appelé la fonction [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) , il se connecte à la station Windows spécifiée dans cet appel.
2.  Si le processus n’a pas appelé [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation), il se connecte à la station Windows héritée du processus parent.
3.  Si le processus n’a pas appelé [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) et n’a pas hérité de station Windows, le système tente d’ouvrir pour un maximum d' \_ accès autorisé et se connecte à une station Windows comme suit :
    -   Si un nom de station Windows a été spécifié dans le membre **lpDesktop** de la structure [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) qui a été utilisée lors de la création du processus, le processus se connecte à la station Windows spécifiée.
    -   Dans le cas contraire, si le processus est en cours d’exécution dans la session d’ouverture de session de l’utilisateur interactif, le processus se connecte à la station Windows Interactive.
    -   Si le processus s’exécute dans une session de connexion non interactive, le nom de la station Windows est formé en fonction de l’identificateur de session d’ouverture de session et une tentative est effectuée pour ouvrir cette station Windows. Si l’opération d’ouverture échoue parce que cette station Windows n’existe pas, le système essaie de créer la station Windows et un bureau par défaut.

La station de fenêtre affectée pendant ce processus de connexion ne peut pas être fermée en appelant la fonction [**CloseWindowStation**](/windows/win32/api/winuser/nf-winuser-closewindowstation) .

Lorsqu’un processus se connecte à une station Windows, le système recherche les descripteurs hérités dans la table de handles du processus. Le système utilise le premier handle de station Windows qu’il trouve. Si vous souhaitez qu’un processus enfant se connecte à une station de fenêtre héritée particulière, vous devez vous assurer que seul le handle souhaité est marqué comme pouvant être hérité. Si un processus enfant hérite de plusieurs descripteurs de station de fenêtre, les résultats de la connexion de la station Windows ne sont pas définis.

Handles d’une station Windows ouverte par le système lors de la connexion d’un processus à une station Windows ne peuvent pas être hérités.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Connexion de thread à un bureau](thread-connection-to-a-desktop.md)
</dt> </dl>

 

 