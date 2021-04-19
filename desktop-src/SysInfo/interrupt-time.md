---
description: Le temps d’interruption correspond à la durée écoulée depuis le dernier démarrage du système, en intervalles de 100 nanosecondes.
ms.assetid: 56fe322e-53ea-4186-9b5e-352f69b09109
title: Temps d’interruption
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6018d97ab0eecd1182c02b734357ca13fbe12632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529127"
---
# <a name="interrupt-time"></a><span data-ttu-id="906f7-103">Temps d’interruption</span><span class="sxs-lookup"><span data-stu-id="906f7-103">Interrupt Time</span></span>

<span data-ttu-id="906f7-104">Le *temps d’interruption* correspond à la durée écoulée depuis le dernier démarrage du système, en intervalles de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="906f7-104">*Interrupt time* is the amount of time since the system was last started, in 100-nanosecond intervals.</span></span> <span data-ttu-id="906f7-105">Le nombre de temps d’interruptions commence à zéro lorsque le système démarre et est incrémenté à chaque interruption d’horloge par la longueur d’un cycle d’horloge.</span><span class="sxs-lookup"><span data-stu-id="906f7-105">The interrupt-time count begins at zero when the system starts and is incremented at each clock interrupt by the length of a clock tick.</span></span> <span data-ttu-id="906f7-106">La longueur exacte d’un cycle d’horloge dépend du matériel sous-jacent et peut varier entre les systèmes.</span><span class="sxs-lookup"><span data-stu-id="906f7-106">The exact length of a clock tick depends on underlying hardware and can vary between systems.</span></span>

<span data-ttu-id="906f7-107">Contrairement à l' [heure système](system-time.md), le nombre d’interruptions n’est pas soumis aux ajustements des utilisateurs ou du service de temps Windows, ce qui en fait un meilleur choix pour mesurer les durées courtes.</span><span class="sxs-lookup"><span data-stu-id="906f7-107">Unlike [system time](system-time.md), the interrupt-time count is not subject to adjustments by users or the Windows time service, making it a better choice for measuring short durations.</span></span> <span data-ttu-id="906f7-108">Les applications qui requièrent une plus grande précision que le nombre d’interruptions doivent utiliser un [minuteur de haute résolution](../winmsg/about-timers.md).</span><span class="sxs-lookup"><span data-stu-id="906f7-108">Applications that require greater precision than the interrupt-time count should use a [high-resolution timer](../winmsg/about-timers.md).</span></span> <span data-ttu-id="906f7-109">Utilisez la fonction [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) pour récupérer la fréquence de la minuterie haute résolution et la fonction [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) pour récupérer la valeur du compteur.</span><span class="sxs-lookup"><span data-stu-id="906f7-109">Use the [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) function to retrieve the frequency of the high-resolution timer and the [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) function to retrieve the counter's value.</span></span>

