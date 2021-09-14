---
description: Windows fournit des api que vous pouvez utiliser pour acquérir des horodatages haute résolution ou mesurer des intervalles de temps.
ms.assetid: D66E0FC2-3AF2-489B-B4B5-78648905B77B
title: Acquisition d’horodatages haute résolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9a1300967738b717ab8d8c822bf2af3f6a4a7ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217945"
---
# <a name="acquiring-high-resolution-time-stamps"></a>Acquisition d’horodatages haute résolution

Windows fournit des api que vous pouvez utiliser pour acquérir des horodatages haute résolution ou mesurer des intervalles de temps. L’API principale pour le code natif est [**QueryPerformanceCounter (QPC)**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Pour les pilotes de périphérique, l’API en mode noyau est [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter). Pour le code managé, la classe [**System. Diagnostics. chronomètre**](/previous-versions/windows/) utilise **QPC** comme heure précise.

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) est indépendant de et n’est pas synchronisé avec les références d’heure externes. Pour récupérer les horodatages qui peuvent être synchronisés avec une référence horaire externe, par exemple, le temps universel coordonné (UTC, Universal Time Coordinated) pour une utilisation dans des mesures à un moment donné dans le temps de haute résolution, utilisez [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).

Les horodatages et les mesures de l’intervalle de temps font partie intégrante des mesures de performances de l’ordinateur et du réseau. Ces opérations de mesure des performances incluent le calcul du temps de réponse, le débit et la latence, ainsi que l’exécution du code de profilage. Chacune de ces opérations implique une mesure des activités qui se produisent pendant un intervalle de temps défini par un événement de début et de fin qui peut être indépendant de toute référence au moment de la journée externe.

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) est généralement la meilleure méthode pour utiliser les événements d’horodatage et mesurer les petits intervalles de temps qui se produisent sur le même système ou la même machine virtuelle. Envisagez d’utiliser [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) lorsque vous souhaitez horodater des événements sur plusieurs ordinateurs, à condition que chaque ordinateur participe à un schéma de synchronisation horaire tel que NTP (Network Time Protocol). **QPC** vous aide à éviter les difficultés qui peuvent être rencontrées avec d’autres approches de mesure du temps, telles que la lecture directe du compteur d’horodatage du processeur (TSC).

