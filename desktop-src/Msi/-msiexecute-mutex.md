---
description: Le \_ mutex MSIExecute est défini uniquement lors du traitement de la table InstallExecuteSequence, de la table AdminExecuteSequence ou de la table AdvtExecuteSequence.
ms.assetid: 2186422d-ccb2-4f7e-8c6d-326c00e0d9a9
title: Mutex _MSIExecute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c22a9ca79e83e8593c2ee99884965acfd414ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864554"
---
# <a name="_msiexecute-mutex"></a>\_Mutex MSIExecute

Le \_ mutex MSIExecute est défini uniquement lors du traitement de la table [InstallExecuteSequence](installexecutesequence-table.md), de la table [AdminExecuteSequence](adminexecutesequence-table.md)ou de la table [AdvtExecuteSequence](advtexecutesequence-table.md).

Étant donné que deux installations ne peuvent pas être exécutées dans le même processus, une tentative d’appel de l’interface de programmation d’applications (API) du programme d’installation retourne une erreur d' \_ installation \_ déjà \_ en cours d’exécution (1618) dans deux cas :

-   Pendant que le \_ mutex MSIExecute est défini.
-   Pendant que le processus en cours traite la table [InstallUISequence](installuisequence-table.md) ou la [table AdminUISequence](adminuisequence-table.md).

Pour plus d’informations sur l’application en cours d’installation, consultez les messages de [journalisation des événements](event-logging.md) .

Dans les cas où il n’est pas pratique de retourner une erreur d' \_ installation \_ déjà en \_ cours d’exécution, vous pouvez récupérer l’état actuel du service Windows Installer avant de tenter de démarrer l’installation à l’aide de la fonction [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) . Le service Windows Installer est en cours d’exécution si la valeur du membre **dwControlsAccepted** de la structure du [**processus d' \_ état \_ du service**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) retourné est arrêt de l' **\_ acceptation \_ du service**.

**Windows Installer 2,0 :** Non pris en charge. L’utilisation de la fonction [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) pour récupérer l’état actuel du service Windows Installer requiert Windows Installer version 3,0 ou ultérieure.

 

 
