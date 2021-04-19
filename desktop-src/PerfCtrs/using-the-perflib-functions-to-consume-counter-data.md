---
title: Utilisation des fonctions PerfLib pour consommer des données de compteurs
description: Les fonctions de l’API PerfLib peuvent être utilisées pour consommer des données de compteur de performances v2 directement lorsque PDH ne peut pas être utilisé.
ms.date: 08/17/2020
ms.topic: article
ms.openlocfilehash: 9fec3bb97ec32ff98e2b317b737023da81147bdd
ms.sourcegitcommit: f7cf41ffc79d1ffead9de2fc61677201f94b423a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2020
ms.locfileid: "106513745"
---
# <a name="using-the-perflib-functions-to-consume-counter-data"></a>Utilisation des fonctions PerfLib pour consommer des données de compteurs

Utilisez les fonctions de consommateur PerfLib pour consommer des données de performances à partir de fournisseurs de données de performances v2 lorsque vous ne pouvez pas utiliser les [fonctions d’assistance des données de performance (PDH)](using-the-pdh-functions-to-consume-counter-data.md). Ces fonctions peuvent être utilisées lors de l’écriture d’applications OneCore pour collecter des countersets v2 ou lorsque vous devez collecter des countersets v2 avec des dépendances et une surcharge minimales.

> [!TIP]
> Les fonctions de consommateur de PerfLib v2 sont plus difficiles à utiliser que les fonctions de performance Data Helper (PDH) et ne prennent en charge que la collecte de données à partir de fournisseurs v2. Les fonctions PDH doivent être préférées pour la plupart des applications.

Les fonctions de consommateur de PerfLib v2 sont l’API de bas niveau pour la collecte de données à partir de **fournisseurs v2**. Les fonctions de consommateur de PerfLib v2 ne prennent pas en charge la collecte de données à partir de **fournisseurs v1**.

> [!WARNING]
> Les fonctions de consommateur de PerfLib v2 peuvent potentiellement collecter des données à partir de sources non approuvées, par exemple, à partir de services locaux à privilèges limités ou à partir d’ordinateurs distants. Les fonctions de consommateur de PerfLib v2 ne valident pas les données pour l’intégrité ou la cohérence. Il revient à votre application consommateur de vérifier que les données retournées sont cohérentes, par exemple, que les valeurs de taille dans le bloc de données retourné ne dépassent pas la taille réelle du bloc de données retourné. Cela est particulièrement important lorsque l’application consommateur s’exécute avec des privilèges élevés.

## <a name="perflib-usage"></a>Utilisation de PerfLib

L' `perflib.h` en-tête comprend les déclarations utilisées par les fournisseurs en mode utilisateur V2 (c’est-à-dire l’API du fournisseur Perflib) et les consommateurs v2 (c’est-à-dire l’API du consommateur Perflib). Elle déclare les fonctions suivantes pour la consommation des données de performances v2 :

- Utilisez [**PerfEnumerateCounterSet**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset) pour récupérer les GUID des countersets inscrits par les fournisseurs v2 sur le système.
- Utilisez [**PerfQueryCounterSetRegistrationInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo) pour obtenir des informations sur un CounterSet particulier, tel que le nom, la description, le type (instance unique ou multi-instance) du CounterSet, les types de compteurs, les noms de compteurs et les descriptions de compteurs.
- Utilisez [**PerfEnumerateCounterSetInstances**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances) pour obtenir les noms des instances actuellement actives d’un CounterSet multi-instance.
- Utilisez [**PerfOpenQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle) pour créer un nouveau descripteur de requête à utiliser pour collecter des données à partir d’un ou plusieurs countersets.
- Utilisez [**PerfCloseQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle) pour fermer un handle de requête.
- Utilisez [**PerfAddCounters**](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters) pour ajouter une requête à un handle de requête.
- Utilisez [**PerfDeleteCounters**](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters) pour supprimer une requête d’un handle de requête.
- Utilisez [**PerfQueryCounterInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo) pour obtenir des informations sur les requêtes en cours sur un handle de requête.
- Utilisez [**PerfQueryCounterData**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata) pour collecter les données de performances à partir d’un handle de requête.

