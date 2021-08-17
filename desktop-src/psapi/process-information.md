---
title: Informations sur le processus
description: Le système gère une liste des processus en cours d’exécution. Vous pouvez récupérer les identificateurs de ces processus en appelant la fonction EnumProcesses. Cette fonction remplit un tableau de valeurs DWORD avec les identificateurs de tous les processus du système.
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5facb72f094059997c271cb9f38beaea08981430bba40902d620a23e2875b26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094890"
---
# <a name="process-information"></a>Informations sur le processus

Le système gère une liste des processus en cours d’exécution. Vous pouvez récupérer les identificateurs de ces processus en appelant la fonction [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) . Cette fonction remplit un tableau de valeurs **DWORD** avec les identificateurs de tous les processus du système.

De nombreuses fonctions dans PSAPIi requièrent un handle de processus. Pour obtenir un handle de processus pour un processus en cours d’exécution, transmettez son identificateur de processus (obtenu à partir de [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) à la fonction [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) . N’oubliez pas d’appeler la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) lorsque vous avez terminé avec le handle de processus.

 

 