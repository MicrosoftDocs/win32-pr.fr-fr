---
title: Affinité du processeur sous WOW64
description: 32 bits Windows prend en charge un maximum de 32 processeurs. Par conséquent, les fonctions telles que GetProcessAffinityMask simulent un ordinateur avec des processeurs 32 lorsqu’ils sont appelés sous WOW64.
ms.assetid: f50a03e8-1c23-4eb0-a1ff-471c28d6b611
keywords:
- affinité du processeur 64-bit Windows programmation
- Windows de la programmation WOW64 64 bits, affinité du processeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09cfb3aaaa676bf14d8810a6d73b210236a8fba39ad8274d1e04538dd743e2b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643319"
---
# <a name="processor-affinity-under-wow64"></a>Affinité du processeur sous WOW64

32 bits Windows prend en charge un maximum de 32 processeurs. Par conséquent, les fonctions telles que [**GetProcessAffinityMask**](/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask) simulent un ordinateur avec des processeurs 32 lorsqu’ils sont appelés sous WOW64.

Le masque d’affinité est obtenu en effectuant une opération or au niveau du bit des 32 premiers bits du masque avec les 32 bits de poids faible. Par conséquent, si un thread a une affinité pour les processeurs 0, 1 et 32, WOW64 signale l’affinité de 0 à 1, car le processeur 32 est mappé au processeur 0. Les fonctions qui définissent l’affinité du processeur, telles que [**SetThreadAffinityMask**](/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask), limitent les processeurs aux 32 premiers processeurs sous WOW64.

Pour plus d’informations sur l’affinité du processeur, consultez [plusieurs processeurs](/windows/desktop/ProcThread/multiple-processors).

 

 