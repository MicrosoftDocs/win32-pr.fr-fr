---
description: Spécifiez les informations relatives à l’objet de performance auquel la classe de compteur de performance WMI est mappée.
ms.assetid: 7b8b7f00-95d8-4c1e-8638-157d0f4c7c32
ms.tgt_platform: multiple
title: Qualificateurs de classe pour les classes de compteurs de performances
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b8168dcc0523c629202ac4d5c4a0ea51ecc8bd68d5ac4498fb38059b940fd83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820094"
---
# <a name="class-qualifiers-for-performance-counter-classes"></a>Qualificateurs de classe pour les classes de compteurs de performances

Les qualificateurs de classe spécifient des informations sur l’objet de performance auquel la [classe de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI est mappée. Pour plus d’informations, consultez [analyse des données de performances](monitoring-performance-data.md).

-   [Qualificateurs pour les PerformanceClasses bruts et mis en forme](#qualifiers-for-raw-and-formatted-performanceclasses)
-   [Qualificateurs pour les classes de performances brutes](#)
-   [Qualificateurs pour les classes de performance mises en forme](#)
-   [Rubriques connexes](#related-topics)


Compteur de performances : les qualificateurs spécifiques sont automatiquement attachés par le fournisseur « WbemPerfClass » aux classes et propriétés [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) dans le \\ cimv2 racine.

Ces informations s’appliquent à toutes les instances de la classe. Certains qualificateurs avec des valeurs **booléennes** qui ont toujours la **valeur false** peuvent ne pas être présents sur des classes spécifiques.

## <a name="qualifiers-for-raw-and-formatted-performanceclasses"></a>Qualificateurs pour les PerformanceClasses bruts et mis en forme

Les qualificateurs suivants s’appliquent à toutes les classes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Cuisson**
</dt> <dd>

**boolean**

Indique si la classe contient des données cuisinées.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**NomComplet**
</dt> <dd>

**string**

Nom de l’objet de performance. Pour plus d’informations, consultez [Compteurs de performances](/windows/desktop/PerfCtrs/performance-counters-portal).

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**
</dt> <dd>

**sint32**

Ne fournit pas de données de détail. Contient toujours la valeur 100.

</dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Dynamique**
</dt> <dd>

**boolean**

Toujours défini sur **true** , car les instances sont toujours dynamiques.

</dd> <dt>

<span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**
</dt> <dd>

**boolean**

Indique si la classe provient d’une bibliothèque de performance héritée. Toujours défini sur **true**.

</dd> <dt>

<span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**
</dt> <dd>

**sint32**

Les index ne sont plus valides. Ce qualificateur est toujours égal à zéro.

</dd> <dt>

<span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf** 
</dt> <dd>

**boolean**

Indique que la classe est une classe haute performance. Toujours défini sur **true**.

</dd> <dt>

<span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Paramètres régionaux**
</dt> <dd>

**sint32**

Identificateur de paramètres régionaux. La valeur est toujours 1033 (anglais des États-Unis).

</dd> <dt>

<span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**
</dt> <dd>

**int32**

Les index ne sont plus valides. Ce qualificateur est toujours égal à zéro.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Moteur**
</dt> <dd>

**string**

Nom du fournisseur d’instance. La valeur est « WbemPerfV2 ».

</dd> <dt>

<span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**
</dt> <dd>

**string**

Nom du pilote dans la clé **de \_ \_ \\ CurrentControlSet \\ services de l’ordinateur local** , sous laquelle la clé de performance peut être localisée. Ce nom est également le nom du service qui fournit le compteur de performance.

</dd> <dt>

<span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**
</dt> <dd>

**boolean**

Si la **valeur est true**, indique qu’il n’existe qu’une seule instance de la classe.

</dd> </dl>

## <a name="qualifiers-for-raw-performance-classes"></a>Qualificateurs pour les classes de performances brutes

Les qualificateurs suivants s’appliquent à toutes les classes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).

<dl> <dt>

<span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Réduis**
</dt> <dd>

**boolean**

Indique si l’obtention d’instances de cette classe est une opération coûteuse. Affectez toujours la valeur **true** pour les classes avec « \_ coûteux » ajouté à la fin du nom de la classe.

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**
</dt> <dd>

**uint32**

Ne fournit pas de données de détail. Contient toujours la valeur 100.

</dd> <dt>

<span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**
</dt> <dd>

**boolean**

La valeur est toujours **false**.

</dd> </dl>

## <a name="qualifiers-for-formatted-performance-classes"></a>Qualificateurs pour les classes de performance mises en forme

Les qualificateurs suivants s’appliquent à toutes les classes dérivées de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**Cook automatique**
</dt> <dd>

**int32**

Indique que les valeurs des instances de classe sont calculées automatiquement à partir de la classe de données brutes correspondante. La valeur est toujours 1.

</dd> <dt>

<span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**RawClass autocook \_**
</dt> <dd>

**string**

Nom de la classe brute à utiliser pour le calcul de la classe mise en forme. Ce qualificateur est requis.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Analyse des données de performances](monitoring-performance-data.md)
</dt> <dt>

[Qualificateurs spécifiques aux classes de performance WMI](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[Classes du compteur de performances](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Accès aux classes de performance préinstallées par WMI](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Tâches WMI : analyse des performances](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
