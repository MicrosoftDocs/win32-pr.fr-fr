---
description: Chaque journal dans la clé EventLog contient des sous-clés appelées sources d’événements. La source de l’événement est le nom du logiciel qui enregistre l’événement.
ms.assetid: bc7fdc74-be41-4d17-997c-27171ef73f0f
title: Sources de l’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2b408b76cdbc6e93e44099fea2842f9655a963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544800"
---
# <a name="event-sources"></a>Sources de l’événement

Chaque journal dans la [clé EventLog](eventlog-key.md) contient des sous-clés appelées *sources d’événements*. La source de l’événement est le nom du logiciel qui enregistre l’événement. Il s’agit généralement du nom de l’application ou du nom d’un sous-composant de l’application si l’application est volumineuse. Vous pouvez ajouter au maximum 16 384 sources d’événements au registre. Le journal de **sécurité** est réservé à l’usage du système. Les pilotes de périphérique doivent ajouter leurs noms dans le journal **système** . Les applications et les services doivent ajouter leurs noms au journal des **applications** ou créer un journal personnalisé.

La structure des sources d’événements est la suivante :

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            EventLog
               Application
                  AppName
               Security
               System
                  DriverName
               CustomLog
                  AppName
```

Vous ne pouvez pas utiliser un nom de source qui a déjà été utilisé comme nom de journal. En outre, les noms de source ne peuvent pas être hiérarchiques ; autrement dit, ils ne peuvent pas contenir de barre oblique inverse (« \\ »).

Chaque source d’événement contient des informations (par exemple, un [fichier de message](message-files.md)) spécifiques au logiciel qui consignera les événements, comme indiqué dans le tableau suivant.



<table>
<thead>
<tr class="header">
<th>Valeur de Registre</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CategoryCount</strong></td>
<td>Nombre de catégories d’événements prises en charge. Cette valeur est de type <strong>REG_DWORD</strong>.</td>
</tr>
<tr class="even">
<td><strong>CategoryMessageFile</strong></td>
<td>Chemin d’accès au fichier de message de catégorie. Un fichier de message de catégorie contient des chaînes dépendantes de la langue qui décrivent les catégories. Cette valeur peut être de type <strong>REG_SZ</strong> ou <strong>REG_EXPAND_SZ</strong>.</td>
</tr>
<tr class="odd">
<td><strong>EventMessageFile</strong></td>
<td>Chemin d’accès à un ou plusieurs fichiers de messages d’événement ; Utilisez un point-virgule pour délimiter plusieurs fichiers. Un fichier de message d’événement contient des chaînes dépendantes de la langue qui décrivent les événements. Cette valeur peut être de type <strong>REG_SZ</strong> ou <strong>REG_EXPAND_SZ</strong>.</td>
</tr>
<tr class="even">
<td><strong>ParameterMessageFile</strong></td>
<td>Chemin d’accès au fichier de messages de paramètres. Un fichier de message de paramètre contient des chaînes indépendantes du langage qui doivent être insérées dans les chaînes de description de l’événement. Cette valeur peut être de type <strong>REG_SZ</strong> ou <strong>REG_EXPAND_SZ</strong>.</td>
</tr>
<tr class="odd">
<td><strong>TypesSupported</strong></td>
<td>Masque de rébinaire des types pris en charge. Cette valeur est de type <strong>REG_DWORD</strong>. Il peut s’agir d’une ou plusieurs des valeurs suivantes : <dl> <strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)<br />
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)<br />
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)<br />
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)<br />
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)<br />
</dl></td>
</tr>
</tbody>
</table>



 

Lorsqu’une application utilise la fonction [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) ou [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) pour obtenir un handle vers un journal des événements, le service de journalisation des événements recherche la source d’événement spécifiée dans le registre. Par exemple, le journal des **applications** peut contenir des sources d’événements pour Microsoft SQL Server et Microsoft Excel. Si une application utilise [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) ou **OpenEventLog** avec un nom source d’application, SQL ou Excel, le service de journalisation des événements retourne un handle au journal des **applications** .

Une application peut utiliser le journal des **applications** sans ajouter une nouvelle source d’événement au registre. Si l’application appelle [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) et transmet un nom de source qui est introuvable dans le registre, le service de journalisation des événements utilise par défaut le journal des **applications** . Toutefois, étant donné qu’il n’y a aucun fichier de message, les observateur d’événements ne peuvent pas mapper d’identificateurs d’événements ou de catégories d’événements à une chaîne de description, et affichent une erreur. Pour cette raison, vous devez ajouter une source d’événement unique au registre pour votre application et spécifier un fichier de message.

 

 



