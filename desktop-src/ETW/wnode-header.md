---
description: La \_ structure d’en-tête WNODE est un membre de la structure des propriétés de trace d’événements \_ \_ .
ms.assetid: 862a8f46-a326-48c6-92b7-8bb667837bb7
title: Structure WNODE_HEADER (Wmistr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WNODE_HEADER
api_type:
- HeaderDef
api_location:
- Wmistr.h
ms.openlocfilehash: e8ad8bd5e1fd4917fa031e7553ed0e7e460244b8ab7c7da347a62d7430036cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015237"
---
# <a name="wnode_header-structure"></a>\_Structure d’en-tête WNODE

La structure d' **\_ en-tête WNODE** est un membre de la structure des [**\_ \_ Propriétés de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WNODE_HEADER {
  ULONG BufferSize;
  ULONG ProviderId;
  union {
    ULONG64 HistoricalContext;
    struct {
      ULONG Version;
      ULONG Linkage;
    };
  };
  union {
    HANDLE        KernelHandle;
    LARGE_INTEGER TimeStamp;
  };
  GUID  Guid;
  ULONG ClientContext;
  ULONG Flags;
} WNODE_HEADER, *PWNODE_HEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**BufferSize**
</dt> <dd>

Taille totale de la mémoire allouée, en octets, pour les propriétés de session de suivi d’événements. La taille de la mémoire doit inclure la place de la structure des [**\_ \_ Propriétés**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) de la trace d’événements plus la chaîne de nom de session et la chaîne de nom de fichier journal qui suivent la structure en mémoire.

</dd> <dt>

**ProviderId**
</dt> <dd>

Réservé à un usage interne.

</dd> <dt>

**HistoricalContext**
</dt> <dd>

Lors de la sortie, handle vers la session de suivi d’événements.

</dd> <dt>

**Version**
</dt> <dd>

Réservé à un usage interne.

</dd> <dt>

**Liaison**
</dt> <dd>

Réservé à un usage interne.

</dd> <dt>

**KernelHandle**
</dt> <dd>

Réservé à un usage interne.

</dd> <dt>

**Confirmé**
</dt> <dd>

Heure à laquelle les informations de cette structure ont été mises à jour, en intervalles de 100 nanosecondes depuis le 1er janvier 1601 à minuit.

</dd> <dt>

**Guid**
</dt> <dd>

GUID que vous définissez pour la session.

Pour une session de journal de noyau NT, définissez ce membre sur **SystemTraceControlGuid**.

Si ce membre a la valeur **SystemTraceControlGuid** ou **GlobalLoggerGuid**, l’enregistreur d’événements est un journal système.

Pour une session d’enregistreur d’événements privée, définissez ce membre sur le GUID du fournisseur que vous allez activer pour la session.

Si vous démarrez une session qui n’est pas une session de journalisation de noyau ou privée, vous n’êtes pas obligé de spécifier un GUID de session. Si vous ne spécifiez pas de GUID, ETW en crée un pour vous. Vous devez spécifier un GUID de session uniquement si vous souhaitez modifier les autorisations par défaut associées à une session spécifique. Pour plus d’informations, consultez la fonction EventAccessControl.

Vous ne pouvez pas démarrer plusieurs sessions avec le même GUID de session.

**avant Windows Vista :** Vous pouvez démarrer plusieurs sessions avec le même GUID de session.

</dd> <dt>

**ClientContext**
</dt> <dd>

Résolution d’horloge à utiliser lors de la journalisation de l’horodatage pour chaque événement. La valeur par défaut est le compteur de performance des requêtes (QPC).

**avant Windows Vista :** La valeur par défaut est l’heure système.

**avant Windows 10, version 1703 :** Deux types d’horloge distincts ne peuvent pas être utilisés simultanément par les enregistreurs d’événements système.

**à partir de Windows 10, version 1703 :** La restriction de type d’horloge a été supprimée. Les trois types d’horloge peuvent maintenant être utilisés simultanément par les enregistreurs d’événements système.