<span data-ttu-id="906f7-110">Les fonctions [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)et [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) peuvent être utilisées pour récupérer le nombre d’interruptions.</span><span class="sxs-lookup"><span data-stu-id="906f7-110">The [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions can be used to retrieve the interrupt-time count.</span></span> <span data-ttu-id="906f7-111">L’interruption non biaisée signifie que seul le moment où le système est en état de fonctionnement est compté. par conséquent, le nombre de temps d’interruption n’est pas « biaisé » au moment où le système passe en mode veille ou veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="906f7-111">Unbiased interrupt-time means that only time that the system is in the working state is counted—therefore, the interrupt-time count is not "biased" by time the system spends in sleep or hibernation.</span></span>

<span data-ttu-id="906f7-112">**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP/2000 :** La fonction [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) est disponible à partir de Windows 7 et de windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="906f7-112">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:** The [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) function is available starting with Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="906f7-113">La résolution de l’horloge définie par les fonctions [**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) et [**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) affecte la résolution des fonctions [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) et [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) .</span><span class="sxs-lookup"><span data-stu-id="906f7-113">The timer resolution set by the [**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) functions affects the resolution of the [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) and [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) functions.</span></span> <span data-ttu-id="906f7-114">Toutefois, l’augmentation de la résolution de la minuterie n’est pas recommandée, car elle peut réduire les performances globales du système et augmenter la consommation d’énergie en empêchant le processeur de pénétrer dans des États d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="906f7-114">However, increasing the timer resolution is not recommended because it can reduce overall system performance and increase power consumption by preventing the processor from entering power-saving states.</span></span> <span data-ttu-id="906f7-115">Au lieu de cela, les applications doivent utiliser un minuteur haute résolution.</span><span class="sxs-lookup"><span data-stu-id="906f7-115">Instead, applications should use a high-resolution timer.</span></span>

> [!Note]  
> <span data-ttu-id="906f7-116">Les fonctions [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)et [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) produisent des résultats différents sur les versions Debug (« checked ») de Windows, car le nombre de temps d’interruption et le nombre de cycles sont avancés d’environ 49 jours.</span><span class="sxs-lookup"><span data-stu-id="906f7-116">The [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions produces different results on debug ("checked") builds of Windows, because the interrupt-time count and tick count are advanced by approximately 49 days.</span></span> <span data-ttu-id="906f7-117">Cela permet d’identifier les bogues qui peuvent ne pas se produire tant que le système n’a pas été exécuté pendant une longue période.</span><span class="sxs-lookup"><span data-stu-id="906f7-117">This helps to identify bugs that might not occur until the system has been running for a long time.</span></span> <span data-ttu-id="906f7-118">La version vérifiée est disponible pour les abonnés MSDN via le site Web [Microsoft Developer Network (MSDN)](https://msdn.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="906f7-118">The checked build is available to MSDN subscribers through the [Microsoft Developer Network (MSDN)](https://msdn.microsoft.com/default.aspx) Web site.</span></span>

 

<span data-ttu-id="906f7-119">L’exemple suivant montre comment récupérer le nombre de temps d’interruption en appelant les fonctions [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)et [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) .</span><span class="sxs-lookup"><span data-stu-id="906f7-119">The following example shows how to retrieve the interrupt-time count by calling the [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions.</span></span> <span data-ttu-id="906f7-120">Créez un lien vers la bibliothèque OneCore. lib lorsque vous générez une application console qui appelle ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="906f7-120">Link to the OneCore.lib library when you build a console application that calls these functions.</span></span>


```C++
#include "stdafx.h"
#include <windows.h>
#include <realtimeapiset.h>

void InterruptTimeTest()
{
    ULONGLONG InterruptTime;
    ULONGLONG PreciseInterruptTime;
    ULONGLONG UnbiasedInterruptTime;
    ULONGLONG PreciseUnbiasedInterruptTime;

        // The interrupt time that QueryInterruptTime reports is based on the 
        // latest tick of the system clock timer. The system clock timer is 
        // the hardware timer that periodically generates interrupts for the 
        // system clock. The uniform period between system clock timer 
        // interrupts is referred to as a system clock tick, and is typically 
        // in the range of 0.5 milliseconds to 15.625 milliseconds, depending 
        // on the hardware platform. The interrupt time value retrieved by 
        // QueryInterruptTime is accurate within a system clock tick.

    QueryInterruptTime(&InterruptTime);
    printf("Interrupt time: %.7f seconds\n", 
            (double)InterruptTime/(double)10000000);

        // Precise interrupt time is more precise than the interrupt time that
        // QueryInterruptTime reports because the functions that report  
        // precise interrupt time read the timer hardware directly.

    QueryInterruptTimePrecise(&PreciseInterruptTime);
    printf("Precise interrupt time: %.7f seconds\n", 
            (double)PreciseInterruptTime/(double)10000000);

        // Unbiased interrupt time means that only time that the system is in 
        // the working state is counted. Therefore, the interrupt-time count 
        // is not biased by time the system spends in sleep or hibernation.

    QueryUnbiasedInterruptTime(&UnbiasedInterruptTime);
    printf("Unbiased interrupt time: %.7f seconds\n", 
            (double)UnbiasedInterruptTime/(double)10000000);

        // QueryUnbiasedInterruptTimePrecise gets an interrupt-time count
        // that is both unbiased and precise, as defined in the comments
        // included earlier in this example.

    QueryUnbiasedInterruptTimePrecise(&PreciseUnbiasedInterruptTime);
    printf("Precise unbiased interrupt time: %.7f seconds\n", 
            (double)PreciseUnbiasedInterruptTime/(double)10000000);

}

int main(void)
{
    void InterruptTimeTime();

    InterruptTimeTest();
    return(0);
}
```



<span data-ttu-id="906f7-121">Pour récupérer le temps écoulé qui compte pour la mise en veille ou la mise en veille prolongée, utilisez la fonction [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) ou [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) , ou utilisez le compteur de performances système de temps d’activité du système.</span><span class="sxs-lookup"><span data-stu-id="906f7-121">To retrieve elapsed time that accounts for sleep or hibernation, use the [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) or [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) function, or use the System Up Time performance counter.</span></span> <span data-ttu-id="906f7-122">Ce compteur de performance peut être récupéré à partir des données de performances de la clé de Registre **HKEY \_ performance \_ Data**.</span><span class="sxs-lookup"><span data-stu-id="906f7-122">This performance counter can be retrieved from the performance data in the registry key **HKEY\_PERFORMANCE\_DATA**.</span></span> <span data-ttu-id="906f7-123">La valeur retournée est une valeur de 8 octets.</span><span class="sxs-lookup"><span data-stu-id="906f7-123">The value returned is an 8-byte value.</span></span> <span data-ttu-id="906f7-124">Pour plus d’informations, consultez [Compteurs de performances](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="906f7-124">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

## <a name="related-topics"></a><span data-ttu-id="906f7-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="906f7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="906f7-126">**QueryInterruptTime**</span><span class="sxs-lookup"><span data-stu-id="906f7-126">**QueryInterruptTime**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)
</dt> <dt>

[<span data-ttu-id="906f7-127">**QueryInterruptTimePrecise**</span><span class="sxs-lookup"><span data-stu-id="906f7-127">**QueryInterruptTimePrecise**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)
</dt> <dt>

[<span data-ttu-id="906f7-128">**QueryUnbiasedInterruptTime**</span><span class="sxs-lookup"><span data-stu-id="906f7-128">**QueryUnbiasedInterruptTime**</span></span>](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)
</dt> <dt>

[<span data-ttu-id="906f7-129">**QueryUnbiasedInterruptTimePrecise**</span><span class="sxs-lookup"><span data-stu-id="906f7-129">**QueryUnbiasedInterruptTimePrecise**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)
</dt> <dt>

[<span data-ttu-id="906f7-130">**timeBeginPeriod**</span><span class="sxs-lookup"><span data-stu-id="906f7-130">**timeBeginPeriod**</span></span>](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod)
</dt> <dt>

[<span data-ttu-id="906f7-131">**timeEndPeriod**</span><span class="sxs-lookup"><span data-stu-id="906f7-131">**timeEndPeriod**</span></span>](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod)
</dt> </dl>

 

 
