---
description: Le temps d’interruption correspond à la durée écoulée depuis le dernier démarrage du système, en intervalles de 100 nanosecondes.
ms.assetid: 56fe322e-53ea-4186-9b5e-352f69b09109
title: Temps d’interruption
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6018d97ab0eecd1182c02b734357ca13fbe12632
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193720"
---
# <a name="interrupt-time"></a>Temps d’interruption

Le *temps d’interruption* correspond à la durée écoulée depuis le dernier démarrage du système, en intervalles de 100 nanosecondes. Le nombre de temps d’interruptions commence à zéro lorsque le système démarre et est incrémenté à chaque interruption d’horloge par la longueur d’un cycle d’horloge. La longueur exacte d’un cycle d’horloge dépend du matériel sous-jacent et peut varier entre les systèmes.

contrairement à l' [heure système](system-time.md), le nombre d’interruptions n’est pas soumis aux ajustements des utilisateurs ou du service de temps Windows, ce qui en fait un meilleur choix pour mesurer les durées courtes. Les applications qui requièrent une plus grande précision que le nombre d’interruptions doivent utiliser un [minuteur de haute résolution](../winmsg/about-timers.md). Utilisez la fonction [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) pour récupérer la fréquence de la minuterie haute résolution et la fonction [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) pour récupérer la valeur du compteur.

Les fonctions [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)et [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) peuvent être utilisées pour récupérer le nombre d’interruptions. L’interruption non biaisée signifie que seul le moment où le système est en état de fonctionnement est compté. par conséquent, le nombre de temps d’interruption n’est pas « biaisé » au moment où le système passe en mode veille ou veille prolongée.

**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP/2000 :** la fonction [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) est disponible à partir de Windows 7 et Windows Server 2008 R2.

La résolution de l’horloge définie par les fonctions [**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) et [**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) affecte la résolution des fonctions [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) et [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) . Toutefois, l’augmentation de la résolution de la minuterie n’est pas recommandée, car elle peut réduire les performances globales du système et augmenter la consommation d’énergie en empêchant le processeur de pénétrer dans des États d’économie d’énergie. Au lieu de cela, les applications doivent utiliser un minuteur haute résolution.

> [!Note]  
> les fonctions [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)et [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) produisent des résultats différents sur les builds de débogage (« checked ») de Windows, car le nombre de temps d’interruption et le nombre de cycles sont avancés d’environ 49 jours. Cela permet d’identifier les bogues qui peuvent ne pas se produire tant que le système n’a pas été exécuté pendant une longue période. La version vérifiée est disponible pour les abonnés MSDN via le site Web [Microsoft Developer Network (MSDN)](https://msdn.microsoft.com/default.aspx) .

 

L’exemple suivant montre comment récupérer le nombre de temps d’interruption en appelant les fonctions [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)et [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) . créez un lien vers la bibliothèque OneCore. lib lorsque vous générez une application console qui appelle ces fonctions.


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



Pour récupérer le temps écoulé qui compte pour la mise en veille ou la mise en veille prolongée, utilisez la fonction [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) ou [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) , ou utilisez le compteur de performances système de temps d’activité du système. Ce compteur de performance peut être récupéré à partir des données de performances de la clé de Registre **HKEY \_ performance \_ Data**. La valeur retournée est une valeur de 8 octets. Pour plus d’informations, consultez [Compteurs de performances](/windows/desktop/PerfCtrs/performance-counters-portal).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)
</dt> <dt>

[**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)
</dt> <dt>

[**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)
</dt> <dt>

[**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)
</dt> <dt>

[**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod)
</dt> <dt>

[**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod)
</dt> </dl>

 

 
