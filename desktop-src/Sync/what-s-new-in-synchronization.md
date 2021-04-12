---
description: Windows comprend les nouveaux éléments de programmation suivants pour la synchronisation.
ms.assetid: 16cd98d2-adc5-4a14-ad39-a0c5b4cc00cc
title: Nouveautés de la synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702ba10126d9c0eeeb85462195680b074918584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203025"
---
# <a name="whats-new-in-synchronization"></a>Nouveautés de la synchronisation

Windows comprend les nouveaux éléments de programmation suivants pour la synchronisation.

## <a name="windows-8"></a>Windows 8

### <a name="new-functions"></a>Nouvelles fonctions

<dl> <dt>

[**DeleteSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier)
</dt> <dd>

Supprime une barrière de synchronisation.

</dd> <dt>

[**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

Fait en sorte que le thread appelant attende une barrière de synchronisation jusqu’à ce que le nombre maximal de threads soit entré dans le cloisonnement.

</dd> <dt>

[**GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex)
</dt> <dd>

Récupère les résultats d’une opération avec chevauchement sur le fichier spécifié, le canal nommé ou l’appareil de communication dans l’intervalle de délai d’attente spécifié. Le thread appelant peut effectuer une attente signalable.

</dd> <dt>

[**InitializeSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

Spécifie le nombre maximal de threads et le nombre de spins pour une nouvelle barrière de synchronisation.

</dd> <dt>

[**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress)
</dt> <dd>

Attend la modification de la valeur à l’adresse spécifiée.

</dd> <dt>

[**WakeByAddressAll**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall)
</dt> <dd>

Sort tous les threads en attente de la modification de la valeur d’une adresse.

</dd> <dt>

[**WakeByAddressSingle**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle)
</dt> <dd>

Sort un thread en attente de la modification de la valeur d’une adresse.

</dd> </dl>

### <a name="new-interlocked-functions"></a>Nouvelles fonctions verrouillées

<dl> <dt>

[**InterlockedAddNoFence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))
</dt> <dd>

Effectue une opération d’addition atomique sur les valeurs **longues** spécifiées. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))
</dt> <dd>

Effectue une opération d’addition atomique sur les valeurs **LongLong** spécifiées. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedAndNoFence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))
</dt> <dd>

Effectue une opération atomique et sur les valeurs **longues** spécifiées. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))
</dt> <dd>

Effectue une opération atomique et sur les valeurs **char** spécifiées. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))
</dt> <dd>

Effectue une opération atomique et sur les valeurs **courtes** spécifiées. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))
</dt> <dd>

Effectue une opération atomique et sur les valeurs **LongLong** spécifiées. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))
</dt> <dd>

Teste le bit spécifié de la valeur **LONG64** spécifiée et le complète. L'opération est atomique.

</dd> <dt>

[**InterlockedBitTestAndResetAcquire**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))
</dt> <dd>

Teste le bit spécifié de la valeur **longue** spécifiée et lui affecte la valeur 0. L’opération est atomique et est effectuée avec la sémantique d’acquisition de mémoire acquise.

</dd> <dt>

[**InterlockedBitTestAndResetRelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))
</dt> <dd>

Teste le bit spécifié de la valeur **longue** spécifiée et lui affecte la valeur 0. L’opération est atomique et est effectuée à l’aide de la sémantique de libération de mémoire.

</dd> <dt>

[**InterlockedBitTestAndSetAcquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))
</dt> <dd>

Teste le bit spécifié de la valeur **longue** spécifiée et lui affecte la valeur 1. L’opération est atomique et est effectuée avec la sémantique d’acquisition de mémoire acquise.

</dd> <dt>

[**InterlockedBitTestAndSetRelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))
</dt> <dd>

Teste le bit spécifié de la valeur **longue** spécifiée et lui affecte la valeur 1. L’opération est atomique et est effectuée avec la sémantique d’ordonnancement de mémoire de version.

</dd> <dt>

[**InterlockedCompareExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))
</dt> <dd>

