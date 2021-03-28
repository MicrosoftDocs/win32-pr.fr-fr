---
description: Les fournisseurs classiques utilisent la fonction TraceEventInstance pour suivre les événements qui font partie d’une transaction unique. Vous pouvez également utiliser cette fonction pour tracer les événements parent/enfant.
ms.assetid: 246e9443-3120-49bf-a6e3-64dddba348fa
title: Écriture d’événements connexes dans un fournisseur Classic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771b08a66625d5cd6e723fbc2e12eed87bd1d434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321106"
---
# <a name="writing-related-events-in-a-classic-provider"></a>Écriture d’événements connexes dans un fournisseur Classic

Les fournisseurs [classiques](about-event-tracing.md) utilisent la fonction [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) pour suivre les événements qui font partie d’une transaction unique. Vous pouvez également utiliser cette fonction pour tracer les événements parent/enfant.

Avant d’appeler la fonction [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) , vous devez d’abord appeler la fonction [**CreateTraceInstanceId**](/windows/win32/api/evntrace/nf-evntrace-createtraceinstanceid) pour obtenir un identificateur de transaction. Cette fonction génère un identificateur de transaction unique et le mappe à un handle de GUID de classe inscrit. Les descripteurs des GUID de classe inscrits sont disponibles dans les membres **RegHandle** des structures d' [**inscription de \_ GUID \_ de trace**](/windows/win32/api/evntrace/ns-evntrace-trace_guid_registration) , après l’appel de la fonction [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) . L’identificateur de transaction est placé dans le membre **InstanceID** d’une structure d' [**\_ \_ informations d’instance d’événement**](/windows/win32/api/evntrace/ns-evntrace-event_instance_info) que vous transmettez à la fonction **CreateTraceInstanceId** .

La structure d' [**\_ \_ en-tête**](/windows/win32/api/evntrace/ns-evntrace-event_instance_header) de l’instance d’événement qui est passée à la fonction [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) est similaire à la structure d' [**\_ \_ en-tête de suivi d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) (consultez suivi des [événements](tracing-events.md)), à la différence qu’elle contient des informations supplémentaires relatives aux instances et ne contient pas de membre **GUID** .

Les instances d’événements peuvent être utilisées pour établir une relation hiérarchique entre les événements. La fonction [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) accepte les informations spécifiques à l’instance de deux instances d’événement. Le paramètre *pInstInfo* pointe vers la structure d' [**\_ \_ informations**](/windows/win32/api/evntrace/ns-evntrace-event_instance_info) de l’instance d’événement de l’instance de l’événement, et le paramètre *pParentInstInfo* pointe vers la structure d’informations de l' **\_ instance \_ d’événement** d’une instance d’événement parent. La définition d’une instance d’événement « parent » est définie par l’application ; le parent peut être n’importe quelle instance déjà générée.

 

 
