---
description: Classe de type d’événement pour l’événement d’en-tête du fichier journal. Cette classe contient des informations sur la session de suivi d’événements.
ms.assetid: 3d0c4044-da06-4850-95c4-99b4ea28fcd9
title: Classe EventTrace_Header
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace_Header
- EventTrace_Header.BufferSize
- EventTrace_Header.Version
- EventTrace_Header.ProviderVersion
- EventTrace_Header.NumberOfProcessors
- EventTrace_Header.EndTime
- EventTrace_Header.TimerResolution
- EventTrace_Header.MaxFileSize
- EventTrace_Header.LogFileMode
- EventTrace_Header.BuffersWritten
- EventTrace_Header.StartBuffers
- EventTrace_Header.PointerSize
- EventTrace_Header.EventsLost
- EventTrace_Header.CPUSpeed
- EventTrace_Header.LoggerName
- EventTrace_Header.LogFileName
- EventTrace_Header.TimeZoneInformation
- EventTrace_Header.BootTime
- EventTrace_Header.PerfFreq
- EventTrace_Header.StartTime
- EventTrace_Header.ReservedFlags
- EventTrace_Header.BuffersLost
api_type:
- NA
api_location: ''
ms.openlocfilehash: a5d0515b9d7d720409e0a72aec7aad5dc54561637563976a35d03b3e0dec79f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829989"
---
# <a name="eventtrace_header-class"></a>\_Classe d’en-tête EventTrace

Classe de type d’événement pour l’événement d’en-tête du fichier journal. Cette classe contient des informations sur la session de suivi d’événements.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(0)]
class EventTrace_Header : EventTraceEvent
{
  uint32 BufferSize;
  uint32 Version;
  uint32 ProviderVersion;
  uint32 NumberOfProcessors;
  uint64 EndTime;
  uint32 TimerResolution;
  uint32 MaxFileSize;
  uint32 LogFileMode;
  uint32 BuffersWritten;
  uint32 StartBuffers;
  uint32 PointerSize;
  uint32 EventsLost;
  uint32 CPUSpeed;
  uint32 LoggerName;
  uint32 LogFileName;
  uint8  TimeZoneInformation[];
  uint64 BootTime;
  uint64 PerfFreq;
  uint64 StartTime;
  uint32 ReservedFlags;
  uint32 BuffersLost;
};
```

## <a name="members"></a>Membres

La classe d' **\_ en-tête EventTrace** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe d' **\_ en-tête EventTrace** a ces propriétés.

<dl> <dt>

**BootTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (17)
</dt> </dl>

Heure à laquelle le système a été démarré, en intervalles de 100 nanosecondes depuis le 1er janvier 1601 à minuit.

</dd> <dt>

**BufferSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (1)
</dt> </dl>

Taille des tampons de la session de suivi d’événements, en kilo-octets.

</dd> <dt>

**BuffersLost**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (21)
</dt> </dl>

Nombre total de mémoires tampons perdues.

</dd> <dt>

**BuffersWritten**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (9)
</dt> </dl>

Nombre total de mémoires tampons écrites par la session de suivi d’événements.

</dd> <dt>

**CPUSpeed**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (13)
</dt> </dl>

Vitesse du processeur, en mégahertz.

**Windows 2000 :** Non pris en charge.

</dd> <dt>

**EndTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (5)
</dt> </dl>

Heure à laquelle la session de suivi d’événements s’est arrêtée, en intervalles de 100 nanosecondes depuis le 1er janvier 1601 à minuit. Cette valeur peut être 0 si vous consommez des événements en temps réel ou à partir d’un fichier journal dans lequel le fournit des événements de journalisation continue.

</dd> <dt>

**EventsLost**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (12)
</dt> </dl>

Nombre d’événements perdus pendant la session de suivi d’événements.

</dd> <dt>

**LogFileMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (8), **format ("x")**
</dt> </dl>

Mode de journalisation actuel pour la session de suivi d’événements. Pour obtenir la liste des valeurs, consultez constantes de mode de journalisation.

</dd> <dt>

**Nomdefichierjournal**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (15), **pointeur**
</dt> </dl>

Nom du fichier journal de suivi d’événements qui contient les événements.

</dd> <dt>

**LoggerName**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (14), **pointeur**
</dt> </dl>

Nom de la session de suivi d’événements.

</dd> <dt>

**MaxFileSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (7)
</dt> </dl>

Taille maximale du fichier journal, en mégaoctets.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (4)
</dt> </dl>

Nombre de processeurs sur le système.

</dd> <dt>

**PerfFreq**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (18)
</dt> </dl>

Fréquence du compteur de performance haute résolution, s’il en existe un.

</dd> <dt>

**PointerSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (11)
</dt> </dl>

Taille du type de données du pointeur, en octets.

</dd> <dt>

**ProviderVersion**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (3)
</dt> </dl>

Numéro de build du système d’exploitation.

</dd> <dt>

**ReservedFlags**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (20)
</dt> </dl>

Réservé.

</dd> <dt>

**StartBuffers**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (10)
</dt> </dl>

Réservé.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (19)
</dt> </dl>

Heure de début de la session de suivi d’événements, en intervalles de 100 nanosecondes depuis le 1er janvier 1601 à minuit.

</dd> <dt>

**TimerResolution**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (6)
</dt> </dl>

Résolution de la minuterie matérielle, en unités de 100 nanosecondes.

</dd> <dt>

**TimeZoneInformation**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (16), **extension (« noprint »)**, **Max** (176)
</dt> </dl>

Structure [**d' \_ \_ informations de fuseau horaire**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) qui contient le fuseau horaire pour les membres **BootTime**, **EndTime** et **StartTime** .

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (2)
</dt> </dl>

Numéro de version du système d’exploitation. À partir des octets de poids faible, les deux premiers octets contiennent la version principale, les deux octets suivants contiennent une version mineure, les deux octets suivants contiennent Service Pack version principale et les deux derniers octets contiennent Service Pack version mineure.

</dd> </dl>

## <a name="remarks"></a>Remarques

En règle générale, vous souhaitez enregistrer les valeurs des propriétés suivantes pour une utilisation ultérieure lors du traitement des événements à partir du fichier journal.

-   **TimerResolution**: à utiliser avec les membres **KernelTime** et **UserTime** de la structure d' [**\_ \_ en-tête de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) pour déterminer le coût de l’UC pour un ensemble d’instructions. Pour plus d’informations, consultez la section Notes de l' [**\_ \_ en-tête de suivi d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).
-   **PointerSize**: pour les propriétés qui contiennent le qualificateur de **pointeur** , utilisez cette valeur pour déterminer la taille du pointeur. Notez que cette valeur peut ne pas être exacte. Par exemple, sur un ordinateur 64 bits, une application 32 bits enregistre les pointeurs de 4 octets ; Toutefois, la session affecte la valeur 8 à **PointerSize** .
-   **LogFileMode**: permet de déterminer si cette session est une session privée d’enregistreur d’événements. Certaines propriétés ne contiennent pas de données pour les sessions privées des journaux. Par exemple, les membres **KernelTime** et **UserTime** de la structure d' [**\_ \_ en-tête de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**EventTraceEvent**](eventtraceevent.md)
</dt> <dt>

[**\_ \_ en-tête du fichier journal de suivi**](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header)
</dt> </dl>

 

 