Effectue une opération atomique de comparaison et d’échange sur les valeurs spécifiées. La fonction compare deux valeurs 32 bits spécifiées et échange avec une autre valeur 32 bits en fonction du résultat de la comparaison. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedCompareExchange16**](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange16)
</dt> <dd>

Effectue une opération atomique de comparaison et d’échange sur les valeurs spécifiées. La fonction compare deux valeurs 16 bits spécifiées et échange avec une autre valeur de 16 bits en fonction du résultat de la comparaison.

</dd> <dt>

[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))
</dt> <dd>

Effectue une opération atomique de comparaison et d’échange sur les valeurs spécifiées. La fonction compare deux valeurs 16 bits spécifiées et échange avec une autre valeur de 16 bits en fonction du résultat de la comparaison. L’opération est effectuée avec la sémantique d’acquisition de mémoire acquise.

</dd> <dt>

[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))
</dt> <dd>

Effectue une opération atomique de comparaison et d’échange sur les valeurs spécifiées. La fonction compare deux valeurs 16 bits spécifiées et échange avec une autre valeur de 16 bits en fonction du résultat de la comparaison. L’échange est effectué avec la sémantique d’ordonnancement de mémoire de version.

</dd> <dt>

[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))
</dt> <dd>

Effectue une opération atomique de comparaison et d’échange sur les valeurs spécifiées. La fonction compare deux valeurs 16 bits spécifiées et échange avec une autre valeur de 16 bits en fonction du résultat de la comparaison. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))
</dt> <dd>

Effectue une opération atomique de comparaison et d’échange sur les valeurs spécifiées. La fonction compare deux valeurs 64 bits spécifiées et échange avec une autre valeur 64 bits en fonction du résultat de la comparaison. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedCompareExchange128**](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange128)
</dt> <dd>

Effectue une opération atomique de comparaison et d’échange sur les valeurs spécifiées. La fonction compare deux valeurs 128 bits spécifiées et échange avec une autre valeur 128 bits en fonction du résultat de la comparaison.

</dd> <dt>

[**InterlockedCompareExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))
</dt> <dd>

Effectue une opération atomique de comparaison et d’échange sur les valeurs spécifiées. La fonction compare deux valeurs de pointeur spécifiées et échange avec une autre valeur de pointeur en fonction du résultat de la comparaison. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedDecrementNoFence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))
</dt> <dd>

Décrémente (réduit d’une unité) la valeur de la variable 32 bits spécifiée comme une opération atomique. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedDecrement16**](/windows/desktop/api/Winnt/nf-winnt-interlockeddecrement16)
</dt> <dd>

Décrémente (réduit d’une unité) la valeur de la variable 16 bits spécifiée comme une opération atomique.

</dd> <dt>

[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))
</dt> <dd>

Décrémente (réduit d’une unité) la valeur de la variable 16 bits spécifiée comme une opération atomique. L’opération est effectuée avec la sémantique d’acquisition de mémoire acquise.

</dd> <dt>

[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))
</dt> <dd>

Décrémente (réduit d’une unité) la valeur de la variable 16 bits spécifiée comme une opération atomique. L’opération est effectuée avec la sémantique d’ordonnancement de mémoire de version.

</dd> <dt>

[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))
</dt> <dd>

Décrémente (réduit d’une unité) la valeur de la variable 16 bits spécifiée comme une opération atomique. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))
</dt> <dd>

Décrémente (réduit d’une unité) la valeur de la variable 64 bits spécifiée comme une opération atomique. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))
</dt> <dd>

Affecte à une variable 64 bits la valeur spécifiée sous la forme d’une opération atomique. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedExchange8**](/windows/desktop/api/Winnt/nf-winnt-interlockedexchange8)
</dt> <dd>

Définit une variable 8 bits à la valeur spécifiée comme une opération atomique.

</dd> <dt>

[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))
</dt> <dd>

Définit une variable de 16 bits à la valeur spécifiée comme une opération atomique. L’opération est effectuée à l’aide d’une sémantique d’ordonnancement de mémoire.

