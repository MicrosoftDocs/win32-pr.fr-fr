---
description: La classe CMsgThread est une classe Worker thread qui met en file d’attente les demandes au thread de mise en file d’attente pour une exécution asynchrone.
ms.assetid: 57e50abf-c90d-4c8f-afd8-25f29b6a0376
title: CMsgThread, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread
api_type:
- COM
api_location: ''
ms.openlocfilehash: 021683808900a7265f4708dae0bb29ff6d07f6619430ed5687eb77d5e2332a3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813699"
---
# <a name="cmsgthread-class"></a>CMsgThread, classe

La `CMsgThread` classe est une classe de thread de travail qui met en file d’attente les demandes au thread de mise en file d’attente pour une exécution asynchrone. Pour utiliser cette classe, dérivez votre classe de celle-ci et substituez la fonction membre [**CMsgThread :: ThreadMessageProc**](cmsgthread-threadmessageproc.md) . La fonction membre **ThreadMessageProc** effectue chaque requête. Vos fonctions client et la fonction membre **ThreadMessageProc** doivent partager une définition commune des paramètres dans l’objet [**CMsg**](cmsg.md) .

Un mécanisme négocié indique au thread de travail de se fermer. En règle générale, il s’agit d’une valeur du code de message **uMsg** de la classe [**CMsg**](cmsg.md) .

Il est judicieux d’envoyer ce message à partir du destructeur de votre classe dérivée, et d’appeler la fonction membre [**CMsgThread :: WaitForThreadExit**](cmsgthread-waitforthreadexit.md) avant de terminer la destruction de la classe dérivée.



| Membres de données protégés                                    | Description                                                                                                                           |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| m \_ hSem                                                   | Indique un descripteur utilisé pour la signalisation.                                                                                                |
| \_verrou m                                                   | Protège l’accès aux listes.                                                                                                             |
| m \_ lWaiting                                               | Indique l’attente d’un thread libre.                                                                                                  |
| m \_ ThreadQueue                                            | Remplace la fonction membre [**CMsgThread :: GetThreadMsg**](cmsgthread-getthreadmsg.md) et bloque sur d’autres éléments que cette file d’attente. |
| Fonctions de membre                                          | Description                                                                                                                           |
| [**CMsgThread**](cmsgthread-cmsgthread.md)               | Construit un objet **CMsgThread** .                                                                                                   |
| [**CreateThread**](cmsgthread-createthread.md)           | Crée un thread.                                                                                                                     |
| [**GetThreadHandle**](cmsgthread-getthreadhandle.md)     | Récupère le handle de thread.                                                                                                          |
| [**GetThreadID**](cmsgthread-getthreadid.md)             | Récupère l’identificateur du thread.                                                                                               |
| [**GetThreadPriority**](cmsgthread-getthreadpriority.md) | Récupère la priorité actuelle du thread.                                                                                                |
| [**PutThreadMsg**](cmsgthread-putthreadmsg.md)           | Met en file d’attente une demande d’exécution par le thread de travail.                                                                                  |
| [**ResumeThread**](cmsgthread-resumethread.md)           | Poursuit l’opération du thread de travail.                                                                                         |
| [**SetThreadPriority**](cmsgthread-setthreadpriority.md) | Affecte une nouvelle valeur à la priorité du thread.                                                                                       |
| [**SuspendThread**](cmsgthread-suspendthread.md)         | Interrompt l’opération d’un thread en cours d’exécution.                                                                                           |
| [**WaitForThreadExit**](cmsgthread-waitforthreadexit.md) | Bloque jusqu’à ce que le thread se termine après un appel à la fonction membre [**CMsgThread :: SuspendThread**](cmsgthread-suspendthread.md) . |
| Fonctions membres substituables                              | Description                                                                                                                           |
| [**GetThreadMsg**](cmsgthread-getthreadmsg.md)           | Récupère un objet [**CMsg**](cmsg.md) mis en file d’attente contenant une requête.                                                                  |
| [**OnThreadInit**](cmsgthread-onthreadinit.md)           | Fournit l’initialisation sur un thread.                                                                                                  |
| [**ThreadMessageProc**](cmsgthread-threadmessageproc.md) | Traite les demandes. Il s’agit d’une fonction membre virtuelle pure.                                                                           |



 

 

 



