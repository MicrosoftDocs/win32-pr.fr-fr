---
description: Pour déboguer un processus qui est déjà en cours d’exécution, le débogueur doit utiliser DebugActiveProcess avec l’identificateur de processus. Pour récupérer une liste d’identificateurs de processus, utilisez la fonction EnumProcesses ou Process32First.
ms.assetid: 2662411f-a69a-442b-a177-a27ea025bb01
title: Débogage d’un processus en cours d’exécution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f93d184907bb66a651f04a5e144e40bf5955a672
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109991"
---
# <a name="debugging-a-running-process"></a>Débogage d’un processus en cours d’exécution

Pour déboguer un processus qui est déjà en cours d’exécution, le débogueur doit utiliser [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) avec l’identificateur de processus. Pour récupérer une liste d’identificateurs de processus, utilisez la fonction [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) ou [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) .

[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) attache le débogueur au processus actif. Dans ce cas, seul le processus actif peut être débogué ; ses processus enfants ne peuvent pas. Le débogueur doit avoir un accès approprié au processus en cours d’exécution pour utiliser **DebugActiveProcess**. Pour plus d’informations sur les droits d’accès, consultez [Access Control](../secauthz/access-control.md).

Une fois que le débogueur a créé ou attaché lui-même au processus qu’il envisage de déboguer, le système notifie le débogueur de tous les événements de débogage qui se produisent dans le processus et, s’il est spécifié, dans tous les processus enfants. Pour plus d’informations sur les événements de débogage, consultez [débogage d’événements](debugging-events.md).

Pour détacher du processus en cours de débogage, le débogueur doit utiliser la fonction [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) .

 

 
