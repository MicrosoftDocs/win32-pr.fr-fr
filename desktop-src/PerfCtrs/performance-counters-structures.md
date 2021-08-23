---
description: Vous utilisez les structures suivantes lorsque vous travaillez avec des données de performances.
ms.assetid: 97118b64-3a2f-49c0-92e7-324df08bdb12
title: Structures des compteurs de performance
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 00e9a505a9fe74592f571f3db108af2247a6d44889bc3ddbc2e4dae0844600b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674749"
---
# <a name="performance-counters-structures"></a>Structures des compteurs de performance

Vous utilisez les structures suivantes lorsque vous travaillez avec des données de performances.

Pour plus d’informations sur les fonctions qui sont disponibles pour l’utilisation des compteurs de performance, consultez [fonctions des compteurs de performances](performance-counters-functions.md).

## <a name="performance-data-helper-pdh-structures"></a>Structures d’assistance des données de performance (PDH)

Les consommateurs qui utilisent les fonctions [d’assistance des données de performance (PDH)](using-the-pdh-functions-to-consume-counter-data.md) utilisent les structures suivantes :

- [**PDH \_ Parcourir \_ DLG \_ config**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a)
- [**PDH \_ Parcourir \_ DLG \_ config \_ H**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_ha)
- [**\_informations sur le compteur PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_info_a)
- [**\_éléments du \_ chemin d’accès au compteur PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)
- [**\_éléments du \_ \_ chemin d' \_ accès de l’élément de données PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_data_item_path_elements_a)
- [**PDH \_ fmt \_ COUNTERVALUE**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue)
- [**\_ \_ élément COUNTERVALUE de la fmt PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue_item_a)
- [**\_compteur brut \_ PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)
- [**\_élément de \_ compteur \_ brut PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter_item_a)
- [**\_enregistrement de \_ journal \_ brut PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_log_record)
- [**\_statistiques PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics)
- [**\_informations de temps PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info)

## <a name="perflib-v2-consumer-structures"></a>Structures de consommateur PerfLib v2

Les consommateurs qui utilisent les fonctions de [consommateur de Perflib v2](using-the-perflib-functions-to-consume-counter-data.md) utilisent les structures suivantes :

- [**\_données du compteur de performances \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_data)
- [**\_ \_ en-tête de compteur de performances**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_header)
- [**\_identificateur du compteur de performances \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identifier)
- [**\_informations de \_ Registre du compteur de performances \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_reg_info)
- [**\_ \_ informations sur le registre de performance COUNTERSET \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_reg_info)
- [**\_ \_ en-tête de données perf**](/windows/desktop/api/Perflib/ns-perflib-perf_data_header)
- [**\_ \_ en-tête d’instance perf**](/windows/desktop/api/Perflib/ns-perflib-perf_instance_header)
- [**\_compteurs multiples de performances \_**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_counters)
- [**\_instances multiples \_ perf**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_instances)
- [**\_ \_ en-tête de mémoire tampon de chaîne perf \_**](/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header)
- [**\_ \_ en-tête de compteur de chaîne perf \_**](/windows/win32/api/perflib/ns-perflib-perf_string_counter_header)

## <a name="perflib-v2-provider-structures"></a>Structures du fournisseur PerfLib v2

Les [fournisseurs de données de performances v2](providing-counter-data-using-version-2-0.md) utilisent les structures suivantes :

- [**\_identité du compteur de performances \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [**\_informations sur le compteur de performances \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [**\_informations du COUNTERSET de performance \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [**\_instance du COUNTERSET de performance \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)
- [**\_contexte du fournisseur de performances \_**](/windows/win32/api/perflib/ns-perflib-perf_provider_context)

## <a name="performance-dll-structures"></a>Structures de DLL de performance

Les [fournisseurs de DLL d’extension de performance](providing-counter-data-using-a-performance-dll.md) et les [consommateurs qui utilisent les fonctions de Registre pour consommer des données de compteur](using-the-registry-functions-to-consume-counter-data.md) utilisent les structures suivantes :

- [**\_bloc de compteur de performances \_**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block)
- [**\_définition du compteur de performances \_**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)
- [**\_bloc de données perf \_**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block)
- [**définition de l' \_ instance perf \_**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition)
- [**\_type d’objet perf \_**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type)
