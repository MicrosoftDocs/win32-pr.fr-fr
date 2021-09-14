---
description: Les consommateurs de suivi d’événements peuvent traiter les événements d’un ou de plusieurs fournisseurs.
ms.assetid: 039a9f66-228e-4258-9967-2b2cd7d31091
title: Consommation d’événements (traçage d’événements)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad8234cc66d07b5a52c10ab39c7d7b3c8aa029
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007442"
---
# <a name="consuming-events-event-tracing"></a>Consommation d’événements (traçage d’événements)

Les consommateurs de suivi d’événements peuvent traiter les événements d’un ou de plusieurs fournisseurs. Les consommateurs peuvent traiter des événements à partir d’un fichier journal ou en temps réel. Vous pouvez consommer des événements en temps réel uniquement si le contrôleur spécifie le mode de journalisation en temps réel pour la session. pour des raisons de performances, le traitement en temps réel n’est pas recommandé avant Windows Vista.

Pour spécifier la session de trace à partir de laquelle vous souhaitez traiter les événements, vous utilisez la structure du [**\_ \_ fichier journal de suivi d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) . Vous devez initialiser une copie de cette structure pour chaque fichier journal ou session en temps réel que vous souhaitez traiter.

Pour consommer des événements à partir d’un fichier journal, définissez le membre **LogFileName** sur le nom du fichier journal. Pour consommer des événements à partir d’une session en temps réel, définissez le membre **LoggerName** sur le nom de session. Vous utilisez également cette structure pour spécifier le rappel [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) et le rappel [*EventCallback suivante*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback) ou [**EventRecordCallback**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback) utilisé pour traiter les événements.

-   [**EventRecordCallback**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback): reçoit et traite tous les événements (y compris l’événement d’en-tête) à partir d’un ou de plusieurs fichiers journaux et d’une session en temps réel. Vous implémentez ce rappel si vous utilisez les fonctions d’assistance des données de trace pour analyser les données d’événement ou si vous souhaitez récupérer les métadonnées relatives à l’événement.
-   [*EventCallback suivante*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback): reçoit et traite tous les événements (y compris l’événement d’en-tête) à partir d’un ou de plusieurs fichiers journaux et d’une session en temps réel.
-   [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka): reçoit et traite les informations récapitulatives relatives à la mémoire tampon actuelle, comme les événements perdus. ETW appelle le rappel après la transmission de tous les événements de la mémoire tampon au consommateur. Le consommateur peut également utiliser ce rappel pour annuler le traitement des événements. Toutefois, si vous consommez des événements en temps réel, ETW remet les événements jusqu’à ce que le contrôleur arrête la session.

Après avoir défini une ou plusieurs sessions de suivi, appelez la fonction [**OpenTrace**](/windows/win32/api/evntrace/nf-evntrace-opentracea) pour chaque session de trace que vous souhaitez traiter. vous pouvez traiter les événements à partir d’un ou de plusieurs fichiers journaux, mais à partir d’une seule session en temps réel. Vous transmettez ensuite la liste des handles de session de suivi que **OpenTrace** retourne à la fonction [**ProcessTrace**](/windows/win32/api/evntrace/nf-evntrace-processtrace) . La fonction **ProcessTrace** combine les événements, les trie par ordre chronologique, puis les remet aux rappels un par un. Les événements peuvent être filtrés pour n’inclure que ceux qui appartiennent à un laps de temps spécifique à l’aide des paramètres *StartTime* et *EndTime* . La fonction **ProcessTrace** bloque le thread jusqu’à ce que votre consommateur traite tous les événements dans les sessions de trace, [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) retourne la **valeur false** ou que vous appelez [**CloseTrace**](/windows/win32/api/evntrace/nf-evntrace-closetrace).

**avant Windows Vista :** Vous pouvez appeler [**CloseTrace**](/windows/win32/api/evntrace/nf-evntrace-closetrace) uniquement après le retour de [**ProcessTrace**](/windows/win32/api/evntrace/nf-evntrace-processtrace) .

Pour obtenir un exemple qui montre comment utiliser des événements publiés à l’aide d’un manifeste, de fichiers MOF ou TMF, consultez [extraction de données d’événement à l’aide de Tdh](retrieving-event-data-using-tdh.md). notez qu’à partir de Windows Vista, vous devez utiliser les fonctions d’assistance des données de trace (TDH) pour consommer des événements.

Pour obtenir un exemple qui montre comment consommer des événements publiés à l’aide de MOF, consultez [extraction de données d’événement à l’aide de MOF](retrieving-event-data-using-mof.md).

 

 
