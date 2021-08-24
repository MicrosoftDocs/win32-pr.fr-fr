---
title: Parcours du thread
description: Un instantané qui inclut la liste des threads contient des informations sur chaque thread de chaque processus en cours d’exécution.
ms.assetid: 2440b781-652d-4d73-b173-87504e7b49b5
keywords:
- énumérer
- énumération, threads
- threads
- threads, énumération des threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4f75f4690be05a7703dab80965fb41035da03cb21f244a4b5a9039a4a61ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513849"
---
# <a name="thread-walking"></a>Parcours du thread

Un instantané qui inclut la liste des threads contient des informations sur chaque thread de chaque processus en cours d’exécution. Vous pouvez récupérer des informations pour le premier thread de la liste à l’aide de la fonction [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) . Après avoir récupéré le premier thread de la liste, vous pouvez récupérer des informations pour les threads suivants à l’aide de la fonction [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) . **Thread32First** et **Thread32Next** remplissent une structure [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) avec des informations sur les threads individuels de l’instantané.

Vous pouvez énumérer les threads d’un processus spécifique en prenant un instantané qui comprend les threads, puis en parcourant la liste des threads, en conservant les informations sur les threads qui ont le même identificateur de processus que le processus spécifié.

Vous pouvez récupérer un code d’état d’erreur étendu pour [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) et [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) à l’aide de la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

> [!Note]  
> Le contenu du membre **th32ThreadID** de [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) est un identificateur de thread et peut être utilisé par toutes les fonctions qui requièrent un identificateur de thread.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Parcours de la liste des threads](traversing-the-thread-list.md)
</dt> </dl>

 

 