</dd> <dt>

[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))
</dt> <dd>

Définit une variable de 16 bits à la valeur spécifiée comme une opération atomique. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))
</dt> <dd>

Affecte à une variable 64 bits la valeur spécifiée sous la forme d’une opération atomique. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))
</dt> <dd>

Échange atomiquement une paire d’adresses. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedExchangeAddNoFence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))
</dt> <dd>

Effectue un ajout atomique de valeurs 2 32 bits. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))
</dt> <dd>

Effectue un ajout atomique de valeurs 2 64 bits. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedIncrementNoFence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))
</dt> <dd>

Incrémente (augmente d’une unité) la valeur de la variable 32 bits spécifiée comme une opération atomique. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedIncrement16**](/windows/desktop/api/Winnt/nf-winnt-interlockedincrement16)
</dt> <dd>

Incrémente (augmente d’une unité) la valeur de la variable 16 bits spécifiée comme une opération atomique.

</dd> <dt>

[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))
</dt> <dd>

Incrémente (augmente d’une unité) la valeur de la variable 16 bits spécifiée comme une opération atomique. L’opération est effectuée à l’aide d’une sémantique d’ordonnancement de mémoire.

</dd> <dt>

[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))
</dt> <dd>

Incrémente (augmente d’une unité) la valeur de la variable 16 bits spécifiée comme une opération atomique. L’opération est effectuée à l’aide de la sémantique d’ordonnancement de mémoire Release.

</dd> <dt>

[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))
</dt> <dd>

Incrémente (augmente d’une unité) la valeur de la variable 16 bits spécifiée comme une opération atomique. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))
</dt> <dd>

Incrémente (augmente d’une unité) la valeur de la variable 64 bits spécifiée comme une opération atomique. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedOrNoFence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))
</dt> <dd>

Effectue une opération atomique ou sur les valeurs **longues** spécifiées. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))
</dt> <dd>

Effectue une opération atomique ou sur les valeurs **char** spécifiées. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))
</dt> <dd>

Effectue une opération atomique ou sur les valeurs **courtes** spécifiées. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))
</dt> <dd>

Effectue une opération atomique ou sur les valeurs **LongLong** spécifiées. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedPushListSListEx**](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)
</dt> <dd>

Insère une liste à liaison unique à l’avant d’une autre liste à liaison unique. L’accès aux listes est synchronisé sur un système multiprocesseur. Cette version de la méthode n’utilise pas la Convention d’appel [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx) .

</dd> <dt>

[**InterlockedXorNoFence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))
</dt> <dd>

Effectue une opération atomique XOR sur les valeurs **longues** spécifiées. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))
</dt> <dd>

Effectue une opération Atomic XOR sur les valeurs **char** spécifiées. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))
</dt> <dd>

Effectue une opération atomique XOR sur les valeurs **courtes** spécifiées. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> <dt>

[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))
</dt> <dd>

Effectue une opération Atomic XOR sur les valeurs **LongLong** spécifiées. L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.

</dd> </dl>

## <a name="windows-7"></a>Windows 7

### <a name="new-functions"></a>Nouvelles fonctions

<dl> <dt>

[**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)
</dt> <dd>

Active le minuteur attendu spécifié et fournit des informations de contexte pour le minuteur.

</dd> <dt>

[**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)
</dt> <dd>

Tente d’acquérir un verrou SRW (Slim Reader/Writer) en mode exclusif. Si l’appel réussit, le thread appelant prend la propriété du verrou.

</dd> <dt>

[**TryAcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)
</dt> <dd>

Tente d’acquérir un verrou SRW (Slim Reader/Writer) en mode partagé. Si l’appel réussit, le thread appelant prend la propriété du verrou.

</dd> </dl>

### <a name="new-structures"></a>Nouvelles structures

<dl> <dt>

[**contexte de la raison \_**](/windows/win32/api/minwinbase/ns-minwinbase-reason_context)
</dt> <dd>

Contient les informations de contexte pour une minuterie activée avec [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex).

</dd> </dl>

 

 
