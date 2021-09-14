---
description: Tout thread peut créer une fenêtre.
ms.assetid: 27f04f9f-52d9-46d6-8e06-9b032682b7c7
title: création d’Windows dans les threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebcde45ca37696b6dbc90e639f630a689498b04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013886"
---
# <a name="creating-windows-in-threads"></a>création d’Windows dans les threads

Tout thread peut créer une fenêtre. Le thread qui crée la fenêtre est propriétaire de la fenêtre et de sa file d’attente de messages associée. Par conséquent, le thread doit fournir une boucle de messages pour traiter les messages dans sa file d’attente de messages. En outre, vous devez utiliser [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) ou [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) dans ce thread, plutôt que les autres [fonctions Wait](/windows/desktop/Sync/wait-functions), afin qu’il puisse traiter les messages. Dans le cas contraire, le système peut devenir bloqué lorsque le thread reçoit un message alors qu’il est en attente.

La fonction [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) peut être utilisée pour permettre à un ensemble de threads de partager le même état d’entrée. En partageant l’état d’entrée, les threads partagent leur concept de fenêtre active. En procédant ainsi, un thread peut toujours activer la fenêtre d’un autre thread. Cette fonction est également utile pour partager l’état du focus, l’état de capture de la souris, l’état du clavier et l’état de l’ordre des fenêtres dans les fenêtres créées par différents threads dont l’état d’entrée est partagé.

pour plus d’informations sur la création de fenêtres, consultez [Windows des Classes](../winmsg/window-classes.md).

 

 
