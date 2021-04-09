---
description: Windows prend en charge les opérations d’e/s de fichier synchrones et asynchrones (avec chevauchement) sur les ressources de communication série.
ms.assetid: cee44596-ad73-4afb-b86a-744b0b46d9d5
title: Opérations de lecture et d’écriture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a26cc53dbe8c52286fe53c81202ab3828808b1aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110591"
---
# <a name="read-and-write-operations"></a>Opérations de lecture et d’écriture

Windows prend en charge les opérations d’e/s de fichier synchrones et asynchrones (avec chevauchement) sur les ressources de communication série. Les opérations avec chevauchement permettent au thread appelant d’effectuer d’autres tâches pendant que l’opération s’exécute en arrière-plan. Un thread utilise la fonction [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) ou [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) pour lire à partir d’une ressource de communication, et la fonction [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) ou [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) pour écrire dans une ressource de communication. **ReadFile** et **WriteFile** peuvent être exécutés de façon synchrone ou asynchrone. **ReadFileEx** et **WriteFileEx** peuvent être exécutés de façon asynchrone uniquement.

Le comportement de ces fonctions de lecture et d’écriture est affecté par le fait que la fonction est exécutée comme une opération avec chevauchement, si les paramètres de délai d’attente sont associés au handle et si les paramètres de contrôle de flow sont associés au descripteur.

Un thread peut également écrire dans une ressource de communication à l’aide de la fonction [**TransmitCommChar**](/windows/desktop/api/Winbase/nf-winbase-transmitcommchar) , qui transmet un caractère spécifié avant les données en attente dans la mémoire tampon de sortie. Cette fonction est utile pour transmettre un signal de haute priorité au système récepteur. La transmission du caractère de priorité élevée est toujours soumise au contrôle de transit et aux délais d’attente d’écriture, et l’opération est exécutée de façon synchrone.

Un thread peut utiliser la fonction [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) pour ignorer tous les caractères dans la mémoire tampon d’entrée ou de sortie d’un appareil. **PurgeComm** peut également terminer les opérations de lecture ou d’écriture en attente, même si les opérations n’ont pas été effectuées. Si un thread utilise **PurgeComm** pour vider une mémoire tampon de sortie, les caractères supprimés ne sont pas transmis. Pour vider la mémoire tampon de sortie tout en veillant à ce que le contenu soit transmis, un thread peut appeler la fonction [**FlushFileBuffers**](/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers) (opération synchrone). Notez, cependant, que **FlushFileBuffers** est soumis au contrôle de Flow, mais qu’il n’écrit pas d’expiration, et qu’il ne retourne pas tant que toutes les opérations d’écriture en attente n’ont pas été transmises.

 

 
