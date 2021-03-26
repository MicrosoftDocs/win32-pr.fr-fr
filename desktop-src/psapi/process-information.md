---
title: Informations sur le processus
description: Le système gère une liste des processus en cours d’exécution. Vous pouvez récupérer les identificateurs de ces processus en appelant la fonction EnumProcesses. Cette fonction remplit un tableau de valeurs DWORD avec les identificateurs de tous les processus du système.
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 147debe36dd2647cd46d19a62b0374f47b73bc58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315552"
---
# <a name="process-information"></a>Informations sur le processus

Le système gère une liste des processus en cours d’exécution. Vous pouvez récupérer les identificateurs de ces processus en appelant la fonction [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) . Cette fonction remplit un tableau de valeurs **DWORD** avec les identificateurs de tous les processus du système.

De nombreuses fonctions dans PSAPIi requièrent un handle de processus. Pour obtenir un handle de processus pour un processus en cours d’exécution, transmettez son identificateur de processus (obtenu à partir de [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) à la fonction [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) . N’oubliez pas d’appeler la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) lorsque vous avez terminé avec le handle de processus.

 

 