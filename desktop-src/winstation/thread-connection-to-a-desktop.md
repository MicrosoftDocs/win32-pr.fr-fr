---
title: Connexion de thread à un bureau
description: Une fois qu’un processus s’est connecté à une station Windows, le système affecte un bureau au thread qui effectue la connexion.
ms.assetid: 45016619-ed11-4b0c-84e3-f8662553c64d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a503390468ea5ed1771ece7a942a2d615ac6f0a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404485"
---
# <a name="thread-connection-to-a-desktop"></a>Connexion de thread à un bureau

Une fois qu’un processus s’est connecté à une station Windows, le système affecte un bureau au thread qui effectue la connexion. Le système détermine le Bureau à assigner au thread conformément aux règles suivantes :

1.  Si le thread a appelé la fonction [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) , il se connecte au bureau spécifié.
2.  Si le thread n’a pas appelé [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop), il se connecte au bureau hérité du processus parent.
3.  Si le thread n’a pas appelé [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) et n’a pas hérité de bureau, le système tente d’ouvrir pour un maximum d' \_ accès autorisé et se connecte à un bureau comme suit :
    -   Si un nom de bureau a été spécifié dans le membre **lpDesktop** de la structure [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) qui a été utilisée lors de la création du processus, le thread se connecte au bureau spécifié.
    -   Dans le cas contraire, le thread se connecte au bureau par défaut de la station Windows à laquelle le processus est connecté.

Le bureau affecté au cours de ce processus de connexion ne peut pas être fermé en appelant la fonction [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop) .

Lorsqu’un processus se connecte à un ordinateur de bureau, le système recherche les descripteurs hérités dans la table de handles du processus. Le système utilise le premier handle de bureau qu’il trouve. Si vous souhaitez qu’un processus enfant se connecte à un bureau hérité particulier, vous devez vous assurer que le seul handle souhaité est marqué comme étant pouvant être hérité. Si un processus enfant hérite de plusieurs handles de bureau, les résultats de la connexion au bureau ne sont pas définis.

Handles vers un bureau que le système ouvre lors de la connexion d’un processus à un bureau ne peuvent pas être hérités.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Traiter la connexion à une station Windows](process-connection-to-a-window-station.md)
</dt> </dl>

 

 