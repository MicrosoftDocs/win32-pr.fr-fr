---
description: Classe de base abstraite pour toutes les classes de compteur de performances brutes concrètes.
ms.assetid: 3c457996-54d9-4425-8a57-15176d027e3a
ms.tgt_platform: multiple
title: Classe Win32_PerfRawData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfRawData
- Win32_PerfRawData.Caption
- Win32_PerfRawData.Description
- Win32_PerfRawData.Name
- Win32_PerfRawData.Frequency_Object
- Win32_PerfRawData.Frequency_PerfTime
- Win32_PerfRawData.Frequency_Sys100NS
- Win32_PerfRawData.Timestamp_Object
- Win32_PerfRawData.Timestamp_PerfTime
- Win32_PerfRawData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: f6500706b7e2298ad98aa894e33436b0306e406e003562fcb6533265abd0b2be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020127"
---
# <a name="win32_perfrawdata-class"></a>\_Classe PerfRawData Win32

Classe de base abstraite pour toutes les classes de compteur de performances brutes concrètes.

Pour apparaître dans le moniteur système, les classes de compteur de performance doivent être ajoutées à l' \\ espace de noms CIMV2 racine et dérivées de **Win32 \_ PerfRawData**. Les données de ces classes sont fournies par le fournisseur de [compteurs de performances](../wmisdk/performance-counter-provider.md)hautes performances.

Les propriétés suivantes sont héritées lorsqu’une classe est dérivée de **Win32 \_ PerfRawData**:

-   **Horodateur \_ PerfTime**
-   **Horodateur \_ Sys100NS**
-   **Timestamp, \_ objet**
-   **Fréquence \_ PerfTime**
-   **Fréquence \_ Sys100NS**
-   **\_Objet Frequency**

Dans chaque cas, les propriétés doivent être remplies par le fournisseur ou la classe ne peut pas être affichée dans le moniteur système. Ces propriétés sont utilisées pour calculer des formules de type de compteur par les consommateurs de données de performances.

La syntaxe suivante est simplifiée à partir du code MOF et montre toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[abstract, AMENDMENT]
class Win32_PerfRawData : Win32_Perf
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

La classe **Win32 \_ PerfRawData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ PerfRawData** a ces propriétés.

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

La classe **Win32 \_ PerfRawData** est dérivée de la [**\_ performance Win32**](win32-perf.md), qui est dérivée de [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).

Toutes les classes dérivées de la [**\_ performance Win32**](win32-perf.md) sont conçues pour être utilisées avec un objet [*actualisateur*](../wmisdk/gloss-r.md) . Pour plus d’informations sur la création et l’utilisation d’un objet actualisateur dans le langage de programmation C++, consultez [accès aux données de performances en c++](../wmisdk/accessing-performance-data-in-c--.md). Pour plus d’informations sur la création et l’utilisation d’un objet actualisateur dans un langage de programmation de scripts, consultez [actualisation des données WMI dans des scripts](../wmisdk/refreshing-wmi-data-in-scripts.md).

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

 

 
