---
title: Affinité du processeur sous WOW64
description: Windows 32 bits prend en charge un maximum de 32 processeurs. Par conséquent, les fonctions telles que GetProcessAffinityMask simulent un ordinateur avec des processeurs 32 lorsqu’ils sont appelés sous WOW64.
ms.assetid: f50a03e8-1c23-4eb0-a1ff-471c28d6b611
keywords:
- affinité du processeur, programmation Windows 64 bits
- WOW64 64 bits, programmation Windows, affinité du processeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c60ad6cf5055737dc39abd735211c5b4ec4ab9d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728412"
---
# <a name="processor-affinity-under-wow64"></a><span data-ttu-id="b2642-106">Affinité du processeur sous WOW64</span><span class="sxs-lookup"><span data-stu-id="b2642-106">Processor Affinity Under WOW64</span></span>

<span data-ttu-id="b2642-107">Windows 32 bits prend en charge un maximum de 32 processeurs.</span><span class="sxs-lookup"><span data-stu-id="b2642-107">32-bit Windows supports a maximum of 32 processors.</span></span> <span data-ttu-id="b2642-108">Par conséquent, les fonctions telles que [**GetProcessAffinityMask**](/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask) simulent un ordinateur avec des processeurs 32 lorsqu’ils sont appelés sous WOW64.</span><span class="sxs-lookup"><span data-stu-id="b2642-108">Therefore, functions such as [**GetProcessAffinityMask**](/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask) simulate a computer with 32 processors when called under WOW64.</span></span>

<span data-ttu-id="b2642-109">Le masque d’affinité est obtenu en effectuant une opération or au niveau du bit des 32 premiers bits du masque avec les 32 bits de poids faible.</span><span class="sxs-lookup"><span data-stu-id="b2642-109">The affinity mask is obtained by performing a bitwise OR operation of the top 32 bits of the mask with the low 32 bits.</span></span> <span data-ttu-id="b2642-110">Par conséquent, si un thread a une affinité pour les processeurs 0, 1 et 32, WOW64 signale l’affinité de 0 à 1, car le processeur 32 est mappé au processeur 0.</span><span class="sxs-lookup"><span data-stu-id="b2642-110">Therefore, if a thread has affinity for processors 0, 1, and 32, WOW64 reports the affinity as 0 and 1, because processor 32 maps to processor 0.</span></span> <span data-ttu-id="b2642-111">Les fonctions qui définissent l’affinité du processeur, telles que [**SetThreadAffinityMask**](/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask), limitent les processeurs aux 32 premiers processeurs sous WOW64.</span><span class="sxs-lookup"><span data-stu-id="b2642-111">Functions that set processor affinity, such as [**SetThreadAffinityMask**](/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask), restrict processors to the first 32 processors under WOW64.</span></span>

<span data-ttu-id="b2642-112">Pour plus d’informations sur l’affinité du processeur, consultez [plusieurs processeurs](/windows/desktop/ProcThread/multiple-processors).</span><span class="sxs-lookup"><span data-stu-id="b2642-112">For more information about processor affinity, see [Multiple Processors](/windows/desktop/ProcThread/multiple-processors).</span></span>

 

 