Vous pouvez spécifier l’une des valeurs suivantes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt>1</dt> </dl></td>
<td>Compteur de performance des requêtes (QPC). Le compteur QPC fournit un horodatage haute résolution qui n’est pas affecté par les réglages de l’horloge système. L’horodatage stocké dans l’événement est équivalent à la valeur retournée par l’API QueryPerformanceCounter. Pour plus d’informations sur les caractéristiques de cet horodatage, consultez <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">acquisition d’horodatages haute résolution</a>.<br/> Vous devez utiliser cette résolution si vous avez des taux d’événements élevés ou si le consommateur fusionne les événements à partir de mémoires tampons différentes. Dans ces cas, la précision et la stabilité de l’horodatage QPC permettent une meilleure précision de l’ordonnancement des événements à partir de mémoires tampons différentes. Toutefois, l’horodatage QPC ne reflète pas les mises à jour de l’horloge système, par exemple, si l’horloge système est avancée en raison de la synchronisation avec un serveur NTP pendant que la trace est en cours, les horodatages QPC dans la trace continuent de refléter le temps comme si aucune mise à jour n’avait eu lieu.<br/> Pour déterminer la résolution, utilisez le membre <strong>PerfFreq</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> lors de l’utilisation de l’événement.<br/> Pour convertir l’horodatage d’un événement en unités 100-ns, utilisez la formule de conversion suivante : <br/> scaledTimestamp = eventRecord. EventHeader. TimeStamp. QuadPart * 10000000,0/logfileHeader. PerfFreq. QuadPart<br/> Notez que sur les ordinateurs plus anciens, l’horodatage peut ne pas être précis, car le compteur ignore parfois les transferts en raison d’erreurs matérielles.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>2</dt> </dl></td>
<td>Heure système. L’heure système fournit un horodatage qui effectue le suivi des modifications apportées à l’horloge du système, par exemple, si l’horloge système est avancée en raison de la synchronisation avec un serveur NTP pendant que la trace est en cours, les horodatages de l’heure système dans la trace se poursuivent également pour correspondre au nouveau paramètre de l’horloge système. <br/>
<ul>
<li>sur les systèmes antérieurs à Windows 10, l’horodatage stocké dans l’événement est équivalent à la valeur retournée par l’API GetSystemTimeAsFileTime.</li>
<li>sur Windows 10 ou version ultérieure, l’horodatage stocké dans l’événement est équivalent à la valeur retournée par l’API GetSystemTimePreciseAsFileTime.</li>
</ul>
avant Windows 10, la résolution de cet horodatage était la résolution d’un cycle d’horloge système, comme indiqué par le membre TimerResolution de TRACE_LOGFILE_HEADER. à partir de Windows 10, la résolution de cet horodatage correspond à la résolution du compteur de performances, comme indiqué par le membre PerfFreq de TRACE_LOGFILE_HEADER.<br/> Pour convertir l’horodatage d’un événement en unités 100-ns, utilisez la formule de conversion suivante : <br/> scaledTimestamp = eventRecord. EventHeader. TimeStamp. QuadPart<br/> notez que lorsque les événements sont capturés sur un système exécutant un système d’exploitation antérieur à Windows 10, si le volume d’événements est élevé, la résolution de l’heure système peut ne pas être suffisamment précise pour déterminer la séquence d’événements. Dans ce cas, un ensemble d’événements aura le même horodatage, mais l’ordre dans lequel ETW remet les événements peut ne pas être correct. à partir de Windows 10, l’horodatage est capturé avec une précision supplémentaire, même si une certaine instabilité peut encore se produire dans les cas où l’horloge système a été réglée lors de la capture de la trace.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>1,3</dt> </dl></td>
<td>Compteur du cycle de l’UC. Le compteur UC fournit l’horodatage de résolution le plus élevé et est le moins gourmand en ressources à récupérer. Toutefois, le compteur UC n’est pas fiable et ne doit pas être utilisé en production. Par exemple, sur certains ordinateurs, les minuteurs changent de fréquence en raison des modifications de la température et de l’alimentation, en plus de s’arrêter dans certains États.<br/> Pour déterminer la résolution, utilisez le membre <strong>CpuSpeedInMHz</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> lors de l’utilisation de l’événement.<br/> Si votre matériel ne prend pas en charge ce type d’horloge, ETW utilise l’heure système.<br/> <strong>Windows Server 2003, Windows xp avec SP1 et Windows xp :</strong> cette valeur n’est pas prise en charge, elle a été introduite dans Windows Server 2003 avec SP1 et Windows XP avec SP2.<br/></td>
</tr>
</tbody>
</table>



 

