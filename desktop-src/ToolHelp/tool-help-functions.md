---
title: Fonctions d’aide de l’outil
description: Répertorie les fonctions de la bibliothèque d’aide de l’outil.
ms.assetid: 83732bd6-f4cf-409d-ad17-86503d408dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f9d95598f9b48343ea9731e1a826fb147a73a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029715"
---
# <a name="tool-help-functions"></a>Fonctions d’aide de l’outil

Les fonctions suivantes font partie de la bibliothèque d’aide d’outils.



| Fonction                                                           | Description                                                                                                      |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)       | Prend un instantané des processus spécifiés, ainsi que les tas, les modules et les threads utilisés par ces processus. |
| [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)                                 | Récupère des informations sur le premier bloc d’un segment de mémoire qui a été alloué par un processus.                      |
| [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)                         | Récupère des informations sur le premier segment de mémoire qui a été alloué par un processus spécifié.                       |
| [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)                           | Récupère des informations sur le segment de mémoire suivant qui a été alloué par un processus.                                  |
| [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)                                   | Récupère des informations sur le bloc suivant d’un segment de mémoire qui a été alloué par un processus.                       |
| [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)                             | Récupère des informations sur le premier module associé à un processus.                                          |
| [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)                               | Récupère des informations sur le module suivant associé à un processus ou à un thread.                                 |
| [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first)                           | Récupère des informations sur le premier processus rencontré dans un instantané système.                                  |
| [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next)                             | Récupère des informations sur le processus suivant enregistré dans un instantané système.                                      |
| [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)                             | Récupère des informations sur le premier thread d’un processus rencontré dans un instantané système.                    |
| [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)                               | Récupère des informations sur le thread suivant d’un processus rencontré dans l’instantané de la mémoire système.            |
| [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) | Copie la mémoire allouée à un autre processus dans une mémoire tampon fournie par l’application.                                  |



 

 

 