-   [prise en charge de QPC dans les versions Windows](#qpc-support-in-windows-versions)
-   [Conseils pour l’acquisition d’horodatages](#guidance-for-acquiring-time-stamps)
    -   [Virtualisation](#virtualization)
    -   [Utilisation directe du TSC](#direct-tsc-usage)
    -   [Exemples d’acquisition d’horodatages](#examples-for-acquiring-time-stamps)
-   [FAQ générale sur QPC et TSC](#general-faq-about-qpc-and-tsc)
-   [FAQ sur la programmation avec QPC et TSC](#faq-about-programming-with-qpc-and-tsc)
-   [Caractéristiques de l’horloge matérielle de bas niveau](#low-level-hardware-clock-characteristics)
    -   [Horloges absolues et horloges de différence](#absolute-clocks-and-difference-clocks)
    -   [Résolution, précision, précision et stabilité](#resolution-precision-accuracy-and-stability)
-   [Informations sur la minuterie matérielle](#hardware-timer-info)

## <a name="qpc-support-in-windows-versions"></a>prise en charge de QPC dans les versions Windows

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) a été introduite dans Windows 2000 et Windows XP et a évolué pour tirer parti des améliorations apportées à la plate-forme matérielle et aux processeurs. ici, nous décrivons les caractéristiques de **QPC** sur différentes versions de Windows pour vous aider à gérer les logiciels qui s’exécutent sur ces versions Windows.

### <a name="windows-xp-and-windows-2000"></a>Windows XP et Windows 2000

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) est disponible sur Windows XP et Windows 2000 et fonctionne bien sur la plupart des systèmes. Toutefois, le BIOS de certains systèmes matériels n’indique pas correctement les caractéristiques de l’UC matérielle (TSC non indifférent), et certains systèmes à plusieurs cœurs ou multiprocesseurs utilisaient des processeurs avec TSCs qui n’ont pas pu être synchronisés entre les cœurs. les systèmes avec un microprogramme défectueux qui exécutent ces versions de Windows peuvent ne pas fournir la même **QPC** de lecture sur différents cœurs s’ils ont utilisé le TSC comme base pour **QPC**.

### <a name="windows-vista-and-windows-server-2008"></a>Windows Vista et Windows Server 2008

tous les ordinateurs livrés avec Windows Vista et Windows Server 2008 utilisaient un compteur de plateforme High Precision Event Timer (HPET) ou le minuteur de gestion de l’alimentation ACPI (temporisateur PM) comme base pour [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Ces minuteurs de plateforme ont une latence d’accès plus élevée que le TSC et sont partagés entre plusieurs processeurs. Cela limite l’extensibilité de **QPC** si elle est appelée simultanément à partir de plusieurs processeurs.

### <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 et Windows Server 2008 R2

la majorité des ordinateurs Windows 7 et Windows Server 2008 R2 disposent de processeurs avec TSCs à débit constant et utilisent ces compteurs comme base pour [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Les TSCs sont des compteurs matériels à haute résolution par processeur qui sont accessibles avec une latence et une surcharge très faibles (dans l’ordre des dizaines ou des centaines de cycles d’ordinateur, selon le type de processeur). Windows 7 et Windows Server 2008 R2 utilisent TSCs comme base de **QPC** sur des systèmes de domaine à une seule horloge où le système d’exploitation (ou l’hyperviseur) est en mesure de synchroniser étroitement les TSCs individuels sur tous les processeurs pendant l’initialisation du système. Sur ces systèmes, le coût de lecture du compteur de performances est nettement plus faible par rapport aux systèmes qui utilisent un compteur de plateforme. En outre, il n’existe aucune surcharge supplémentaire pour les appels simultanés et les requêtes en mode utilisateur contournent souvent des appels système, ce qui réduit encore davantage la surcharge. sur les systèmes où le TSC n’est pas adapté à la minuterie, Windows sélectionne automatiquement un compteur de plateforme (le minuteur HPET ou la minuterie ACPI PM) comme base pour **QPC**.

### <a name="windows-8-windows-81-windows-server-2012-and-windows-server-2012-r2"></a>Windows 8, Windows 8.1, Windows Server 2012 et Windows Server 2012 R2

Windows 8, Windows 8.1, Windows Server 2012 et Windows Server 2012 R2 utilisent TSCs comme base pour le compteur de performance. L’algorithme de synchronisation TSC a été considérablement amélioré pour mieux prendre en charge de grands systèmes avec de nombreux processeurs. En outre, la prise en charge de la nouvelle API précise de l’heure du jour a été ajoutée, ce qui permet d’obtenir des horodatages précis de l’horloge du système d’exploitation. Pour plus d’informations, consultez [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime). sur les plateformes pc Windows RT, le compteur de performances est basé sur un compteur de plateforme propriétaire ou sur le compteur système fourni par le minuteur générique Windows RT PC si la plateforme est équipée.

## <a name="guidance-for-acquiring-time-stamps"></a>Conseils pour l’acquisition d’horodatages

Windows a et continuera à investir dans la fourniture d’un compteur de performances fiable et efficace. Lorsque vous avez besoin d’horodatages avec une résolution de 1 microsecondes ou plus et que vous n’avez pas besoin des horodatages à synchroniser avec une référence horaire externe, choisissez [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter), [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter)ou [**KeQueryInterruptTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise). Lorsque vous avez besoin d’horodatages synchronisés UTC avec une résolution de 1 microsecondes ou plus, choisissez [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) ou [**KeQuerySystemTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequerysystemtimeprecise).

Sur un nombre relativement faible de plateformes qui ne peuvent pas utiliser le registre TSC comme base [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) , par exemple, pour des raisons expliquées dans informations sur la [minuterie matérielle](#hardware-timer-info), l’acquisition d’horodatages haute résolution peut être considérablement plus coûteuse que l’acquisition d’horodatages avec une résolution inférieure. Si la résolution de 10 à 16 millisecondes est suffisante, vous pouvez utiliser [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64), [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), [**KeQueryInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttime)ou [**KeQueryUnbiasedInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryunbiasedinterrupttime) pour obtenir des horodatages qui ne sont pas synchronisés avec une référence horaire externe. Pour les horodatages synchronisés en UTC, utilisez [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) ou [**KeQuerySystemTime**](/windows-hardware/drivers/ddi/wdm/nf-wdm-kequerysystemtime~r1). Si vous avez besoin d’une résolution supérieure, vous pouvez utiliser [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)ou [**KeQueryInterruptTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise) pour obtenir des horodatages à la place.

En général, les résultats des compteurs de performances sont cohérents sur tous les processeurs des systèmes multicœurs et multiprocesseurs, même s’ils sont mesurés sur différents threads ou processus. Voici quelques exceptions à cette règle :

-   les systèmes d’exploitation antérieurs à Windows Vista qui s’exécutent sur certains processeurs peuvent violer cette cohérence pour l’une des raisons suivantes :

    -   Les processeurs matériels ont un TSC non indifférent et le BIOS n’indique pas correctement cette condition.
    -   L’algorithme de synchronisation TSC utilisé n’était pas adapté aux systèmes avec un grand nombre de processeurs.

-   Lorsque vous comparez les résultats des compteurs de performance obtenus à partir de différents threads, envisagez des valeurs qui diffèrent par un battement de ± 1 pour avoir un classement ambigu. Si les horodatages sont tirés du même thread, cette incertitude de l’intervalle ± 1 ne s’applique pas. Dans ce contexte, le terme « Tick » fait référence à un laps de temps égal à 1 ÷ (fréquence du compteur de performance obtenu de [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)).

quand vous utilisez le compteur de performances sur des systèmes de serveur de grande taille avec des domaines à plusieurs horloges qui ne sont pas synchronisés dans le matériel, Windows détermine que le TSC ne peut pas être utilisé à des fins de synchronisation et sélectionne un compteur de plateforme comme base pour [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Bien que ce scénario produise toujours des horodatages fiables, la latence d’accès et l’évolutivité sont affectées. Par conséquent, comme indiqué précédemment dans les instructions d’utilisation précédentes, utilisez uniquement les API qui fournissent 1 microseconde ou une meilleure résolution lorsque cette résolution est nécessaire. Le TSC est utilisé comme base pour les **QPC** sur des systèmes de domaine à plusieurs horloges qui incluent la synchronisation matérielle de tous les domaines d’horloge de processeur, car cela leur fait fonctionner en tant que système de domaine à horloge unique.

La fréquence du compteur de performances est fixée au démarrage du système et est cohérente sur tous les processeurs. vous devez donc uniquement interroger la fréquence à partir de [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) à mesure que l’application est initialisée, puis mettre en cache le résultat.

### <a name="virtualization"></a>Virtualisation

Le compteur de performances est censé fonctionner de manière fiable sur toutes les machines virtuelles invitées s’exécutant sur des hyperviseurs correctement implémentés. Toutefois, les hyperviseurs qui sont conformes à l’interface de la version 1,0 de l’hyperviseur et qui surveillent l’indisponibilité du temps de référence peuvent offrir une surcharge nettement inférieure. Pour plus d’informations sur les interfaces d’hyperviseur et les indications, consultez spécifications de l' [hyperviseur](/virtualization/hyper-v-on-windows/reference/tlfs).

### <a name="direct-tsc-usage"></a>Utilisation directe du TSC

nous vous déconseillons fortement d’utiliser l’instruction de processeur **RDTSC** ou **rdtscp,** pour interroger directement le TSC, car vous n’obtiendrez pas de résultats fiables sur certaines versions de Windows, sur des migrations dynamiques de machines virtuelles et sur des systèmes matériels sans invariant ou synchronisés étroitement TSCs. Au lieu de cela, nous vous encourageons à utiliser [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) pour tirer parti de l’abstraction, de la cohérence et de la portabilité qu’il offre.

### <a name="examples-for-acquiring-time-stamps"></a>Exemples d’acquisition d’horodatages

Les différents exemples de code de ces sections montrent comment obtenir des horodatages.

### <a name="using-qpc-in-native-code"></a>Utilisation de QPC en code natif

Cet exemple montre comment utiliser [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) en code natif C et C++.


```C++
LARGE_INTEGER StartingTime, EndingTime, ElapsedMicroseconds;
LARGE_INTEGER Frequency;

QueryPerformanceFrequency(&Frequency); 
QueryPerformanceCounter(&StartingTime);

// Activity to be timed

QueryPerformanceCounter(&EndingTime);
ElapsedMicroseconds.QuadPart = EndingTime.QuadPart - StartingTime.QuadPart;


//
// We now have the elapsed number of ticks, along with the
// number of ticks-per-second. We use these values
// to convert to the number of elapsed microseconds.
// To guard against loss-of-precision, we convert
// to microseconds *before* dividing by ticks-per-second.
//

ElapsedMicroseconds.QuadPart *= 1000000;
ElapsedMicroseconds.QuadPart /= Frequency.QuadPart;
```



### <a name="acquiring-high-resolution-time-stamps-from-managed-code"></a>Acquisition d’horodatages haute résolution à partir du code managé

Cet exemple montre comment utiliser la classe [**System. Diagnostics. chronomètre**](/previous-versions/windows/) du code managé.


```CSharp
using System.Diagnostics;

long StartingTime = Stopwatch.GetTimestamp();

// Activity to be timed

long EndingTime  = Stopwatch.GetTimestamp();
long ElapsedTime = EndingTime - StartingTime;

double ElapsedSeconds = ElapsedTime * (1.0 / Stopwatch.Frequency);
```



La classe [**System. Diagnostics. chronomètre**](/previous-versions/windows/) fournit également plusieurs méthodes pratiques pour effectuer des mesures d’intervalle de temps.

### <a name="using-qpc-from-kernel-mode"></a>Utilisation de QPC à partir du mode noyau

le noyau Windows fournit un accès en mode noyau au compteur de performances par le biais de [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) à partir desquels le compteur de performance et la fréquence de performance peuvent être obtenus. **KeQueryPerformanceCounter** est disponible uniquement à partir du mode noyau et est fourni pour les rédacteurs de pilotes de périphériques et d’autres composants en mode noyau.

Cet exemple montre comment utiliser [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) en mode noyau C et C++.


```C++
LARGE_INTEGER StartingTime, EndingTime, ElapsedMicroseconds;
LARGE_INTEGER Frequency;

StartingTime = KeQueryPerformanceCounter(&Frequency);

// Activity to be timed

EndingTime = KeQueryPerformanceCounter(NULL);
ElapsedMicroseconds.QuadPart = EndingTime.QuadPart - StartingTime.QuadPart;
ElapsedMicroseconds.QuadPart *= 1000000;
ElapsedMicroseconds.QuadPart /= Frequency.QuadPart;
```



## <a name="general-faq-about-qpc-and-tsc"></a>FAQ générale sur QPC et TSC

Voici des réponses aux questions fréquemment posées sur [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) et TSCs en général.

<dl> <dt>

<span id="Is_QueryPerformanceCounter___the_same_as_the_Win32_GetTickCount___or_________GetTickCount64___function_"></span><span id="is_queryperformancecounter___the_same_as_the_win32_gettickcount___or_________gettickcount64___function_"></span><span id="IS_QUERYPERFORMANCECOUNTER___THE_SAME_AS_THE_WIN32_GETTICKCOUNT___OR_________GETTICKCOUNT64___FUNCTION_"></span>**QueryPerformanceCounter () est-il identique à la fonction Win32 GetTickCount () ou GetTickCount64 () ?**
</dt> <dd>

Non. [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) et [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) ne sont pas liés à [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). **GetTickCount** et **GetTickCount64** retournent le nombre de millisecondes écoulées depuis le démarrage du système.

</dd> <dt>

<span id="Should_I_use_QPC_or_call_the_RDTSC__RDTSCP_instructions_directly_"></span><span id="should_i_use_qpc_or_call_the_rdtsc__rdtscp_instructions_directly_"></span><span id="SHOULD_I_USE_QPC_OR_CALL_THE_RDTSC__RDTSCP_INSTRUCTIONS_DIRECTLY_"></span>**Dois-je utiliser QPC ou appeler directement les instructions RDTSC/RDTSCP ?**
</dt> <dd>

Pour éviter les problèmes d’inexactitude et de portabilité, nous vous encourageons vivement à utiliser [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) au lieu d’utiliser le registre TSC ou les instructions de processeur **RDTSC** ou **rdtscp,** .

</dd> <dt>

<span id="What_is_QPC_s_relation_to_an_external_time_epoch__Can_it_be_synchronized_to_an_________external_epoch_such_as_UTC_"></span><span id="what_is_qpc_s_relation_to_an_external_time_epoch__can_it_be_synchronized_to_an_________external_epoch_such_as_utc_"></span><span id="WHAT_IS_QPC_S_RELATION_TO_AN_EXTERNAL_TIME_EPOCH__CAN_IT_BE_SYNCHRONIZED_TO_AN_________EXTERNAL_EPOCH_SUCH_AS_UTC_"></span>**Qu’est-ce que la relation entre QPC et une époque de temps externe ? Peut-il être synchronisé avec une époque externe telle que l’heure UTC ?**
</dt> <dd>

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) est basé sur un compteur matériel qui ne peut pas être synchronisé avec une référence horaire externe, par exemple UTC. Pour obtenir des horodatages précis au moment de la journée qui peuvent être synchronisés avec une référence UTC externe, utilisez [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).

</dd> <dt>

<span id="Is_QPC_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="is_qpc_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="IS_QPC_AFFECTED_BY_DAYLIGHT_SAVINGS_TIME__LEAP_SECONDS__TIME_ZONES__OR_SYSTEM_________TIME_CHANGES_MADE_BY_THE_ADMINISTRATOR_"></span>**Le QPC est-il affecté par l’heure d’été, les secondes bissextiles, les fuseaux horaires ou les modifications de l’heure système effectuées par l’administrateur ?**
</dt> <dd>

Non. [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) est complètement indépendant de l’heure système et du temps universel coordonné (UTC).

</dd> <dt>

<span id="Is_QPC_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_Turbo_Boost_technology_"></span><span id="is_qpc_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_turbo_boost_technology_"></span><span id="IS_QPC_ACCURACY_AFFECTED_BY_PROCESSOR_FREQUENCY_CHANGES_CAUSED_BY_POWER_________MANAGEMENT_OR_TURBO_BOOST_TECHNOLOGY_"></span>**La précision QPC est-elle affectée par les modifications de fréquence du processeur dues à la gestion de l’alimentation ou à la technologie Turbo Boost ?**
</dt> <dd>

Non. Si le processeur a un TSC invariant, le [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) n’est pas affecté par ce type de modifications. Si le processeur ne dispose pas d’un TSC invariant, **QPC** reviendra à une horloge matérielle de la plateforme qui n’est pas affectée par les modifications de fréquence du processeur ou la technologie Turbo Boost.

</dd> <dt>

<span id="Does_QPC_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="does_qpc_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="DOES_QPC_RELIABLY_WORK_ON_MULTI-PROCESSOR_SYSTEMS__MULTI-CORE_SYSTEM__AND_________SYSTEMS_WITH_HYPER-THREADING_"></span>**QPC fonctionne-t-il de manière fiable sur les systèmes multiprocesseurs, le système multicœur et les systèmes avec Hyper-Threading ?**
</dt> <dd>

Oui

</dd> <dt>

<span id="How_do_I_determine_and_validate_that_QPC_works_on_my_machine_"></span><span id="how_do_i_determine_and_validate_that_qpc_works_on_my_machine_"></span><span id="HOW_DO_I_DETERMINE_AND_VALIDATE_THAT_QPC_WORKS_ON_MY_MACHINE_"></span>**Comment faire déterminer et vérifier que QPC fonctionne sur mon ordinateur ?**
</dt> <dd>

Vous n’avez pas besoin d’effectuer ces vérifications.

</dd> <dt>

<span id="Which_processors_have_non-invariant_TSCs__How_can_I_check_if_my_system_has_a_________non-invariant_TSC_"></span><span id="which_processors_have_non-invariant_tscs__how_can_i_check_if_my_system_has_a_________non-invariant_tsc_"></span><span id="WHICH_PROCESSORS_HAVE_NON-INVARIANT_TSCS__HOW_CAN_I_CHECK_IF_MY_SYSTEM_HAS_A_________NON-INVARIANT_TSC_"></span>**Quels processeurs ont des TSCs non invariants ? Comment puis-je vérifier si mon système a un TSC non indifférent ?**
</dt> <dd>

Vous n’avez pas besoin d’effectuer cette vérification vous-même. Windows systèmes d’exploitation effectuent plusieurs vérifications lors de l’initialisation du système pour déterminer si le TSC est approprié comme base pour [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Toutefois, à des fins de référence, vous pouvez déterminer si votre processeur a un TSC invariant en utilisant l’une des opérations suivantes :

-   utilitaire Coreinfo.exe de Windows Sysinternals
-   vérification des valeurs retournées par l’instruction CPUID concernant les caractéristiques TSC
-   documentation du fabricant du processeur

l’exemple suivant montre les informations sur les invariants TSC fournies par l’utilitaire Windows Sysinternals Coreinfo.exe utility ([www.sysinternals.com](https://www.sysinternals.com)). Un astérisque signifie « true ».

``` syntax
> Coreinfo.exe 

Coreinfo v3.2 - Dump information on system CPU and memory topology
Copyright (C) 2008-2012 Mark Russinovich
Sysinternals - www.sysinternals.com

 <unrelated text removed>

RDTSCP          * Supports RDTSCP instruction
TSC             * Supports RDTSC instruction
TSC-DEADLINE    - Local APIC supports one-shot deadline timer
TSC-INVARIANT   * TSC runs at constant rate
```

</dd> <dt>

<span id="Does_QPC_work_reliably_on__hardware_platforms_"></span><span id="does_qpc_work_reliably_on__hardware_platforms_"></span><span id="DOES_QPC_WORK_RELIABLY_ON__HARDWARE_PLATFORMS_"></span>**QPC fonctionne-t-il de façon fiable sur les plateformes matérielles PC Windows RT ?**
</dt> <dd>

Oui

</dd> <dt>

<span id="How_often_does_QPC_roll_over_"></span><span id="how_often_does_qpc_roll_over_"></span><span id="HOW_OFTEN_DOES_QPC_ROLL_OVER_"></span>**Quelle est la fréquence de l’annulation de QPC ?**
</dt> <dd>

Au moins 100 ans du démarrage système le plus récent, et potentiellement plus longtemps en fonction du minuteur matériel sous-jacent utilisé. Pour la plupart des applications, la substitution n’est pas un problème.

</dd> <dt>

<span id="What_is_the_computational_cost_of_calling_QPC_"></span><span id="what_is_the_computational_cost_of_calling_qpc_"></span><span id="WHAT_IS_THE_COMPUTATIONAL_COST_OF_CALLING_QPC_"></span>**Quel est le coût de calcul de l’appel de QPC ?**
</dt> <dd>

Le coût d’appel de calcul de [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) est déterminé principalement par la plateforme matérielle sous-jacente. Si le registre TSC est utilisé comme base pour QPC, le coût de calcul est déterminé principalement par la durée de traitement d’une instruction **RDTSC** par le processeur. Cette période est comprise entre 10 et 10 cycles de processeur, en fonction du processeur utilisé. Si le TSC ne peut pas être utilisé, le système sélectionnera une autre durée du matériel. Étant donné que ces bases de temps se trouvent sur la carte mère (par exemple, sur le pont Sud PCI ou PCH), le coût de calcul par appel est plus élevé que le TSC, et est fréquemment situé à proximité de 0,8 à 1,0 microsecondes, en fonction de la vitesse du processeur et d’autres facteurs matériels. Ce coût est dominé par le temps nécessaire pour accéder au périphérique matériel sur la carte mère.

</dd> <dt>

<span id="Does_QPC_require_a_kernel_transition__system_call__"></span><span id="does_qpc_require_a_kernel_transition__system_call__"></span><span id="DOES_QPC_REQUIRE_A_KERNEL_TRANSITION__SYSTEM_CALL__"></span>**QPC requiert-t-il une transition de noyau (appel système) ?**
</dt> <dd>

Une transition de noyau n’est pas nécessaire si le système peut utiliser le registre TSC comme base pour [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Si le système doit utiliser une autre base de temps, telle que la minuterie HPET ou PM, un appel système est nécessaire.

</dd> <dt>

<span id="Is_the_performance_counter_monotonic__non-decreasing__"></span><span id="is_the_performance_counter_monotonic__non-decreasing__"></span><span id="IS_THE_PERFORMANCE_COUNTER_MONOTONIC__NON-DECREASING__"></span>**Le compteur de performances est-il monotone (non décroissant) ?**
</dt> <dd>

Oui

</dd> <dt>

<span id="Can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="CAN_THE_PERFORMANCE_COUNTER_BE_USED_TO_ORDER_EVENTS_IN_TIME_"></span>**Le compteur de performances peut-il être utilisé pour ordonner les événements dans le temps ?**
</dt> <dd>

Oui. Toutefois, lors de la comparaison des résultats des compteurs de performance obtenus à partir de différents threads, les valeurs qui diffèrent par une graduation de ± 1 ont un ordre ambigu comme si elles avaient un horodatage identique.

</dd> <dt>

<span id="How_accurate_is_the_performance_counter_"></span><span id="how_accurate_is_the_performance_counter_"></span><span id="HOW_ACCURATE_IS_THE_PERFORMANCE_COUNTER_"></span>**Quel est le degré de précision du compteur de performances ?**
</dt> <dd>

La réponse dépend de plusieurs facteurs. Pour plus d’informations, consultez caractéristiques de l' [horloge matérielle de bas niveau](#low-level-hardware-clock-characteristics).

</dd> </dl>

## <a name="faq-about-programming-with-qpc-and-tsc"></a>FAQ sur la programmation avec QPC et TSC

Voici des réponses aux questions fréquemment posées sur la programmation avec [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) et TSCs.

<dl> <dt>

<span id="I_need_to_convert_the_QPC_output_to_milliseconds._How_can_I_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="i_need_to_convert_the_qpc_output_to_milliseconds._how_can_i_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="I_NEED_TO_CONVERT_THE_QPC_OUTPUT_TO_MILLISECONDS._HOW_CAN_I_AVOID_LOSS_OF_________PRECISION_WITH_CONVERTING_TO_DOUBLE_OR_FLOAT_"></span>**Je dois convertir la sortie QPC en millisecondes. Comment puis-je éviter la perte de précision lors de la conversion en double ou float ?**
</dt> <dd>

Il y a plusieurs choses à garder à l’esprit lors de l’exécution de calculs sur des compteurs de performances d’entiers :

-   La Division d’entiers perd le reste. Cela peut entraîner une perte de précision dans certains cas.
-   La conversion entre des entiers 64 bits et une virgule flottante (double) peut entraîner une perte de précision, car la mantisse à virgule flottante ne peut pas représenter toutes les valeurs intégrales possibles.
-   La multiplication des entiers 64 bits peut entraîner un dépassement sur les entiers.

En règle générale, retardez ces calculs et conversions autant que possible pour éviter d’aggraver les erreurs introduites.

</dd> <dt>

<span id="How_can_I_convert_QPC_to_100_nanosecond_ticks_so_I_can_add_it_to_a_________FILETIME_"></span><span id="how_can_i_convert_qpc_to_100_nanosecond_ticks_so_i_can_add_it_to_a_________filetime_"></span><span id="HOW_CAN_I_CONVERT_QPC_TO_100_NANOSECOND_TICKS_SO_I_CAN_ADD_IT_TO_A_________FILETIME_"></span>**Comment puis-je convertir QPC en graduations de 100 nanosecondes afin de pouvoir l’ajouter à un FILETIME ?**
</dt> <dd>

Une heure de fichier est une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes qui se sont écoulés depuis 12:00 h 00. Le 1er janvier 1601 temps universel coordonné (UTC). Les heures de fichier sont utilisées par les appels d’API Win32 qui renvoient l’heure du jour, par exemple [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) et [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime). En revanche, [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) retourne des valeurs qui représentent le temps en unités de 1/(fréquence du compteur de performance obtenu à partir de [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)). La conversion entre les deux requiert le calcul du rapport entre l’intervalle **QPC** et les intervalles de 100 nanosecondes. Veillez à éviter la perte de précision, car les valeurs peuvent être petites (0,0000001/0,000000340).

</dd> <dt>

<span id="Why_is_the_time_stamp_that_is_returned_from_QPC_a_signed_integer_"></span><span id="why_is_the_time_stamp_that_is_returned_from_qpc_a_signed_integer_"></span><span id="WHY_IS_THE_TIME_STAMP_THAT_IS_RETURNED_FROM_QPC_A_SIGNED_INTEGER_"></span>**Pourquoi l’horodatage renvoyé par QPC est-il un entier signé ?**
</dt> <dd>

Les calculs qui impliquent des horodatages [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) peuvent impliquer la soustraction. En utilisant une valeur signée, vous pouvez gérer des calculs qui peuvent produire des valeurs négatives.

</dd> <dt>

<span id="How_can_I_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="how_can_i_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="HOW_CAN_I_OBTAIN_HIGH_RESOLUTION_TIME_STAMPS_FROM_MANAGED_CODE_"></span>**Comment puis-je obtenir des horodatages haute résolution à partir du code managé ?**
</dt> <dd>

Appelez la méthode [**chronomètre. getTimestamp**](/previous-versions/windows/) à partir de la classe [**System. Diagnostics. chronomètre**](/previous-versions/windows/) . Pour obtenir un exemple d’utilisation de **chronomètre. getTimestamp**, consultez [acquisition d’horodatages haute résolution à partir du code managé](#acquiring-high-resolution-time-stamps-from-managed-code).

</dd> <dt>

<span id="Under_what_circumstances_does_QueryPerformanceFrequency_return_FALSE__or_________QueryPerformanceCounter_return_zero_"></span><span id="under_what_circumstances_does_queryperformancefrequency_return_false__or_________queryperformancecounter_return_zero_"></span><span id="UNDER_WHAT_CIRCUMSTANCES_DOES_QUERYPERFORMANCEFREQUENCY_RETURN_FALSE__OR_________QUERYPERFORMANCECOUNTER_RETURN_ZERO_"></span>**Dans quelles circonstances QueryPerformanceFrequency retourne FALSe ou QueryPerformanceCounter retourne zéro ?**
</dt> <dd>

cela ne se produit pas sur les systèmes qui exécutent Windows XP ou version ultérieure.

</dd> <dt>

<span id="Do_I_need_to_set_the_thread_affinity_to_a_single_core_to_use_QPC_"></span><span id="do_i_need_to_set_the_thread_affinity_to_a_single_core_to_use_qpc_"></span><span id="DO_I_NEED_TO_SET_THE_THREAD_AFFINITY_TO_A_SINGLE_CORE_TO_USE_QPC_"></span>**Ai-je besoin de définir l’affinité de thread sur un seul cœur pour utiliser QPC ?**
</dt> <dd>

Non. Pour plus d’informations, consultez [conseils pour l’acquisition d’horodatages](#guidance-for-acquiring-time-stamps). Ce scénario n’est ni nécessaire ni souhaitable. L’exécution de ce scénario peut nuire aux performances de votre application en restreignant le traitement à un seul cœur ou en créant un goulot d’étranglement sur un seul cœur si plusieurs threads définissent leur affinité sur le même noyau lors de l’appel de [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

</dd> </dl>

## <a name="low-level-hardware-clock-characteristics"></a>Caractéristiques de l’horloge matérielle de bas niveau

Ces sections présentent les caractéristiques de l’horloge matérielle de bas niveau.

### <a name="absolute-clocks-and-difference-clocks"></a>Horloges absolues et horloges de différence

Les horloges absolues fournissent des lectures temporelles précises. Elles sont généralement basées sur le temps universel coordonné (UTC, Universal Time Coordinated) et, par conséquent, leur précision dépend en partie de la façon dont elles sont synchronisées avec une référence horaire externe. Les horloges de différence mesurent les intervalles de temps et ne sont généralement pas basées sur une époque de temps externe. [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) est une horloge de différence et n’est pas synchronisée avec une époque ou référence de temps externe. Lorsque vous utilisez **QPC** pour les mesures de l’intervalle de temps, vous obtiendrez généralement une meilleure précision que si vous obteniez des horodatages dérivés d’une horloge absolue. Cela est dû au fait que le processus de synchronisation de l’heure d’une horloge absolue peut introduire des décalages de phase et de fréquence qui augmentent l’incertitude des mesures de l’intervalle de temps à long terme.

### <a name="resolution-precision-accuracy-and-stability"></a>Résolution, précision, précision et stabilité

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) utilise un compteur matériel comme base. Les minuteurs matériels se composent de trois parties : un générateur de graduations, un compteur qui compte les graduations et un moyen de récupérer la valeur de compteur. Les caractéristiques de ces trois composants déterminent la résolution, la précision, la précision et la stabilité des **QPC**.

Si un générateur de matériel fournit des graduations à une vitesse constante, les intervalles de temps peuvent être mesurés en comptant simplement ces graduations. La vitesse à laquelle les battements sont générées est appelée fréquence et exprimée en Hertz (Hz). La réciproque de la fréquence est appelée intervalle de période ou de cycle et est exprimée dans un système international approprié d’unités de temps (SI) (par exemple, seconde, milliseconde, microseconde ou nanoseconde).

![intervalle de temps](images/tick-interval.png)

La résolution de la minuterie est égale à la période. La résolution détermine la possibilité de faire la distinction entre deux horodatages et place une limite inférieure sur les intervalles de temps les plus petits qui peuvent être mesurés. C’est ce que l’on appelle parfois la résolution de graduation.

La mesure numérique du temps introduit une incertitude de mesure de ± 1 cycle, car le compteur numérique avance en étapes discrètes, tandis que le temps progresse continuellement. Cette incertitude est appelée une erreur de quantification. Pour les mesures d’intervalle de temps classiques, cet effet peut souvent être ignoré car l’erreur de quantification est bien plus petite que l’intervalle de temps mesuré.

![mesure du temps numérique](images/digital-time-measure.png)

Toutefois, si la période mesurée est faible et s’approche de la résolution de la minuterie, vous devez tenir compte de cette erreur de quantification. La taille de l’erreur introduite est celle d’une période d’horloge.

Les deux diagrammes suivants illustrent l’impact de l’incertitude du battement ± 1 à l’aide d’un minuteur avec une résolution de 1 unité de temps.

![incertitude du cycle](images/tick-uncertainty.png)

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) retourne la fréquence de [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter), et la période et la résolution sont égales à la réciproque de cette valeur. La fréquence des compteurs de performance renvoyée par **QueryPerformanceFrequency** est déterminée lors de l’initialisation du système et ne change pas pendant l’exécution du système.

> [!Note]  
> Il existe des cas où [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) ne retourne pas la fréquence réelle du générateur de cycles matériels. Par exemple, dans de nombreux cas, **QueryPerformanceFrequency** retourne la fréquence TSC divisée par 1024 ; et sur Hyper-V, la fréquence du compteur de performance est toujours de 10 MHz lorsque l’ordinateur virtuel invité s’exécute sous un [hyperviseur](https://msdn.microsoft.com/library/Ff542584(v=VS.85).aspx) qui implémente l’interface de l' [hyperviseur version 1,0](https://msdn.microsoft.com/library/Ff541458(v=VS.85).aspx). Par conséquent, ne supposez pas que **QueryPerformanceFrequency** retourne la fréquence TSC précise.

 

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) lit le compteur de performance et retourne le nombre total de cycles qui se sont produits depuis le démarrage du système d’exploitation Windows, y compris l’heure à laquelle l’ordinateur se trouvait dans un état de veille tel que en veille, en veille prolongée ou en veille connectée.

Ces exemples montrent comment calculer l’intervalle de graduation et la résolution et comment convertir le nombre de graduations en valeur d’heure.

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Exemple 1**
</dt> <dd>

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) retourne la valeur 3 125 000 sur un ordinateur particulier. Quel est l’intervalle de graduation et la résolution des mesures de [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) sur cet ordinateur ? L’intervalle de graduation, ou point, est la réciproque de 3 125 000, qui est 0,000000320 (320 nanosecondes). Par conséquent, chaque battement représente le passage de nanosecondes de 320. Les intervalles de temps inférieurs à 320 nanosecondes ne peuvent pas être mesurés sur cet ordinateur.

Intervalle de graduation = 1/(fréquence de performance)

Intervalle de graduation = 1/3125000 = 320 NS

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Exemple 2**
</dt> <dd>

Sur le même ordinateur que l’exemple précédent, la différence entre les valeurs retournées par deux appels successifs à [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) est de 5. Combien de temps s’est écoulé entre les deux appels ? 5 battements multiplié par 320 nanosecondes génèrent 1,6 microsecondes.

ElapsedTime = intervalle de \* graduations

ElapsedTime = 5 \* 320 NS = 1,6 μs

</dd> </dl>

L’accès (lecture) du compteur du logiciel prend du temps, et ce temps d’accès peut réduire la précision de la mesure du temps. Cela est dû au fait que la durée minimale de l’intervalle (l’intervalle de temps le plus court pouvant être mesuré) est la plus grande de la résolution et du temps d’accès.

Précision = \[ résolution maximale, AccessTime\]

Par exemple, considérez un minuteur matériel hypothétique avec une résolution de 100 nanosecondes et un temps d’accès de 800 nanoseconde. Cela peut être le cas si la minuterie de la plateforme a été utilisée à la place du Registre TSC comme base de [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Par conséquent, la précision est de 800 nanosecondes non 100 nanosecondes, comme indiqué dans ce calcul.

Précision = MAX \[ 800 NS, 100 NS \] = 800 NS

Ces deux figures illustrent cet effet.

![heure d’accès QPC](images/qpc-access-time.png)

Si le temps d’accès est supérieur à la résolution, ne tentez pas d’améliorer la précision en devinant. En d’autres termes, il s’agit d’une erreur qui consiste à supposer que l’horodatage est pris précisément au milieu, ou au début ou à la fin de l’appel.

En revanche, prenons l’exemple suivant dans lequel l’heure d’accès [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) est uniquement de 20 nanosecondes et la résolution de l’horloge matérielle est de 100 nanosecondes. Cela peut être le cas si le registre TSC a été utilisé comme base pour **QPC**. Ici, la précision est limitée par la résolution de l’horloge.

![précision QPC](images/qpc-precision.png)

Dans la pratique, vous pouvez rechercher les sources de temps pour lesquelles le temps nécessaire pour lire le compteur est plus grand ou plus petit que la résolution. Dans les deux cas, la précision est la plus grande des deux.

Ce tableau fournit des informations sur la résolution approximative, le temps d’accès et la précision d’une variété d’horloges. Notez que certaines valeurs varient selon les processeurs, les plateformes matérielles et les vitesses de processeur.



| Source de l’horloge                                                      | Fréquence d’horloge nominale | Résolution de l’horloge    | Temps d’accès (par défaut) | Précision       |
|-------------------------------------------------------------------|-------------------------|---------------------|-----------------------|-----------------|
| ORDINATEUR RTC                                                            | 64 Hz                   | 15,625 millisecondes | N/A                   | N/A             |
| Compteur de performances de requête utilisant TSC avec une horloge de processeur de 3 GHz  | 3 MHz                   | 333 nanosecondes     | 30 nanosecondes        | 333 nanosecondes |
| Instruction de machine **RDTSC** sur un système avec une durée de cycle de 3 GHz | 3 GHz                   | 333 picoseconds     | 30 nanosecondes        | 30 nanosecondes  |



 

Comme [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) utilise un compteur matériel, lorsque vous comprenez certaines caractéristiques de base des compteurs matériels, vous vous familiarisez avec les fonctionnalités et les limitations de **QPC**.

Le générateur de cycles matériels le plus couramment utilisé est un oscillateur à cristal. Le cristal est un petit morceau de quartz ou autre matériau céramique qui présente des caractéristiques piézoélectriques qui fournissent une référence de fréquence peu coûteuse avec une stabilité et une précision excellentes. Cette fréquence est utilisée pour générer les graduations comptées par l’horloge.

La précision d’un minuteur fait référence au degré de conformité à une valeur true ou standard. Cela dépend principalement de la capacité de l’oscillateur Crystal à fournir des graduations à la fréquence spécifiée. Si la fréquence d’oscillation est trop élevée, l’horloge est « exécutée rapidement » et les intervalles mesurés s’affichent plus longtemps qu’ils ne le sont vraiment. en outre, si la fréquence est trop faible, l’horloge s’exécute lentement et les intervalles mesurés sont plus courts qu’ils ne le sont vraiment.

Pour les mesures d’intervalle de temps standard pour une durée brève (par exemple, les mesures de temps de réponse, les mesures de latence réseau, etc.), la précision de l’oscillateur matériel est généralement suffisante. Toutefois, pour certaines mesures, la précision de la fréquence de l’oscillateur devient importante, en particulier pour les intervalles de temps longs ou lorsque vous souhaitez comparer les mesures effectuées sur des ordinateurs différents. Le reste de cette section explore les effets de la précision de l’oscillateur.

La fréquence d’oscillation des cristaux est définie pendant le processus de fabrication et est spécifiée par le fabricant en termes de fréquence spécifiée plus ou moins une tolérance de fabrication exprimée en « parties par million » (ppm), appelée décalage de fréquence maximale. Un cristal avec une fréquence spécifiée de 1 million Hz et un décalage de fréquence maximal de ± 10 ppm se trouve dans les limites de spécifications si sa fréquence réelle est comprise entre 999 990 Hz et 1 000 010 Hz.

En remplaçant les parties de l’expression par million de microsecondes par seconde, nous pouvons appliquer cette erreur de décalage de fréquence aux mesures de l’intervalle de temps. Un oscillateur avec un décalage de + 10 ppm a une erreur de 10 microsecondes par seconde. En conséquence, lorsque vous mesurez un intervalle de 1 seconde, il s’exécute rapidement et mesure un intervalle de 1 seconde comme 0,999990 secondes.

Une référence pratique est qu’une erreur de fréquence de 100 ppm provoque une erreur de 8,64 secondes après 24 heures. Ce tableau présente l’incertitude de mesure en raison de l’erreur accumulée pendant des intervalles de temps plus longs.



| Durée de l’intervalle de temps | incertitude de mesure due à une erreur accumulée avec une tolérance de fréquence de +/-10 PPM |
|------------------------|--------------------------------------------------------------------------------------|
| 1 microseconde          | ± 10 picoseconds (10-12)                                                             |
| 1 milliseconde          | ± 10 nanosecondes (10-9)                                                              |
| 1 seconde               | ± 10 microsecondes                                                                    |
| 1 heure                 | ± 60 microsecondes                                                                    |
| 1 jour                  | ± 0,86 secondes                                                                       |
| 1 semaine                 | ± 6,08 secondes                                                                       |



 

Le tableau ci-dessus montre que pour les intervalles de temps réduits, l’erreur de décalage de fréquence peut souvent être ignorée. Toutefois, pour des intervalles de temps longs, même un décalage de fréquence réduit peut entraîner une incertitude significative de la mesure.

Les oscillateurs Crystal utilisés dans les ordinateurs personnels et les serveurs sont généralement fabriqués avec une tolérance de fréquence de ± 30 à 50 pièces par million et, rarement, les cristaux peuvent être désactivés jusqu’à 500 ppm. Bien que les cristaux avec des tolérances de décalage de fréquence beaucoup plus étroites soient disponibles, ils sont plus onéreux et ne sont donc pas utilisés dans la plupart des ordinateurs.

pour réduire les effets indésirables de cette erreur de décalage de fréquence, les versions récentes de Windows, en particulier Windows 8, utilisent plusieurs minuteries matérielles pour détecter le décalage de fréquence et compenser le décalage dans la mesure du possible. ce processus d’étalonnage est effectué au démarrage de Windows.

Comme le montrent les exemples suivants, l’erreur de décalage de fréquence d’une horloge matérielle influence la précision obtenue et la résolution de l’horloge peut être moins importante.

![l’erreur de décalage de fréquence influe sur la précision obtenue](images/freq-offset-error.png)

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Exemple 1**
</dt> <dd>

Supposons que vous exécutiez des mesures d’intervalle de temps à l’aide d’un oscillateur de 1 MHz, qui a une résolution de 1 microseconde et une erreur de décalage de fréquence maximale de ± 50 ppm. Nous supposons à présent que le décalage soit exactement + 50 ppm. Cela signifie que la fréquence réelle est de 1 000 050 Hz. Si nous avons mesuré un intervalle de temps de 24 heures, notre mesure serait de 4,3 secondes trop courtes (23:59:55.700000 mesuré par rapport à 24:00:00.000000 réel).

Secondes dans une journée = 86400

Erreur de décalage de fréquence = 50 ppm = 0,00005

86 400 secondes \* 0,00005 = 4,3 secondes

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Exemple 2**
</dt> <dd>

Supposons que l’horloge TSC du processeur est contrôlée par un oscillateur cristallin et que la fréquence spécifiée est de 3 GHz. Cela signifie que la résolution est de 1/3000000000 ou d’environ 333 picoseconds. Supposons que le cristal utilisé pour contrôler l’horloge du processeur a une tolérance de fréquence de ± 50 ppm et qu’elle est en fait de + 50 ppm. Malgré la haute résolution, une mesure de l’intervalle de temps de 24 heures sera toujours de 4,3 secondes. (23:59:55.7000000000 mesuré par rapport à 24:00:00.0000000000 réel).

Secondes dans une journée = 86400

Erreur de décalage de fréquence = 50 ppm = 0,00005

86 400 secondes \* 0,00005 = 4,3 secondes

Cela montre qu’une horloge TSC haute résolution ne fournit pas nécessairement des mesures plus précises qu’une horloge de résolution inférieure.

</dd> <dt>

<span id="Example_3"></span><span id="example_3"></span><span id="EXAMPLE_3"></span>**Exemple 3**
</dt> <dd>

Envisagez d’utiliser deux ordinateurs différents pour mesurer le même intervalle de 24 heures. Les deux ordinateurs ont un oscillateur avec un décalage de fréquence maximal de ± 50 ppm. À quelle distance la mesure du même intervalle de temps sur ces deux systèmes peut-elle être ? Comme dans les exemples précédents, ± 50 ppm génère une erreur maximale de ± 4,3 secondes après 24 heures. Si un système exécute 4,3 secondes rapidement et que les autres 4,3 secondes sont lentes, l’erreur maximale au bout de 24 heures peut être de 8,6 secondes.

Secondes dans une journée = 86400

Erreur de décalage de fréquence = ± 50 ppm = ± 0,00005

± (86 400 secondes \* 0,00005) = ± 4,3 secondes

Décalage maximal entre les deux systèmes = 8,6 secondes

En résumé, l’erreur de décalage de fréquence devient de plus en plus importante lorsque vous mesurez des intervalles de temps longs et que vous comparez des mesures entre différents systèmes.

La stabilité d’un minuteur indique si la fréquence des graduations change au fil du temps, par exemple suite à des modifications de températures. Les cristaux de quartz utilisés comme générateurs de battements sur les ordinateurs présentent de petites modifications de fréquence en tant que fonction de température. L’erreur provoquée par la dérive thermique est généralement faible par rapport à l’erreur de décalage de fréquence pour les plages de température courantes. Toutefois, les concepteurs de logiciels pour les équipements portables ou les équipements soumis à des fluctuations de température importante peuvent avoir à prendre en compte cet effet.

</dd> </dl>

## <a name="hardware-timer-info"></a>Informations sur la minuterie matérielle

<dl> <dt>

<span id="TSC_Register"></span><span id="tsc_register"></span><span id="TSC_REGISTER"></span>**Registre TSC**
</dt> <dd>

Certains processeurs Intel et AMD contiennent un registre TSC qui est un registre 64 bits qui augmente à un taux élevé, généralement égal à l’horloge du processeur. La valeur de ce compteur peut être lue à l’aide des instructions de l’ordinateur **RDTSC** ou **rdtscp,** , ce qui permet de réduire le temps d’accès et le coût de calcul dans l’ordre des dizaines ou des centaines de cycles de machine, en fonction du processeur.

Bien que le registre TSC ressemble à un mécanisme d’horodatage idéal, voici quelques circonstances dans lesquelles il ne peut pas fonctionner de manière fiable à des fins de minuterie :

-   Tous les processeurs n’ont pas de registres TSC. par conséquent, l’utilisation du Registre TSC dans le logiciel crée directement un problème de portabilité. (Windows sélectionnera une autre source de temps pour [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) dans ce cas, ce qui évite le problème de portabilité.)
-   Certains processeurs peuvent varier la fréquence de l’horloge TSC ou arrêter l’avancement du Registre TSC, ce qui rend le TSC inadapté à des fins de synchronisation sur ces processeurs. Ces processeurs sont appelés registres TSC non invariants. (Windows détecte automatiquement cela et sélectionne une autre source de temps pour [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).
-   Sur les systèmes multiprocesseurs ou multicœurs, certains processeurs et systèmes ne peuvent pas synchroniser les horloges de chaque cœur avec la même valeur. (Windows détecte automatiquement cela et sélectionne une autre source de temps pour [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).
-   Sur certains systèmes multiprocesseurs volumineux, vous ne pourrez peut-être pas synchroniser les horloges du processeur avec la même valeur même si le processeur a un TSC invariant. (Windows détecte automatiquement cela et sélectionne une autre source de temps pour [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).
-   Certains processeurs exécutent des instructions dans le désordre. Cela peut entraîner des nombres de cycles incorrects lorsque **RDTSC** est utilisé pour les séquences d’instructions Time, car l’instruction **RDTSC** peut être exécutée à une heure différente de celle spécifiée dans votre programme. L’instruction **rdtscp,** a été introduite sur certains processeurs en réponse à ce problème.

Comme les autres minuteries, le TSC est basé sur un oscillateur à quartz dont la fréquence exacte n’est pas connue à l’avance et qui a une erreur de décalage de fréquence. Ainsi, avant de pouvoir être utilisé, il doit être étalonné à l’aide d’une autre référence de minutage.

lors de l’initialisation du système, Windows vérifie si le TSC est adapté à des fins de synchronisation et effectue l’étalonnage et la synchronisation de base de la fréquence nécessaires.

</dd> <dt>

<span id="PM_Clock"></span><span id="pm_clock"></span><span id="PM_CLOCK"></span>**Heure PM**
</dt> <dd>

Le minuteur ACPI, également appelé horloge PM, a été ajouté à l’architecture système pour fournir des horodatages fiables indépendamment de la vitesse des processeurs. Comme il s’agissait du seul objectif de ce minuteur, il fournit un horodatage en un seul cycle d’horloge, mais il ne fournit pas d’autres fonctionnalités.

</dd> <dt>

<span id="HPET_Timer"></span><span id="hpet_timer"></span><span id="HPET_TIMER"></span>**Minuteur HPET**
</dt> <dd>

Le High Precision Event Timer (HPET) a été développé conjointement par Intel et Microsoft afin de répondre aux exigences de synchronisation du multimédia et d’autres applications de temps. la prise en charge de HPET a été Windows depuis Windows Vista, et Windows 7 et Windows 8 certification de Logo matériel nécessite la prise en charge de HPET dans la plateforme matérielle.

</dd> </dl>

 

 
