---
description: La fonction CreateThread crée un nouveau thread pour un processus.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Fonctions de thread pour le débogage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5ab0865d5585656a5c22c24e2604032de8b888
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523671"
---
# <a name="thread-functions-for-debugging"></a>Fonctions de thread pour le débogage

La fonction [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) crée un nouveau thread pour un processus. Les débogueurs doivent généralement examiner ou modifier le contenu des registres d’un thread. Pour ce faire, un débogueur doit obtenir un handle pour le thread à l’aide de la fonction [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) et en spécifiant l’accès approprié au thread (contexte d’obtention de thread \_ \_ , contexte de groupe de threads \_ \_ , ou les deux). La fonction [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) permet à un débogueur d’obtenir l’identificateur d’un thread existant.

Un processus avec un accès approprié à un thread peut examiner les registres du thread à l’aide de la fonction [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) et définir le contenu des registres du thread à l’aide de la fonction [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) .

Un processus peut également obtenir \_ \_ l’accès de reprise d’interruption de thread à un thread. Ce type d’accès permet à un débogueur de contrôler l’exécution d’un thread à l’aide des fonctions [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) et [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) . Pour plus d’informations sur les threads, consultez [processus et threads](../procthread/processes-and-threads.md).

 

 
