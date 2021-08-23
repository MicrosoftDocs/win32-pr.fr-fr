---
description: Classe de base abstraite pour les classes de données calculées préinstallées.
ms.assetid: 4eb6ad42-0f68-44f4-be19-095c51b4b1b6
ms.tgt_platform: multiple
title: Classe Win32_PerfFormattedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfFormattedData
- Win32_PerfFormattedData.Caption
- Win32_PerfFormattedData.Description
- Win32_PerfFormattedData.Name
- Win32_PerfFormattedData.Frequency_Object
- Win32_PerfFormattedData.Frequency_PerfTime
- Win32_PerfFormattedData.Frequency_Sys100NS
- Win32_PerfFormattedData.Timestamp_Object
- Win32_PerfFormattedData.Timestamp_PerfTime
- Win32_PerfFormattedData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: 55a765102d5fcc40caff41a7fa68184afea114838152dd84157d506a62c15da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020137"
---
# <a name="win32_perfformatteddata-class"></a>\_Classe PerfFormattedData Win32

Classe de base abstraite pour les classes de données calculées préinstallées. Un exemple d’une telle classe est [**le \_ \_ \_ disque logique Win32 PerfFormattedData Perfdisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md). ces classes contiennent des valeurs calculées fournies par le Fournisseur de données de performances haute performance [mis en forme](../wmisdk/formatted-performance-data-provider.md).

La syntaxe suivante est simplifiée à partir du code MOF et montre toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[abstract, AMENDMENT]
class Win32_PerfFormattedData : Win32_Perf
{
  string Caption;
  string Description;
  string Name;
  uint64 Frequency_Object;
  uint64 Frequency_PerfTime;
  uint64 Frequency_Sys100NS;
  uint64 Timestamp_Object;
  uint64 Timestamp_PerfTime;
  uint64 Timestamp_Sys100NS;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ PerfFormattedData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ PerfFormattedData** a ces propriétés.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Description textuelle courte pour la statistique ou la métrique.

Cette propriété est héritée de la [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description textuelle de la statistique ou métrique.

Cette propriété est héritée de la [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).

</dd> <dt>

**\_Objet Frequency**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fréquence en graduations par seconde de la propriété de l' **\_ objet timestamp** . Lorsqu’il est sous-classé, le fournisseur définit cette propriété.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

Cette propriété est héritée de la [**\_ performance Win32**](win32-perf.md).

</dd> <dt>

**Fréquence \_ PerfTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fréquence en graduations par seconde de la propriété **Frequency \_ PerfTime** . une valeur peut être obtenue en appelant la fonction Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

Cette propriété est héritée de la [**\_ performance Win32**](win32-perf.md).

</dd> <dt>

**Fréquence \_ Sys100NS**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fréquence en graduations par seconde de la propriété **timestamp \_ Sys100NS** (10 millions).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

Cette propriété est héritée de la [**\_ performance Win32**](win32-perf.md).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Étiquette par laquelle la statistique ou la métrique est connue. Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.

Cette propriété est héritée de la [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).

</dd> <dt>

**Timestamp, \_ objet**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Horodatage défini par l’objet. Le fournisseur définit sa propriété.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

Cette propriété est héritée de la [**\_ performance Win32**](win32-perf.md).

</dd> <dt>

**Horodateur \_ PerfTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Horodateur du compteur de performances élevé. une valeur peut être obtenue en appelant la fonction Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

Cette propriété est héritée de la [**\_ performance Win32**](win32-perf.md).

</dd> <dt>

**Horodateur \_ Sys100NS**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur d’horodatage en unités de nanosecondes de 100.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

Cette propriété est héritée de la [**\_ performance Win32**](win32-perf.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ PerfFormattedData** est dérivée de la [**\_ performance Win32**](win32-perf.md), qui est dérivée de [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md). La classe se trouve dans l’espace de noms **\\ cimv2 racine** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                             |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>WmiPerfInst.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Performances Win32**](win32-perf.md)
</dt> <dt>

[Classes du compteur de performances](performance-counter-classes.md)
</dt> <dt>

[Accès aux classes de performance préinstallées par WMI](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Tâches WMI : analyse des performances](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Accès aux données de performances dans le script](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
