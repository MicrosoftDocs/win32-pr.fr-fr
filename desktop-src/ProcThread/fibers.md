---
description: Une fibre est une unité d’exécution qui doit être planifiée manuellement par l’application.
ms.assetid: 6283f56b-23ae-4840-abd0-2478a50c670c
title: Fibres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0383e6d207a77c621f00f358c72bb8873ecb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756561"
---
# <a name="fibers"></a>Fibres

Une *fibre* est une unité d’exécution qui doit être planifiée manuellement par l’application. Les fibres s’exécutent dans le contexte des threads qui les planifient. Chaque thread peut planifier plusieurs fibres. En général, les fibres ne fournissent pas d’avantages par rapport à une application multithread bien conçue. Toutefois, l’utilisation de fibres peut faciliter le portage des applications conçues pour planifier leurs propres threads.

Du point de vue du système, une fibre utilise l’identité du thread qui l’exécute. Par exemple, si une fibre accède au [stockage local des threads](thread-local-storage.md) (TLS), elle accède au stockage local des threads du thread qui l’exécute. En outre, si une fibre appelle la fonction [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) , le thread qui l’exécute s’arrête. Toutefois, les informations d’état associées à une fibre ne sont pas toutes les mêmes que celles associées à un thread. Les seules informations d’État conservées pour une fibre sont sa pile, un sous-ensemble de ses registres et les données de fibre fournies lors de la création de la fibre. Les registres enregistrés sont l’ensemble des registres généralement conservés dans un appel de fonction.

Les fibres ne sont pas planifiées de manière préventive. Vous planifiez une fibre en la basculant à partir d’une autre fibre. Le système planifie toujours l’exécution des threads. Lorsqu’un thread exécutant des fibres est préempté, sa fibre en cours d’exécution est préemptée, mais reste sélectionnée. La fibre sélectionnée s’exécute lorsque son thread s’exécute.

Avant de planifier la première fibre, appelez la fonction [**ConvertThreadToFiber**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiber) pour créer une zone dans laquelle enregistrer les informations d’état de la fibre. Le thread appelant est maintenant la fibre en cours d’exécution. Les informations d’État stockées pour cette fibre incluent les données fibre passées comme argument à **ConvertThreadToFiber**.

La fonction [**CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber) est utilisée pour créer une nouvelle fibre à partir d’une fibre existante ; l’appel requiert la taille de la pile, l’adresse de départ et les données de fibre. L’adresse de départ est généralement une fonction fournie par l’utilisateur, appelée fonction Fiber, qui accepte un paramètre (les données Fiber) et ne retourne pas de valeur. Si votre fonction fibre retourne, le thread qui exécute la fibre s’arrête. Pour exécuter une fibre créée avec **CreateFiber**, appelez la fonction [**SwitchToFiber**](/windows/desktop/api/WinBase/nf-winbase-switchtofiber) . Vous pouvez appeler **SwitchToFiber** avec l’adresse d’une fibre créée par un thread différent. Pour ce faire, l’adresse doit être renvoyée à l’autre thread quand elle est appelée **CreateFiber** et vous devez utiliser une synchronisation appropriée.

Une fibre peut récupérer les données de fibre en appelant la macro [**GetFiberData**](/windows/win32/api/winnt/nf-winnt-getfiberdata) . Une fibre peut récupérer l’adresse de fibre à tout moment en appelant la macro [**GetCurrentFiber**](/windows/win32/api/winnt/nf-winnt-getcurrentfiber) .

## <a name="fiber-local-storage"></a>Stockage local Fiber

Une fibre peut utiliser le *stockage local de fibres* (FLS) pour créer une copie unique d’une variable pour chaque fibre. Si aucune commutation de fibre ne se produit, FLS agit exactement comme le [stockage local des threads](thread-local-storage.md). Les fonctions FLS ([**FlsAlloc**](/windows/win32/api/fibersapi/nf-fibersapi-flsalloc), [**FlsFree**](/windows/win32/api/fibersapi/nf-fibersapi-flsfree), [**FlsGetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flsgetvalue)et [**FlsSetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flssetvalue)) manipulent les FLS associées au thread actuel. Si le thread exécute une fibre et que la fibre est basculée, le FLS est également basculé.

Pour nettoyer les données associées à une fibre, appelez la fonction [**DeleteFiber**](/windows/desktop/api/WinBase/nf-winbase-deletefiber) . Ces données incluent la pile, un sous-ensemble des registres et les données de fibre. Si la fibre en cours d’exécution appelle **DeleteFiber**, son thread appelle [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) et se termine. Toutefois, si la fibre sélectionnée d’un thread est supprimée par une fibre s’exécutant dans un autre thread, le thread avec la fibre supprimée est susceptible de se terminer anormalement, car la pile de fibres a été libérée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de fibres](using-fibers.md)
</dt> </dl>

 

 
