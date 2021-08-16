---
description: Les applications peuvent rencontrer des problèmes lorsqu’elles sont exécutées sur des systèmes multiprocesseurs en raison d’hypothèses qu’elles rendent valides uniquement sur les systèmes à un seul processeur.
ms.assetid: b20a1d2c-b795-4ed8-ac33-539a347020c8
title: Problèmes de synchronisation et de multiprocesseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0e86a2c69cf0a0c0e56656475f73fb489f7433a94511703b3777302702bb32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886207"
---
# <a name="synchronization-and-multiprocessor-issues"></a>Problèmes de synchronisation et de multiprocesseur

Les applications peuvent rencontrer des problèmes lorsqu’elles sont exécutées sur des systèmes multiprocesseurs en raison d’hypothèses qu’elles rendent valides uniquement sur les systèmes à un seul processeur.

## <a name="thread-priorities"></a>Priorités des threads

Prenons l’exemple d’un programme avec deux threads, l’un avec une priorité plus élevée que l’autre. Sur un système à processeur unique, le thread dont la priorité est la plus élevée n’abandonne pas le contrôle au thread de priorité inférieure, car le planificateur donne la préférence aux threads de priorité plus élevée. Sur un système multiprocesseur, les deux threads peuvent s’exécuter simultanément, chacun sur son propre processeur.

Les applications doivent synchroniser l’accès aux structures de données pour éviter les conditions de concurrence. Le code qui suppose que les threads de priorité plus élevée sont exécutés sans interférence de threads de priorité inférieure échouera sur les systèmes multiprocesseurs.

## <a name="memory-ordering"></a>Ordonnancement de mémoire

Lorsqu’un processeur écrit dans un emplacement de mémoire, la valeur est mise en cache pour améliorer les performances. De même, le processeur tente de répondre aux demandes de lecture à partir du cache pour améliorer les performances. En outre, les processeurs commencent à extraire les valeurs de la mémoire avant d’être demandées par l’application. Cela peut se produire dans le cadre d’une exécution spéculative ou en raison de problèmes de ligne de cache.

Les caches de l’UC peuvent être partitionnés en banques accessibles en parallèle. Cela signifie que les opérations de mémoire peuvent être effectuées dans le désordre. Pour garantir que les opérations de mémoire sont effectuées dans l’ordre, la plupart des processeurs fournissent des instructions de barrière de mémoire. Une *barrière de mémoire complète* garantit que les opérations de lecture et d’écriture de la mémoire qui s’affichent avant l’instruction de barrière de mémoire sont validées dans la mémoire avant toute opération de lecture et d’écriture de mémoire qui s’affiche après l’instruction de barrière de mémoire. Une *barrière de lecture* de la mémoire ordonne uniquement les opérations de lecture de la mémoire et une *barrière d’écriture* de la mémoire ne commande que les opérations d’écriture de la mémoire. Ces instructions garantissent également que le compilateur désactive toutes les optimisations qui pourraient réorganiser les opérations de mémoire sur les barrières.

Les processeurs peuvent prendre en charge des instructions pour les barrières de mémoire avec les sémantiques Acquire, Release et CLOTURE. Ces sémantiques décrivent l’ordre dans lequel les résultats d’une opération sont disponibles. Avec la sémantique Acquire, les résultats de l’opération sont disponibles avant les résultats de toute opération qui s’affiche après dans le code. Avec la sémantique de version, les résultats de l’opération sont disponibles après les résultats de toute opération qui s’affiche avant dans le code. Les sémantiques de clôture combinent les sémantiques Acquire et Release. Les résultats d’une opération avec la sémantique de clôture sont disponibles avant ceux de toute opération qui s’affiche après dans le code et après ceux de toute opération qui s’affiche avant.

Sur les processeurs x86 et x64 qui prennent en charge SSE2, les instructions sont **mfence** (barrière de mémoire), **lfence** (barrière de charge) et **sfence** (clôture de magasin). Sur les processeurs ARM, les injambess sont **DMB** et **ORD**. Pour plus d’informations, consultez la documentation du processeur.

Les fonctions de synchronisation suivantes utilisent les barrières appropriées pour garantir l’ordonnancement de mémoire :

-   Fonctions qui entrent ou laissent des sections critiques
-   Fonctions qui acquièrent ou libèrent des verrous SRW
-   Début et fin de l’initialisation unique
-   **EnterSynchronizationBarrier** fonction)
-   Fonctions qui signalent des objets de synchronisation
-   Fonctions Wait
-   Fonctions verrouillées (à l’exception des fonctions avec un suffixe _nolimite_ ou des intrinsèques avec le suffixe _\_ NF_ )

## <a name="fixing-a-race-condition"></a>Correction d’une condition de concurrence critique

Le code suivant présente une condition de concurrence sur les systèmes multiprocesseurs, car le processeur qui s’exécute `CacheComputedValue` pour la première fois peut écrire `fValueHasBeenComputed` dans la mémoire principale avant `iValue` d’écrire dans la mémoire principale. Par conséquent, un deuxième processeur `FetchComputedValue` s’exécutant en même temps lit la valeur `fValueHasBeenComputed` **true**, mais la nouvelle valeur de `iValue` est toujours dans le cache du premier processeur et n’a pas été écrite dans la mémoire.

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

Cette condition de concurrence peut être réparée à l’aide du mot clé **volatile** ou de la fonction [**interlockedexchang**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) pour garantir que la valeur de `iValue` est mise à jour pour tous les processeurs avant que la valeur de `fValueHasBeenComputed` soit définie sur **true**.

à compter de Visual Studio 2005, s’il est compilé en mode **/volatile : ms** , le compilateur utilise la sémantique acquire pour les opérations de lecture sur les variables **volatiles** et les sémantiques de libération pour les opérations d’écriture sur les variables **volatiles** (lorsqu’elles sont prises en charge par l’uc). Par conséquent, vous pouvez corriger l’exemple comme suit :

``` syntax
volatile int iValue;
volatile BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

avec Visual Studio 2003, les références **volatiles** à **volatiles** sont ordonnées ; le compilateur ne réorganise pas l’accès aux variables **volatiles** . Toutefois, ces opérations peuvent être réorganisées par le processeur. Par conséquent, vous pouvez corriger l’exemple comme suit :

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          FALSE, FALSE)==FALSE) 
  {
    InterlockedExchange ((LONG*)&iValue, (LONG)ComputeValue());
    InterlockedExchange ((LONG*)&fValueHasBeenComputed, TRUE);
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          TRUE, TRUE)==TRUE) 
  {
    InterlockedExchange((LONG*)piResult, (LONG)iValue);
    return TRUE;
  } 

  else return FALSE;
}
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets de section critique](critical-section-objects.md)
</dt> <dt>

[Accès aux variables verrouillées](interlocked-variable-access.md)
</dt> <dt>

[Fonctions Wait](wait-functions.md)
</dt> </dl>

 

 



