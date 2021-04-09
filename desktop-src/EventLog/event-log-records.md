---
description: Les informations relatives à chaque événement sont stockées dans le journal des événements dans un enregistrement du journal des événements. L’enregistrement du journal des événements contient des informations sur l’heure, le type et la catégorie. Pour plus d’informations, consultez la structure EVENTLOGRECORD.
ms.assetid: 73731505-97f5-4985-8d00-c6ce8604902d
title: Enregistrements du journal des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cc6caf1011c06eda0dca240bb7a3478c549827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864249"
---
# <a name="event-log-records"></a>Enregistrements du journal des événements

Les informations relatives à chaque événement sont stockées dans le journal des événements dans un *enregistrement du journal des événements*. L’enregistrement du journal des événements contient des informations sur l’heure, le type et la catégorie. Pour plus d’informations, consultez la structure [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) .

Le membre **recordNumber** de [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) contient le numéro d’enregistrement de l’enregistrement du journal des événements. Le premier enregistrement écrit dans un journal des événements est le numéro d’enregistrement 1, et les autres enregistrements sont numérotés séquentiellement. Si le numéro d’enregistrement atteint ULONG \_ Max, le numéro d’enregistrement suivant est 0, pas 1 ; Toutefois, vous utilisez zéro pour Rechercher l’enregistrement.

Si la valeur de registre de [rétention](eventlog-key.md) est définie sur zéro, les enregistrements d’événement sont remplacés lorsque la taille maximale du journal est atteinte. Par conséquent, l’enregistrement le plus ancien dans un journal des événements ne peut pas être le numéro 1. Pour identifier l’enregistrement le plus ancien dans le journal, appelez la fonction [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) . Vous pouvez ensuite appeler la fonction [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) et ajouter la valeur retournée au numéro d’enregistrement le plus ancien pour déterminer l’enregistrement le plus récent.

Vous pouvez lire des enregistrements individuels à partir du journal des événements à l’aide de la fonction [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) . Pour plus d’informations, consultez [interrogation des informations sur les événements](querying-for-event-source-messages.md).

 

 



