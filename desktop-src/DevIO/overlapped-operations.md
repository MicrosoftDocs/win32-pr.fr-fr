---
description: Les opérations avec chevauchement permettent à un thread d’exécuter une opération d’e/s longue en arrière-plan, ce qui laisse le thread libre d’effectuer d’autres tâches.
ms.assetid: 8c0eb20d-685a-4750-8253-a87089b68509
title: Opérations avec chevauchement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d8dc9e39386e25129d3e7d7a5281a8299d54ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483272"
---
# <a name="overlapped-operations"></a>Opérations avec chevauchement

Les opérations avec chevauchement permettent à un thread d’exécuter une opération d’e/s longue en arrière-plan, ce qui laisse le thread libre d’effectuer d’autres tâches. Pour permettre les opérations d’e/s avec chevauchement sur une ressource de communication, le thread doit spécifier l’indicateur de **\_ \_ chevauchement** de l’indicateur de fichier dans la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) lorsque le descripteur est ouvert. Pour exécuter la fonction [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) ou [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) comme une opération avec chevauchement, le thread appelant doit spécifier un pointeur vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . La structure **OVERLAPPED** doit contenir un handle vers un objet d’événement à réinitialisation manuelle (et non à une réinitialisation automatique). Le système définit l’état de l’objet d’événement sur non signalé lorsqu’un appel à la fonction d’e/s retourne une valeur avant que l’opération ne soit terminée. Le système définit l’état de l’objet d’événement comme étant signalé lorsque l’opération est terminée. Le thread utilise une fonction Wait pour vérifier l’état actuel de l’objet d’événement ou pour attendre que son état soit signalé.

Les fonctions [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) et [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) ne peuvent être exécutées qu’en tant qu’opérations avec chevauchement. Le thread appelant spécifie un pointeur vers la fonction [**FileIOCompletionRoutine**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) , qui est exécutée lorsque l’opération Overlapped est terminée. La routine d’achèvement est exécutée uniquement si le thread appelant effectue une opération d’alerte.

Pour plus d’informations sur les objets d’événement, les fonctions Wait, les attentes alertables et les routines de saisie semi-automatique, consultez [à propos de la synchronisation](/windows/desktop/Sync/about-synchronization).

 

 
