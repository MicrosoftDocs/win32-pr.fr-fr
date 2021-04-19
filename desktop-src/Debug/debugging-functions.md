---
description: Les fonctions suivantes sont utilisées avec le débogage.
ms.assetid: 95a838a2-f138-4682-b733-3f363b6c4a4b
title: Fonctions de débogage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39bf5f81b08e3a7b324f276fc1a7b5d256d40819
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516560"
---
# <a name="debugging-functions"></a>Fonctions de débogage

Les fonctions suivantes sont utilisées avec le débogage.



| Fonction                                                           | Description                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**CheckRemoteDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)   | Détermine si le processus spécifié est en cours de débogage.                         |
| [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent)                   | Permet à un débogueur de continuer un thread qui a déjà signalé un événement de débogage. |
| [**DebugActiveProcess,**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)                   | Permet à un débogueur de s’attacher à un processus actif et de le déboguer.                     |
| [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop)           | Arrête le débogueur pour déboguer le processus spécifié.                            |
| [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)                                   | Provoque l’exception d’un point d’arrêt dans le processus en cours.                      |
| [**DebugBreakProcess**](/windows/desktop/api/WinBase/nf-winbase-debugbreakprocess)                     | Provoque l’exception d’un point d’arrêt dans le processus spécifié.                    |
| [**DebugSetProcessKillOnExit**](/windows/desktop/api/WinBase/nf-winbase-debugsetprocesskillonexit)     | Définit l’action à exécuter lorsque le thread appelant se termine.                      |
| [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit)                                     | Transfère le contrôle d’exécution au débogueur.                                        |
| [**FlushInstructionCache**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushinstructioncache)             | Vide le cache d’instructions pour le processus spécifié.                            |
| [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext)                       | Récupère le contexte du thread spécifié.                                      |
| [**GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-getthreadselectorentry)           | Récupère une entrée de table de descripteur pour le sélecteur et le thread spécifiés.           |
| [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)                     | Détermine si le processus appelant est en cours de débogage par un débogueur en mode utilisateur.   |
| [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)                     | Envoie une chaîne au débogueur pour l’affichage.                                         |
| [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory)                     | Lit des données à partir d’une zone de mémoire dans un processus spécifié.                           |
| [**SetThreadContext,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)                       | Définit le contexte pour le thread spécifié.                                          |
| [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent)                     | Attend qu’un événement de débogage se produise dans un processus en cours de débogage.                   |
| [**Wow64GetThreadContext**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadcontext)             | Récupère le contexte du thread WOW64 spécifié.                                |
| [**Wow64GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadselectorentry) | Récupère une entrée de table de descripteur pour le sélecteur et le thread WOW64 spécifiés.     |
| [**Wow64SetThreadContext**](/windows/desktop/api/WinBase/nf-winbase-wow64setthreadcontext)             | Définit le contexte du thread WOW64 spécifié.                                     |
| [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory)                   | Écrit des données dans une zone de mémoire dans un processus spécifié.                            |



 

 

 