**Windows 2000 :** Le membre **ClientContext** n’est pas pris en charge.

</dd> <dt>

**Indicateurs**
</dt> <dd>

Doit contenir **le \_ \_ \_ GUID suivi de l’indicateur WNODE** pour indiquer que la structure contient des informations de suivi d’événements.

</dd> </dl>

## <a name="remarks"></a>Remarques

Veillez à initialiser la mémoire pour cette structure à zéro avant de définir les membres.

Pour convertir un horodatage ETW en FILETIME, utilisez la procédure suivante :

<dl> 1. Pour chaque session ou fichier journal en cours de traitement (par exemple, pour chaque journal de suivi d’événements \_ \_ ), consultez le champ logfile. ProcessTraceMode pour déterminer si l' \_ indicateur de datage brut du mode de trace du processus \_ \_ \_ est défini. Par défaut, cet indicateur n’est pas défini. Si cet indicateur n’est pas défini, le runtime ETW convertit automatiquement l’horodateur de chaque enregistrement d’événement \_ en FILETIME avant d’envoyer l' \_ enregistrement d’événement à votre fonction EventRecordCallback, de sorte qu’aucun traitement supplémentaire n’est nécessaire. Les étapes suivantes doivent être utilisées uniquement si la trace est en cours de traitement avec \_ l' \_ indicateur d’horodateur brut du mode de trace processus \_ \_ défini.  
2. Pour chaque session ou fichier journal en cours de traitement (par exemple, pour chaque journal de suivi d’événements \_ \_ ), consultez le champ logfile. LogfileHeader. ReservedFlags pour déterminer l’échelle de l’horodatage du fichier journal. En fonction de la valeur de ReservedFlags, effectuez l’une des étapes suivantes pour déterminer la valeur à utiliser pour timeStampScale dans les étapes restantes : <dl> a. Si ReservedFlags = = 1 (QPC) : DOUBLE timeStampScale = 10000000,0/logFile. LogfileHeader. PerfFreq. QuadPart ;  
b. Si ReservedFlags = = 2 (heure système) : DOUBLE timeStampScale = 1,0 ;  
Notez que les étapes restantes ne sont pas nécessaires pour les événements qui utilisent l’heure système, car les événements fournissent déjà leurs horodatages dans les unités FILETIME. Les étapes restantes fonctionnent, mais elles ne sont pas nécessaires et introduisent une petite erreur d’arrondi.  
c. Si ReservedFlags = = 3 (compteur de cycle UC) : DOUBLE timeStampScale = 10,0/logFile. LogfileHeader. CpuSpeedInMHz ;  
</dl> </dd> 3. On the FIRST call to your EventRecordCallback function for a particular log file, use data from the logFile (EVENT\_TRACE\_LOGFILE) and from the eventRecord (EVENT\_RECORD) to compute the timeStampBase that will be used for the remaining events in the log file: INT64 timeStampBase = logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
4. For each eventRecord (EVENT\_RECORD), convert the event’s timestamp into FILETIME as follows, using the timeStampScale and timeStampBase values calculated in steps 2 and 3: INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
</dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications Windows 2000 Professional \[ desktop apps \| UWP\]<br/>                   |
| Serveur minimal pris en charge<br/> | applications de bureau Windows 2000 Server apps-applications \[ \| UWP\]<br/>                         |
| En-tête<br/>                   | <dl> <dt>Wmistr. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[*ControlCallback*](/windows/win32/api/evntrace/nc-evntrace-wmidprequest)
</dt> <dt>

[**Propriétés de la trace d’événements \_ \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle)
</dt> <dt>

[**\_entier long**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)
</dt> </dl>

 

 