Si votre consommateur consomme des données uniquement à partir d’un fournisseur spécifique où le GUID et les index de compteur sont stables et que vous avez accès au fichier de symboles généré par [CTRPP](ctrpp.md)(à partir du `-ch` paramètre ctrpp), vous pouvez coder en dur le GUID du CounterSet et les valeurs d’index de compteur dans votre consommateur.

Dans le cas contraire, vous devrez charger les métadonnées du CounterSet pour déterminer le (s) GUID (s) du CounterSet et les index de compteur à utiliser dans votre requête comme suit :

- Utilisez **PerfEnumerateCounterSet** pour obtenir la liste des GUID du CounterSet pris en charge.
- Pour chaque GUID, utilisez **PerfQueryCounterSetRegistrationInfo** pour charger le nom du CounterSet. Arrêtez quand vous trouvez le nom que vous recherchez.
- Utilisez **PerfQueryCounterSetRegistrationInfo** pour charger les métadonnées restantes (configuration du CounterSet, noms des compteurs, index de compteurs, types de compteurs) pour ce CounterSet.

Si vous avez simplement besoin de connaître les noms des instances actuellement actives d’un CounterSet (c’est-à-dire si vous n’avez pas besoin des valeurs de données de performances réelles), vous pouvez utiliser **PerfEnumerateCounterSetInstances**. Cela prend un GUID du CounterSet comme entrée et retourne un `PERF_INSTANCE_HEADER` bloc avec les noms et les ID des instances actuellement actives du CounterSet donné.

### <a name="queries"></a>Requêtes

Pour collecter des données de performances, vous devez créer un descripteur de requête, y ajouter des requêtes et collecter les données à partir des requêtes.

Plusieurs requêtes peuvent être associées à un descripteur de requête. Quand vous appelez **PerfQueryCounterData** pour un handle de requête, perflib exécute toutes les requêtes du handle et collecte tous les résultats.

Chaque requête spécifie un GUID du CounterSet, un filtre de nom d’instance, un filtre d’ID d’instance facultatif et un filtre d’ID de compteur facultatif.

- Le GUID du CounterSet est requis. Elle indique le GUID du CounterSet à partir duquel la requête collectera les données. Cela est similaire à la `FROM` clause d’une requête SQL.
- Le filtre de nom d’instance est requis. Il indique un modèle de caractère générique que le nom d’instance doit mettre en correspondance pour que l’instance soit incluse dans la requête, en `*` indiquant « tout caractère » et en `?` indiquant « un caractère ». Pour les countersets d’instance unique, cette valeur **doit** être une chaîne de longueur nulle `""` . Pour les countersets multi-instances, cette valeur **doit** être une chaîne non vide (utilisez `"*"` pour accepter tous les noms d’instance). Cela est similaire à une `WHERE InstanceName LIKE NameFilter` clause d’une requête SQL.
- Le filtre de l’ID d’instance est facultatif. S’il est présent (par exemple, s’il est défini sur une valeur autre que `0xFFFFFFFF` ), il indique que la requête doit uniquement collecter les instances où l’ID d’instance correspond à l’ID spécifié. En cas d’absence (c’est-à-dire si `0xFFFFFFFF` la valeur est), elle indique que la requête doit accepter tous les ID d’instance. Cela est similaire à une `WHERE InstanceId == IdFilter` clause d’une requête SQL.
- Le filtre de l’ID de compteur est facultatif. Si elle est présente (c’est-à-dire si elle est définie sur une valeur autre que `PERF_WILDCARD_COUNTER` ), elle indique que la requête doit collecter un compteur unique, similaire à une `SELECT CounterName` clause d’une requête SQL. En cas d’absence (c’est-à-dire si `PERF_WILDCARD_COUNTER` la valeur est), elle indique que la requête doit collecter tous les compteurs disponibles, comme dans une `SELECT *` clause d’une requête SQL.

Utilisez **PerfAddCounters** pour ajouter des requêtes à un handle de requête. Utilisez **PerfDeleteCounters** pour supprimer des requêtes d’un handle de requête.

