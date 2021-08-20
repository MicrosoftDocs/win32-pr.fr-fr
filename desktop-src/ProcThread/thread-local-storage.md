---
description: Avec le stockage local des threads (TLS), vous pouvez fournir des données uniques pour chaque thread auquel le processus peut accéder à l’aide d’un index global. Un thread alloue l’index, qui peut être utilisé par les autres threads pour récupérer les données uniques associées à l’index.
ms.assetid: 40df7410-64d6-4edd-8009-d9c3d2aca920
title: stockage local des threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32c1630fb5690fc3ade4d319e7787c5287b27c270a9b43e3825e547e68bd4c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792997"
---
# <a name="thread-local-storage"></a>stockage local des threads

Tous les threads d’un processus partagent son espace d’adressage virtuel. Les variables locales d’une fonction sont uniques à chaque thread qui exécute la fonction. Toutefois, les variables statiques et globales sont partagées par tous les threads dans le processus. Avec le *stockage local des threads* (TLS), vous pouvez fournir des données uniques pour chaque thread auquel le processus peut accéder à l’aide d’un index global. Un thread alloue l’index, qui peut être utilisé par les autres threads pour récupérer les données uniques associées à l’index.

La constante TLS \_ minimale \_ disponible définit le nombre minimal d’index TLS disponibles dans chaque processus. Cette valeur minimale est d’au moins 64 pour tous les systèmes. Le nombre maximal d’index par processus est de 1 088.

Lorsque les threads sont créés, le système alloue un tableau de valeurs **LPVOID** pour TLS, qui sont initialisées à la valeur null. Pour qu’un index puisse être utilisé, il doit être alloué par l’un des threads. Chaque thread stocke ses données pour un index TLS dans un *emplacement TLS* dans le tableau. Si les données associées à un index tiennent dans une valeur **LPVOID** , vous pouvez stocker les données directement dans l’emplacement TLS. Toutefois, si vous utilisez un grand nombre d’index de cette manière, il est préférable d’allouer un stockage distinct, de consolider les données et de réduire le nombre d’emplacements TLS en cours d’utilisation.

Le diagramme suivant illustre le fonctionnement du protocole TLS. Pour obtenir un exemple de code illustrant l’utilisation du stockage local des threads, consultez [utilisation du stockage local des threads](using-thread-local-storage.md).

![Diagramme illustrant le fonctionnement du processus T L S.](images/tls.png)

Le processus a deux threads, thread 1 et thread 2. Il alloue deux index pour une utilisation avec TLS, gdwTlsIndex1 et gdwTlsIndex2. Chaque thread alloue deux blocs de mémoire (un pour chaque index) dans lequel stocker les données et stocke les pointeurs vers ces blocs de mémoire dans les emplacements TLS correspondants. Pour accéder aux données associées à un index, le thread récupère le pointeur vers le bloc de mémoire à partir de l’emplacement TLS et le stocke dans la variable locale lpvData.

Il est idéal d’utiliser TLS dans une bibliothèque de liens dynamiques (DLL). Pour obtenir un exemple, consultez [utilisation du stockage local des threads dans une bibliothèque de liens dynamiques](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Stockage local des threads (Visual C++)](/cpp/parallel/thread-local-storage-tls?view=vs-2019)
</dt> <dt>

[Utilisation de TLS (Thread Local Storage)](using-thread-local-storage.md)
</dt> <dt>

[Utilisation du stockage local des threads dans une bibliothèque de liens dynamiques](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
