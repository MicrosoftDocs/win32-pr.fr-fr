---
description: Les applications doivent synchroniser l’accès aux variables partagées par plusieurs threads.
ms.assetid: 729c0e68-ef52-4d6c-b771-a89043a937e6
title: Accès aux variables verrouillées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca2e083d3e3420e870ad9781b0d262df3d0786f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518798"
---
# <a name="interlocked-variable-access"></a>Accès aux variables verrouillées

Les applications doivent synchroniser l’accès aux variables partagées par plusieurs threads. Les applications doivent également s’assurer que les opérations sur ces variables sont effectuées de manière atomique (effectuées dans leur intégralité ou pas du tout.)

Les lectures et écritures simples dans des variables 32 bits correctement alignées sont des opérations atomiques. En d’autres termes, vous ne vous retrouvez pas avec une seule partie de la variable mise à jour. tous les bits sont mis à jour de manière atomique. Toutefois, la synchronisation de l’accès n’est pas garantie. Si deux threads lisent et écrivent à partir de la même variable, vous ne pouvez pas déterminer si un thread effectuera son opération de lecture avant que l’autre n’exécute son opération d’écriture.

Les lectures et écritures simples pour aligner correctement les variables 64 bits sont atomiques sur Windows 64 bits. Il n’est pas garanti que les lectures et écritures dans les valeurs 64 bits soient atomiques sur les fenêtres 32 bits. Il n’est pas garanti que les lectures et écritures dans les variables d’autres tailles soient atomiques sur les plateformes.

## <a name="the-interlocked-api"></a>API verrouillée

Les fonctions verrouillées fournissent un mécanisme simple pour synchroniser l’accès à une variable partagée par plusieurs threads. Elles effectuent également des opérations sur les variables de manière atomique. Les threads de processus différents peuvent utiliser ces fonctions si la variable est dans la mémoire partagée.

Les fonctions [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) et [**InterlockedDecrement**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement) combinent les étapes impliquées dans l’incrémentation ou la décrémentation d’une variable en une opération atomique. Cette fonctionnalité est utile dans un système d’exploitation multitâche, dans lequel le système peut interrompre l’exécution d’un thread pour accorder une tranche de temps processeur à un autre thread. Sans cette synchronisation, deux threads peuvent lire la même valeur, l’incrémenter de 1 et stocker la nouvelle valeur pour une augmentation totale de 1 au lieu de 2. Les fonctions d’accès variable interbloquées se protègent contre ce type d’erreur.

Les fonctions [**interlockedexchang**](/windows/win32/api/winnt/nf-winnt-interlockedexchange) et [**InterlockedExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedexchangepointer) échangent atomiquement les valeurs des variables spécifiées. La fonction [**InterlockedExchangeAdd**](/windows/win32/api/winnt/nf-winnt-interlockedexchangeadd) combine deux opérations : l’ajout de deux variables et le stockage du résultat dans l’une des variables.

Les fonctions [**InterlockedCompareExchange**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchange), [**InterlockedCompare64Exchange128**](/previous-versions/windows/desktop/legacy/ms683553(v=vs.85))et [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer) combinent deux opérations : la comparaison de deux valeurs et le stockage d’une troisième valeur dans l’une des variables, en fonction du résultat de la comparaison.

Les fonctions [**InterlockedAnd**](/windows/win32/api/winnt/nf-winnt-interlockedand), [**interverrouiller**](/windows/win32/api/winnt/nf-winnt-interlockedor)et [**InterlockedXor**](/windows/win32/api/winnt/nf-winnt-interlockedxor) effectuent atomiquement les opérations and, or et Xor, respectivement.

Il existe des fonctions spécifiquement conçues pour effectuer un accès variable avec verrouillage sur les valeurs et les valeurs de mémoire 64 bits, et elles sont optimisées pour une utilisation sous Windows 64 bits. Chacune de ces fonctions contient « 64 » dans le nom ; par exemple, [**InterlockedDecrement64**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement64) et [**InterlockedCompareExchangeAcquire64**](/previous-versions/windows/desktop/legacy/ms683566(v=vs.85)).

La plupart des fonctions verrouillées fournissent des barrières de mémoire complètes sur toutes les plateformes Windows. Il existe également des fonctions qui combinent les opérations d’accès aux variables interverrouillées de base avec la sémantique d’acquisition et de libération de l’ordonnancement de mémoire prise en charge par certains processeurs. Chacune de ces fonctions contient le mot « Acquire » ou « Release » dans leur nom ; par exemple, [**InterlockedDecrementAcquire**](/previous-versions/windows/desktop/legacy/ms683583(v=vs.85)) et [**InterlockedDecrementRelease**](/previous-versions/windows/desktop/legacy/ms683586(v=vs.85)). Acquérir la sémantique de mémoire spécifiez que l’opération de mémoire qui est effectuée par le thread actuel sera visible avant toute tentative d’opérations de mémoire. La sémantique de libération de mémoire spécifie que l’opération de mémoire qui est effectuée par le thread actuel sera visible une fois toutes les autres opérations de mémoire effectuées. Ces sémantiques vous permettent de forcer les opérations de mémoire à effectuer dans un ordre spécifique. Utilisez la sémantique Acquire lors de l’entrée d’une région protégée et de la sémantique de libération quand vous la quittez.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Intrinsèques du compilateur](/cpp/intrinsics/compiler-intrinsics?view=vs-2019)
</dt> <dt>

[Problèmes de synchronisation et de multiprocesseur](synchronization-and-multiprocessor-issues.md)
</dt> </dl>

 

 