Après avoir modifié les requêtes dans un handle de requête, utilisez **PerfQueryCounterInfo** pour obtenir les index de requête. Les index indiquent l’ordre dans lequel les résultats de la requête sont retournés par **PerfQueryCounterData** (les résultats ne correspondent pas toujours à l’ordre dans lequel les requêtes ont été ajoutées).

Une fois que le handle de requête est prêt, utilisez **PerfQueryCounterData** pour collecter les données. Normalement, vous collectez les données régulièrement (une fois par seconde ou une fois par minute), puis traitez les données en fonction des besoins.

> [!NOTE]
> Les compteurs de performance ne sont pas conçus pour être collectés plusieurs fois par seconde.

**PerfQueryCounterData** retourne un `PERF_DATA_HEADER` bloc, qui se compose d’un en-tête de données avec des horodateurs suivis d’une séquence de `PERF_COUNTER_HEADER` blocs, chacun contenant les résultats d’une requête.

`PERF_COUNTER_HEADER`Peut contenir plusieurs types de données différents, comme indiqué par la valeur du `dwType` champ :

- `PERF_ERROR_RETURN` -PerfLib ne peut pas récupérer les données de compteur valides à partir du fournisseur.
- `PERF_SINGLE_COUNTER` -La requête était destinée à un compteur unique à partir d’un CounterSet à instance unique. Les résultats contiennent uniquement la valeur de compteur demandée.
- `PERF_MULTIPLE_COUNTERS` -La requête était destinée à plusieurs compteurs à partir d’un CounterSet à instance unique. Le résultat contient les valeurs de compteur, ainsi que des informations permettant de faire correspondre chaque valeur avec le compteur correspondant (c’est-à-dire les en-têtes de colonne).
- `PERF_MULTIPLE_INSTANCES` -La requête était destinée à un compteur unique à partir d’un CounterSet multi-instance. Les résultats contiennent les informations d’instance (par exemple, les en-têtes de ligne) et une valeur de compteur par instance.
- `PERF_COUNTERSET` -La requête était destinée à plusieurs compteurs d’un CounterSet multi-instance. Les résultats contiennent les informations d’instance (par exemple, les en-têtes de ligne), les valeurs de compteur pour chaque instance et les informations pour faire correspondre chaque valeur avec le compteur correspondant (c’est-à-dire les en-têtes de colonne).

Les valeurs retournées par **PerfQueryCounterData** sont des `UINT32` `UINT64` valeurs brutes ou. Elles nécessitent généralement un traitement pour produire les valeurs mises en forme attendues. Le traitement requis dépend du type du compteur. De nombreux types de compteurs requièrent des informations supplémentaires pour un traitement complet, par exemple un horodateur ou une valeur d’un compteur « base » dans le même échantillon.

