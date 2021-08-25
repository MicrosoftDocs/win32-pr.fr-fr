---
description: Une session de suivi d’événements privée est une session de suivi d’événements en mode utilisateur qui s’exécute dans le même processus que ses fournisseurs de suivi d’événements&\# 8212 ; la session privée et les fournisseurs qu’elle active doivent tous être dans le même processus.
ms.assetid: fb6a3899-194e-4cb7-b9e5-a7ff85fb7891
title: Configuration et démarrage d’une session de journalisation privée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cf15db05c03e5a412cf07ee6e020d2321380f2d48abba465669dc807729fe38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901499"
---
# <a name="configuring-and-starting-a-private-logger-session"></a>Configuration et démarrage d’une session de journalisation privée

Une session de suivi d’événements privée est une session de suivi d’événements en mode utilisateur qui s’exécute dans le même processus que ses fournisseurs de suivi d’événements : la session privée et les fournisseurs qu’elle active doivent tous être dans le même processus. L’avantage de l’utilisation d’une session privée est que la session privée ne compte pas au maximum de 64 sessions de suivi d’événements s’exécutant simultanément.

La configuration et le démarrage d’une session privée sont similaires au démarrage d’une session de suivi d’événements normale. La différence réside dans le fait que le membre **Wnode. Guid** de la structure des [**\_ \_ Propriétés de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) doit contenir le **GUID** du fournisseur, et non la session, et que le fournisseur doit déjà avoir inscrit le GUID. Notez que si vous définissez également le \_ suivi \_ d’événement privé \_ en mode de \_ journalisation de procédure, vous pouvez utiliser un **GUID** différent pour la session et le fournisseur. Pour plus d’informations sur le démarrage d’une session de suivi d’événements normale, consultez [configuration et démarrage d’une session de suivi d’événements](configuring-and-starting-an-event-tracing-session.md).

Notez que vous ne pouvez pas démarrer, arrêter ou vider une session de trace privée à partir de DllMain ; vous devez le faire dans les routines d’initialisation et de finalisation de la DLL.

de Windows 8.1 à Windows 10, la version 1607, la charge utile d’événement, la portée et les filtres de parcours de pile peuvent être utilisés par la fonction [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) et les structures de [**\_ \_ descripteur de filtre d’événement**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) et de [**\_ \_ paramètres de TRACE**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) pour filtrer sur des conditions spécifiques dans une session de journalisation. Pour plus d’informations sur les filtres de charge utile d’événement, consultez les fonctions [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)et [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) , ainsi que les structures de prédicat **activer les \_ \_ paramètres de trace**, **\_ \_ descripteur de filtre d’événement** et de [**\_ filtre \_ de charge utile**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) .

à partir de Windows 10, la version 1703, les utilisateurs à faibles privilèges peuvent désormais démarrer une session d’enregistreur d’événements privée dans les processus qu’ils ont démarré. Le fournisseur n’a plus besoin d’être inscrit avant l’activation ou le démarrage de la session privée, ce qui signifie que le fournisseur est « pré-activé », de la même façon que les fournisseurs de session non privés. Il existe une limite de 8 enregistreurs d’événements privés au niveau du système pour un processus individuel. Pour des performances accrues dans les scénarios inter-processus, il est recommandé d’utiliser le filtrage pour les API de session (notamment [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea), [**QueryTrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace), [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)et [**StopTrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) lors du démarrage d’un enregistreur d’événements privés du système. Notez que les mêmes filtres doivent être passés à toutes les API de session. Pour plus d’informations sur les filtres, consultez [**Event \_ trace \_ Properties \_ v2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).

Pour plus d’informations sur le démarrage d’une session de suivi d’événements, consultez [configuration et démarrage d’une session de suivi d’événements](configuring-and-starting-an-event-tracing-session.md).

Pour plus d’informations sur le démarrage d’une session de journal de noyau NT, consultez [configuration et démarrage de la session de journalisation du noyau NT](configuring-and-starting-the-nt-kernel-logger-session.md).

Pour plus d’informations sur le démarrage d’une session de journalisation globale, consultez [configuration et démarrage d’une session de journalisation globale](configuring-and-starting-the-global-logger-session.md).

Pour plus d’informations sur le démarrage d’une session de journalisation automatique, consultez [configuration et démarrage d’une session de journalisation](configuring-and-starting-an-autologger-session.md)automatique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration et démarrage d’une session SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configuration et démarrage d’une session de journalisation automatique](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configuration et démarrage d’une session de suivi d’événements](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Configuration et démarrage de la session de journalisation du noyau NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**ACTIVER \_ les \_ paramètres de trace**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**Propriétés de la trace d’événements \_ \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**Propriétés de la trace d’événements \_ \_ \_ v2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
</dt> <dt>

[**descripteur de filtre d’événements \_ \_**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**\_prédicat de filtre de charge utile \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Mise à jour d’une session de suivi d’événements](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