Certains types de compteurs sont des compteurs « Delta » qui ne sont significatifs que lorsqu’ils sont comparés aux données d’un exemple précédent. Par exemple, un compteur de type `PERF_SAMPLE_COUNTER` a une valeur mise en forme censée afficher un taux (le nombre de fois qu’une opération particulière s’est produite par seconde sur l’intervalle échantillon), mais la valeur brute réelle est simplement un nombre (le nombre de fois qu’une chose particulière s’est produite au total). Pour produire la valeur « Rate » mise en forme, vous devez appliquer la formule correspondant au type de compteur. La formule pour `PERF_SAMPLE_COUNTER` est `(N1 - N0) / ((T1 - T0) / F)` : soustraire la valeur de l’exemple actuel de la valeur de l’exemple précédent (en indiquant le nombre de fois où l’événement s’est produit au cours de l’intervalle échantillon), puis divisez le résultat par le nombre de secondes dans l’intervalle échantillon (obtenu en soustrayant l’horodateur de l’exemple actuel de l’horodateur de l’exemple précédent et en divisant par

Pour plus d’informations sur le calcul des valeurs mises en forme à partir de valeurs brutes, consultez [calcul des valeurs de compteur](calculating-counter-values.md) .

## <a name="sample"></a>Exemple

Le code suivant implémente un consommateur qui utilise les fonctions de consommateur de PerfLib v2 pour lire les informations de performances de l’UC à partir du CounterSet « informations sur le processeur ».

Le consommateur est organisé comme suit :

- La `CpuPerfCounters` classe implémente la logique de consommation des données de performances. Il encapsule un handle de requête et une mémoire tampon de données dans laquelle les résultats de la requête sont enregistrés.
- La `CpuPerfTimestamp` structure stocke les informations d’horodatage pour un exemple. Chaque fois que des données sont collectées, l’appelant reçoit une seule `CpuPerfTimestamp` .
- La `CpuPerfData` structure stocke les informations de performance (nom de l’instance et valeurs de performances brutes) pour un processeur. Chaque fois que des données sont collectées, l’appelant reçoit un tableau de `CpuPerfData` (un par UC).

Cet exemple utilise des valeurs GUID et ID de compteur codées en dur, car il est optimisé pour un CounterSet (informations de processeur) spécifique qui ne change pas les valeurs GUID ou ID. Une classe plus générique qui lit les données de performances à partir de countersets arbitraires doit utiliser **PerfQueryCounterSetRegistrationInfo** pour rechercher le mappage entre les ID de compteur et les valeurs de compteur au moment de l’exécution.

Un `CpuPerfCountersConsumer.cpp` programme simple montre comment utiliser les valeurs de la `CpuPerfCounters` classe.

### <a name="cpuperfcountersh"></a>CpuPerfCounters. h

```cpp
#pragma once
#include <sal.h>

// Contains timestamp data for a Processor Information data collection.
struct CpuPerfTimestamp
{
    __int64 PerfTimeStamp;   // Timestamp from the high-resolution clock.
    __int64 PerfTime100NSec; // The number of 100 nanosecond intervals since January 1, 1601, in Coordinated Universal Time (UTC).
    __int64 PerfFreq;        // The frequency of the high-resolution clock.
};

// Contains the raw data from a Processor Information sample.
// Note that the values returned are raw data. Converting from raw data to a
// friendly value may require computation, and the computation may require
// two samples of data. The computation depends on the Type, and the formula
// to use for each type can be found on MSDN.
// For example, ProcessorTime contains raw data of type PERF_100NSEC_TIMER_INV.
// Given two samples of data, s0 at time t0 and s1 at time t1, the friendly
// "% Processor Time" value is computed as:
// 100*(1-(s1.ProcessorTime-s0.ProcessorTime)/(t1.PerfTime100NSec-t0.PerfTime100NSec))
struct CpuPerfData
{
    wchar_t Name[16]; // Format: "NumaNode,NumaIndex", "NumaNode,_Total", or "_Total".
    __int64 unsigned ProcessorTime; // % Processor Time (#0, Type=PERF_100NSEC_TIMER_INV)
    __int64 unsigned UserTime; // % User Time (#1, Type=PERF_100NSEC_TIMER)
    __int64 unsigned PrivilegedTime; // % Privileged Time (#2, Type=PERF_100NSEC_TIMER)
    __int32 unsigned Interrupts; // Interrupts / sec (#3, Type=PERF_COUNTER_COUNTER)
    __int64 unsigned DpcTime; // % DPC Time (#4, Type=PERF_100NSEC_TIMER)
    __int64 unsigned InterruptTime; // % Interrupt Time (#5, Type=PERF_100NSEC_TIMER)
    __int32 unsigned DpcsQueued; // DPCs Queued / sec (#6, Type=PERF_COUNTER_COUNTER)
    __int32 unsigned Dpcs; // DPC Rate (#7, Type=PERF_COUNTER_RAWCOUNT)
    __int64 unsigned IdleTime; // % Idle Time (#8, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C1Time; // % C1 Time (#9, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C2Time; // % C2 Time (#10, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C3Time; // % C3 Time (#11, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C1Transitions; // C1 Transitions / sec (#12, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned C2Transitions; // C2 Transitions / sec (#13, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned C3Transitions; // C3 Transitions / sec (#14, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned PriorityTime; // % Priority Time (#15, Type=PERF_100NSEC_TIMER_INV)
    __int32 unsigned ParkingStatus; // Parking Status (#16, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ProcessorFrequency; // Processor Frequency (#17, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned PercentMaximumFrequency; // % of Maximum Frequency (#18, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ProcessorStateFlags; // Processor State Flags (#19, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ClockInterrupts; // Clock Interrupts / sec (#20, Type=PERF_COUNTER_COUNTER)
    __int64 unsigned AverageIdleTime; // Average Idle Time (#21, Type=PERF_PRECISION_100NS_TIMER)
    __int64 unsigned AverageIdleTimeBase; // Average Idle Time Base (#22, Type=PERF_PRECISION_TIMESTAMP)
    __int64 unsigned IdleBreakEvents; // Idle Break Events / sec (#23, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned ProcessorPerformance; // % Processor Performance (#24, Type=PERF_AVERAGE_BULK)
    __int32 unsigned ProcessorPerformanceBase; // % Processor Performance Base (#25, Type=PERF_AVERAGE_BASE)
    __int64 unsigned ProcessorUtility; // % Processor Utility (#26, Type=PERF_AVERAGE_BULK)
    __int64 unsigned PrivilegedUtility; // % Privileged Utility (#28, Type=PERF_AVERAGE_BULK)
    __int32 unsigned UtilityBase; // % Utility Base (#27, Type=PERF_AVERAGE_BASE)
    __int32 unsigned PercentPerformanceLimit; // % Performance Limit (#30, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned PerformanceLimitFlags; // Performance Limit Flags (#31, Type=PERF_COUNTER_RAWCOUNT)
};

// Performs data collection from the Processor Information performance counter.
class CpuPerfCounters
{
public:

    CpuPerfCounters(CpuPerfCounters const&) = delete;
    void operator=(CpuPerfCounters const&) = delete;

    ~CpuPerfCounters();
    CpuPerfCounters() noexcept;

    // Reads CPU performance counter data.
    // Returns ERROR_SUCCESS (0) on success, ERROR_MORE_DATA if bufferCount is
    // too small, or another Win32 error code on failure.
    _Success_(return == 0)
    unsigned
    ReadData(
        _Out_opt_ CpuPerfTimestamp* timestamp,
        _Out_cap_post_count_(bufferCount, *bufferUsed) CpuPerfData* buffer,
        unsigned bufferCount,
        _Out_ unsigned* bufferUsed) noexcept;

private:

    void* m_hQuery;
    void* m_pData;
    unsigned m_cbData;
};
```

### <a name="cpuperfcounterscpp"></a>CpuPerfCounters. cpp

```cpp
#include "CpuPerfCounters.h"
#include <windows.h>
#include <perflib.h>
#include <winperf.h>
#include <stdlib.h>

_Check_return_ _Ret_maybenull_ _Post_writable_byte_size_(cb)
static void*
AllocateBytes(unsigned cb) noexcept
{
    return malloc(cb);
}

static void
FreeBytes(_Pre_maybenull_ _Post_invalid_ void* p) noexcept
{
    if (p)
    {
        free(p);
    }
    return;
}

static void
AssignCounterValue(
    _Inout_ __int32 unsigned* pVar,
    _In_ PERF_COUNTER_DATA const* pData) noexcept
{
    if (pData->dwDataSize == 4 ||
        pData->dwDataSize == 8)
    {
        *pVar = *reinterpret_cast<__int32 unsigned const*>(pData + 1);
    }
}

static void
AssignCounterValue(
    _Inout_ __int64 unsigned* pVar,
    _In_ PERF_COUNTER_DATA const* pData) noexcept
{
    if (pData->dwDataSize == 8)
    {
        *pVar = *reinterpret_cast<__int64 unsigned const*>(pData + 1);
    }
    else if (pData->dwDataSize == 4)
    {
        *pVar = *reinterpret_cast<__int32 unsigned const*>(pData + 1);
    }
}

CpuPerfCounters::~CpuPerfCounters()
{
    if (m_hQuery)
    {
        PerfCloseQueryHandle(m_hQuery);
    }

    FreeBytes(m_pData);
}

CpuPerfCounters::CpuPerfCounters() noexcept
    : m_hQuery()
    , m_pData()
    , m_cbData()
{
    return;
}

_Success_(return == 0)
unsigned
CpuPerfCounters::ReadData(
    _Out_opt_ CpuPerfTimestamp* timestamp,
    _Out_cap_post_count_(bufferCount, *bufferUsed) CpuPerfData* buffer,
    unsigned bufferCount,
    _Out_ unsigned* bufferUsed) noexcept
{
    unsigned status;
    DWORD cbData;
    PERF_DATA_HEADER* pDataHeader;
    PERF_COUNTER_HEADER const* pCounterHeader;
    PERF_MULTI_COUNTERS const* pMultiCounters;
    PERF_MULTI_INSTANCES const* pMultiInstances;
    PERF_INSTANCE_HEADER const* pInstanceHeader;
    unsigned cInstances = 0;

    if (m_hQuery == nullptr)
    {
        HANDLE hQuery = 0;
        status = PerfOpenQueryHandle(nullptr, &hQuery);
        if (ERROR_SUCCESS != status)
        {
            goto Done;
        }

        struct
        {
            PERF_COUNTER_IDENTIFIER Identifier;
            WCHAR Name[4];
        } querySpec = {
            {
                // ProcessorCounterSetGuid
                { 0xb4fc721a, 0x378, 0x476f, 0x89, 0xba, 0xa5, 0xa7, 0x9f, 0x81, 0xb, 0x36 },
                0,
                sizeof(querySpec),
                PERF_WILDCARD_COUNTER, // Get all data for each CPU.
                0xFFFFFFFF // Get data for all instance IDs.
            },
            L"*" // Get data for all instance names.
        };

        status = PerfAddCounters(hQuery, &querySpec.Identifier, sizeof(querySpec));
        if (ERROR_SUCCESS == status)
        {
            status = querySpec.Identifier.Status;
        }

        if (ERROR_SUCCESS != status)
        {
            PerfCloseQueryHandle(hQuery);
            goto Done;
        }

        // NOTE: A program that adds more than one query to the handle would need to call
        // PerfQueryCounterInfo to determine the order of the query results.

        m_hQuery = hQuery;
    }

    for (;;)
    {
        cbData = 0;
        pDataHeader = static_cast<PERF_DATA_HEADER*>(m_pData);
        status = PerfQueryCounterData(m_hQuery, pDataHeader, m_cbData, &cbData);
        if (ERROR_SUCCESS == status)
        {
            break;
        }
        else if (ERROR_NOT_ENOUGH_MEMORY != status)
        {
            goto Done;
        }

        FreeBytes(m_pData);
        m_cbData = 0;

        m_pData = AllocateBytes(cbData);
        if (nullptr == m_pData)
        {
            status = ERROR_OUTOFMEMORY;
            goto Done;
        }

        m_cbData = cbData;
    }

    // PERF_DATA_HEADER block = PERF_DATA_HEADER + dwNumCounters PERF_COUNTER_HEADER blocks
    if (cbData < sizeof(PERF_DATA_HEADER) ||
        cbData < pDataHeader->dwTotalSize ||
        pDataHeader->dwTotalSize < sizeof(PERF_DATA_HEADER) ||
        pDataHeader->dwNumCounters != 1)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_COUNTERSET block = PERF_COUNTER_HEADER + PERF_MULTI_COUNTERS block + PERF_MULTI_INSTANCES block
    cbData = pDataHeader->dwTotalSize - sizeof(PERF_DATA_HEADER);
    pCounterHeader = reinterpret_cast<PERF_COUNTER_HEADER*>(pDataHeader + 1);
    if (cbData < sizeof(PERF_COUNTER_HEADER) ||
        cbData < pCounterHeader->dwSize ||
        pCounterHeader->dwSize < sizeof(PERF_COUNTER_HEADER) ||
        PERF_COUNTERSET != pCounterHeader->dwType)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_MULTI_COUNTERS block = PERF_MULTI_COUNTERS + dwCounters DWORDs
    cbData = pCounterHeader->dwSize - sizeof(PERF_COUNTER_HEADER);
    pMultiCounters = reinterpret_cast<PERF_MULTI_COUNTERS const*>(pCounterHeader + 1);
    if (cbData < sizeof(PERF_MULTI_COUNTERS) ||
        cbData < pMultiCounters->dwSize ||
        pMultiCounters->dwSize < sizeof(PERF_MULTI_COUNTERS) ||
        (pMultiCounters->dwSize - sizeof(PERF_MULTI_COUNTERS)) / sizeof(DWORD) < pMultiCounters->dwCounters)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_MULTI_INSTANCES block = PERF_MULTI_INSTANCES + dwInstances instance data blocks
    cbData -= pMultiCounters->dwSize;
    pMultiInstances = reinterpret_cast<PERF_MULTI_INSTANCES const*>((LPCBYTE)pMultiCounters + pMultiCounters->dwSize);
    if (cbData < sizeof(PERF_MULTI_INSTANCES) ||
        cbData < pMultiInstances->dwTotalSize ||
        pMultiInstances->dwTotalSize < sizeof(PERF_MULTI_INSTANCES))
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    cInstances = pMultiInstances->dwInstances;
    if (bufferCount < cInstances)
    {
        status = ERROR_MORE_DATA;
        goto Done;
    }

    memset(buffer, 0, sizeof(buffer[0]) * cInstances);

    cbData = pMultiInstances->dwTotalSize - sizeof(PERF_MULTI_INSTANCES);
    pInstanceHeader = reinterpret_cast<PERF_INSTANCE_HEADER const*>(pMultiInstances + 1);
    for (unsigned iInstance = 0; iInstance != pMultiInstances->dwInstances; iInstance += 1)
    {
        CpuPerfData& d = buffer[iInstance];

        // instance data block = PERF_INSTANCE_HEADER block + dwCounters PERF_COUNTER_DATA blocks
        if (cbData < sizeof(PERF_INSTANCE_HEADER) ||
            cbData < pInstanceHeader->Size ||
            pInstanceHeader->Size < sizeof(PERF_INSTANCE_HEADER))
        {
            status = ERROR_INVALID_DATA;
            goto Done;
        }

        unsigned const instanceNameMax = (pInstanceHeader->Size - sizeof(PERF_INSTANCE_HEADER)) / sizeof(WCHAR);
        WCHAR const* const instanceName = reinterpret_cast<WCHAR const*>(pInstanceHeader + 1);
        if (instanceNameMax == wcsnlen(instanceName, instanceNameMax))
        {
            status = ERROR_INVALID_DATA;
            goto Done;
        }

        wcsncpy_s(d.Name, instanceName, _TRUNCATE);

        cbData -= pInstanceHeader->Size;
        PERF_COUNTER_DATA const* pCounterData = reinterpret_cast<PERF_COUNTER_DATA const*>((LPCBYTE)pInstanceHeader + pInstanceHeader->Size);
        for (unsigned iCounter = 0; iCounter != pMultiCounters->dwCounters; iCounter += 1)
        {
            if (cbData < sizeof(PERF_COUNTER_DATA) ||
                cbData < pCounterData->dwSize ||
                pCounterData->dwSize < sizeof(PERF_COUNTER_DATA) + 8 ||
                pCounterData->dwSize - sizeof(PERF_COUNTER_DATA) < pCounterData->dwDataSize)
            {
                status = ERROR_INVALID_DATA;
                goto Done;
            }

            DWORD const* pCounterIds = reinterpret_cast<DWORD const*>(pMultiCounters + 1);
            switch (pCounterIds[iCounter])
            {
            case 0: // PERF_100NSEC_TIMER_INV
                AssignCounterValue(&d.ProcessorTime, pCounterData);
                break;
            case 1: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.UserTime, pCounterData);
                break;
            case 2: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.PrivilegedTime, pCounterData);
                break;
            case 3: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.Interrupts, pCounterData);
                break;
            case 4: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.DpcTime, pCounterData);
                break;
            case 5: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.InterruptTime, pCounterData);
                break;
            case 6: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.DpcsQueued, pCounterData);
                break;
            case 7: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.Dpcs, pCounterData);
                break;
            case 8: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.IdleTime, pCounterData);
                break;
            case 9: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C1Time, pCounterData);
                break;
            case 10: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C2Time, pCounterData);
                break;
            case 11: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C3Time, pCounterData);
                break;
            case 12: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C1Transitions, pCounterData);
                break;
            case 13: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C2Transitions, pCounterData);
                break;
            case 14: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C3Transitions, pCounterData);
                break;
            case 15: // PERF_100NSEC_TIMER_INV
                AssignCounterValue(&d.PriorityTime, pCounterData);
                break;
            case 16: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ParkingStatus, pCounterData);
                break;
            case 17: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ProcessorFrequency, pCounterData);
                break;
            case 18: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PercentMaximumFrequency, pCounterData);
                break;
            case 19: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ProcessorStateFlags, pCounterData);
                break;
            case 20: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.ClockInterrupts, pCounterData);
                break;
            case 21: // PERF_PRECISION_100NS_TIMER
                AssignCounterValue(&d.AverageIdleTime, pCounterData);
                break;
            case 22: // PERF_PRECISION_TIMESTAMP
                AssignCounterValue(&d.AverageIdleTimeBase, pCounterData);
                break;
            case 23: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.IdleBreakEvents, pCounterData);
                break;
            case 24: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.ProcessorPerformance, pCounterData);
                break;
            case 25: // PERF_AVERAGE_BASE
                AssignCounterValue(&d.ProcessorPerformanceBase, pCounterData);
                break;
            case 26: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.ProcessorUtility, pCounterData);
                break;
            case 28: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.PrivilegedUtility, pCounterData);
                break;
            case 27: // PERF_AVERAGE_BASE
                AssignCounterValue(&d.UtilityBase, pCounterData);
                break;
            case 30: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PercentPerformanceLimit, pCounterData);
                break;
            case 31: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PerformanceLimitFlags, pCounterData);
                break;
            }

            cbData -= pCounterData->dwSize;
            pCounterData = reinterpret_cast<PERF_COUNTER_DATA const*>((LPCBYTE)pCounterData + pCounterData->dwSize);
        }

        pInstanceHeader = reinterpret_cast<PERF_INSTANCE_HEADER const*>(pCounterData);
    }

    if (nullptr != timestamp)
    {
        timestamp->PerfTimeStamp = pDataHeader->PerfTimeStamp;
        timestamp->PerfTime100NSec = pDataHeader->PerfTime100NSec;
        timestamp->PerfFreq = pDataHeader->PerfFreq;
    }

    status = ERROR_SUCCESS;

Done:

    *bufferUsed = cInstances;
    return status;
}
```

### <a name="cpuperfcountersconsumercpp"></a>CpuPerfCountersConsumer. cpp

```cpp
#include <windows.h>
#include <stdio.h>
#include "CpuPerfCounters.h"
#include <utility>

int wmain()
{
    unsigned status;
    unsigned const dataMax = 30; // Support up to 30 instances
    CpuPerfCounters cpc;
    CpuPerfTimestamp timestamp[2];
    CpuPerfTimestamp* t0 = timestamp + 0;
    CpuPerfTimestamp* t1 = timestamp + 1;
    CpuPerfData data[dataMax * 2];
    CpuPerfData* d0 = data + 0;
    CpuPerfData* d1 = data + dataMax;
    unsigned used;

    status = cpc.ReadData(t0, d0, dataMax, &used);
    printf("ReadData0 used=%u, status=%u\n", used, status);

    for (unsigned iSample = 1; iSample != 10; iSample += 1)
    {
        Sleep(1000);
        status = cpc.ReadData(t1, d1, dataMax, &used);
        printf("ReadData%u used=%u, status=%u\n", iSample, used, status);

        if (status == ERROR_SUCCESS && used != 0)
        {
            // Show the ProcessorTime value from instance #0 (usually the "_Total" instance):
            auto& s0 = d0[0];
            auto& s1 = d1[0];
            printf("  %ls/%ls = %f\n", s0.Name, s1.Name,
                100.0 * (1.0 - static_cast<double>(s1.ProcessorTime - s0.ProcessorTime) / static_cast<double>(t1->PerfTime100NSec - t0->PerfTime100NSec)));

            std::swap(t0, t1); // Swap "current" and "previous" timestamp pointers.
            std::swap(d0, d1); // Swap "current" and "previous" sample pointers.
        }
    }

    return status;
}
```
