---
description: Cette section décrit les nouvelles fonctionnalités qui ont été ajoutées à Suivi d’v nements pour Windows dans chaque version.
ms.assetid: 5d94a6d2-2280-4a97-aa5a-c9ca2c016c84
title: Nouveautés du suivi d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613433834e5a11f2886b6ee314fdb60114f66976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753029"
---
# <a name="whats-new-in-event-tracing"></a>Nouveautés du suivi d’événements

Cette section décrit les nouvelles fonctionnalités qui ont été ajoutées à Suivi d’v nements pour Windows dans chaque version.

## <a name="windows-10-version-1709"></a>Windows 10, version 1709

ETW peut désormais éventuellement suivre des binaires pour tous les fournisseurs qui sont activés pour la session. Le suivi s’applique rétroactivement aux fournisseurs qui ont été activés pour la session avant l’appel, ainsi qu’à tous les futurs fournisseurs activés pour la session. Vous pouvez également interroger le nombre maximal actuellement configuré d’enregistreurs système autorisés par le système d’exploitation. Pour plus d’informations, consultez les valeurs **TraceProviderBinaryTracking** et **TraceMaxLoggersQuery** de l’énumération des [**classes d' \_ informations \_ de trace**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) , ainsi que la récupération de [données de suivi d’événements supplémentaires](retrieving-additional-event-tracing-data.md).

ETW peut désormais filtrer les événements en fonction du nom de l’événement. Vous pouvez également déterminer quels événements obtiennent leurs piles. Pour plus d’informations, consultez les valeurs de type de filtre d’événement **\_ \_ \_ \_ nom d’événement**, type de filtre d' **événement \_ \_ \_ STACKWALK \_ nom** et **type de filtre d’événement STACKWALK valeurs de \_ \_ \_ \_ niveau \_ kW** de la structure de [**\_ \_ descripteur de filtre d’événement**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) , ainsi que le [**\_ \_ \_ nom d’événement de filtre**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_name) d’événement associé et les structures [**\_ \_ \_ kW de niveau de filtre d’événement**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_level_kw) .

## <a name="windows-10"></a>Windows 10

[TraceLogging](../tracelogging/trace-logging-portal.md) s’appuie sur ETW et fournit un moyen simplifié d’instrumenter le code pour les développeurs natifs, .net et WinRT. TraceLogging vous permet d’inclure des données structurées avec des événements, de mettre en corrélation des événements et ne requiert pas de fichier XML de manifeste d’instrumentation distinct.

Les [caractéristiques du fournisseur](provider-traits.md) ont été ajoutées en tant que méthode d’attachement d’un plus grand nombre de données à l’inscription d’un fournisseur individuel. Elles peuvent être utilisées pour les fournisseurs TraceLogging ou basés sur un manifeste. Cela comprend actuellement la prise en charge de l’ajout d’un nom de fournisseur et/ou d’un groupe de fournisseurs à l’inscription d’un fournisseur individuel. Les groupes de fournisseurs sont une nouvelle fonctionnalité qui permet de contrôler plusieurs fournisseurs ETW dans l’agrégat par le groupe auquel ils appartiennent.

L’état de capture périodique est un moyen d’autoriser régulièrement l’envoi des notifications d’état de capture aux fournisseurs. Quand cette option est activée, les notifications sont envoyées uniquement aux inscriptions du fournisseur qui ont été activées précédemment pour la session active. Chaque fournisseur peut définir sa propre réponse (le cas échéant) à une notification. Pour plus d’informations sur l’implémentation, consultez [**trace \_ periodly \_ capture \_ State \_ info**](/windows/win32/api/evntrace/ns-evntrace-trace_periodic_capture_state_info).

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 et Windows Server 2012 R2

Les fonctionnalités suivantes ont été ajoutées au suivi d’événements sur Windows 8.1 et Windows Server 2012 R2.

Les fonctions qui prennent en charge l’utilisation de la charge utile d’événement, la portée et les filtres de parcours de pile utilisés par la fonction [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) et les structures [**activer les \_ \_ paramètres de trace**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) et [**\_ \_ descripteurs de filtre d’événement**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) pour filtrer sur des conditions spécifiques dans une session de journalisation. Pour plus d'informations, consultez les pages suivantes :

-   [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
-   [**TdhCleanupPayloadEventFilterDescriptor**](/windows/desktop/api/Tdh/nf-tdh-tdhcleanuppayloadeventfilterdescriptor)
-   [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
-   [**TdhDeletePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhdeletepayloadfilter)

En outre, consultez la documentation largement révisée pour la fonction [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) et les structures [**activer les \_ \_ paramètres de trace**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) et le [**\_ \_ descripteur de filtre d’événement**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) utilisées par ces fonctionnalités.

Structure qui définit un prédicat de filtre de charge utile d’événement qui décrit comment filtrer sur un champ unique dans une session de trace utilisée par la nouvelle fonction [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter) et une nouvelle structure utilisée par l’ID d’événement et les filtres de parcours de pile. Pour plus d'informations, consultez les pages suivantes :

-   [**\_ID d' \_ événement de filtre d’événements \_**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_id)
-   [**\_prédicat de filtre de charge utile \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

Fonctions qui récupèrent des informations sur les événements présents dans le manifeste du fournisseur. Pour plus d'informations, consultez les pages suivantes :

-   [**TdhEnumerateManifestProviderEvents**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents)
-   [**TdhGetManifestEventInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhgetmanifesteventinformation)

Structure qui définit un tableau d’événements dans un manifeste de fournisseur utilisé par la nouvelle fonction [**TdhEnumerateManifestProviderEvents**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents) . Pour plus d'informations, consultez les pages suivantes :

-   [**\_informations sur l’événement du fournisseur \_**](/windows/desktop/api/Tdh/ns-tdh-provider_event_info)

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 et Windows Server 2012

Les fonctionnalités suivantes ont été ajoutées au suivi d’événements sur Windows 8 et Windows Server 2012.

Les fonctions qui effectuent des opérations sur un objet d’inscription, fournissent l’analyse de la charge utile d’événement, fournissent l’exploration des fournisseurs de suivi, interrogent les paramètres de session de suivi d’événements et traitent un fichier de trace reconnecté. Pour plus d'informations, consultez les pages suivantes :

-   [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation)
-   [**TdhCloseDecodingHandle**](/windows/desktop/api/Tdh/nf-tdh-tdhclosedecodinghandle)
-   [**TdhGetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhgetdecodingparameter)
-   [**TdhGetWppProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppproperty)
-   [**TdhGetWppMessage**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppmessage)
-   [**TdhLoadManifestFromBinary**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifestfrombinary)
-   [**TdhOpenDecodingHandle**](/windows/desktop/api/Tdh/nf-tdh-tdhopendecodinghandle)
-   [**TdhSetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter)
-   [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation)

Les interfaces qui fournissent des informations au journal sur le processus de suivi et le moment où les événements sont enregistrés, l’accès aux données pour un événement spécifique et l’accès aux fonctionnalités de rejournalisation qui autorisent la manipulation de fichiers de journal de suivi d’événements (ETL). Pour plus d'informations, consultez les pages suivantes :

-   [**ITraceEvent**](/windows/desktop/api/Relogger/nn-relogger-itraceevent)
-   [**ITraceEventCallback**](/windows/desktop/api/Relogger/nn-relogger-itraceeventcallback)
-   [**ITraceRelogger**](/windows/desktop/api/Relogger/nn-relogger-itracerelogger)

Énumérations supplémentaires utilisées par les nouvelles fonctions et interfaces. Pour plus d'informations, consultez les pages suivantes :

-   [**\_classe d’informations d’événement \_**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class)
-   [**\_classe d' \_ informations de requête de trace \_**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 et Windows Server 2008 R2

Les fonctionnalités suivantes ont été ajoutées dans cette version :

-   La possibilité pour les fournisseurs de définir des filtres dans le manifeste. Dans Windows Vista, les contrôleurs pouvaient transmettre des données de filtre au fournisseur. Toutefois, la mise en page des données de filtre n’a pas été définie dans le manifeste, de sorte que le fournisseur doit utiliser d’autres moyens pour fournir la définition de filtre aux contrôleurs. Avec cette version, les fournisseurs peuvent définir la définition de filtre dans le manifeste (consultez l’attribut **Filters** du type complexe [**ProviderType**](../wes/eventmanifestschema-providertype-complextype.md) ). Les contrôleurs peuvent ensuite utiliser la fonction [**TdhEnumerateProviderFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters) pour déterminer la définition de filtre. Les fournisseurs qui utilisent des filtres doivent utiliser la fonction [**EventWriteEx**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) pour écrire l’événement.
-   La possibilité d’utiliser une seule mémoire tampon pour collecter des événements générés sur plusieurs processeurs. L’utilisation d’une seule mémoire tampon élimine les événements qui apparaissent dans le désordre sur les ordinateurs multiprocesseurs. Pour plus d’informations, consultez le mode de journalisation de la [**\_ mise en \_ \_ \_ \_ mémoire tampon non par processeur**](logging-mode-constants.md) . Par défaut, ETW utilise des mémoires tampons par processeur.
-   Possibilité de capturer une trace de la pile pour les événements. Pour activer le suivi de pile pour les événements de noyau, consultez la fonction [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) . Pour activer le suivi de pile pour les événements utilisateur, consultez l’indicateur de trace de la pile des propriétés d’activation d’événement pour le membre **EnableProperty** de l’option [**activer les \_ \_ paramètres de trace**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters). **\_ \_ \_ \_**
-   La possibilité de spécifier le **\_ mode de \_ mise \_ en mémoire tampon de trace** d’événements ou le mode de **\_ fichier de trace d' \_ \_ \_ événements** mode de journalisation avec le mode de journalisation **privé du \_ \_ \_ journal \_** des événements de suivi d’événements (voir [constantes de mode de journalisation](logging-mode-constants.md)).
-   La possibilité d’activer un fournisseur de façon synchrone. Par défaut, les fournisseurs sont activés de manière asynchrone. Pour activer un fournisseur de façon synchrone, définissez le paramètre *timeout* de [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).
-   Capacité du contrôleur à demander que le fournisseur enregistre son état. Pour plus d’informations, consultez l’indicateur d’état de capture du  code de contrôle d' **événement \_ \_ \_ \_** pour le paramètre ControlCode de [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).
-   La possibilité pour les consommateurs de mettre en forme les données d’événement à l’aide de la fonction [**TdhFormatProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty) .
-   Possibilité de décoder des événements manifestes sur des ordinateurs qui ne contiennent pas le fournisseur. Pour plus d’informations, consultez la fonction [**TdhLoadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest) .

Les fonctions suivantes ont été ajoutées dans cette version :

-   [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
-   [**EventWriteEx**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex)
-   [**TdhEnumerateProviderFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters)
-   [**TdhFormatProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty)
-   [**TdhLoadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest)
-   [**TdhUnloadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhunloadmanifest)
-   [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)

Les structures suivantes ont été ajoutées dans cette version :

-   [**\_ID d’événement classique \_**](/windows/win32/api/evntrace/ns-evntrace-classic_event_id)
-   [**ACTIVER \_ les \_ paramètres de trace**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
-   [**TRACE32 de pile des éléments d’événements \_ étendus \_ \_ \_**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace32)
-   [**TRACE64 de pile des éléments d’événements \_ étendus \_ \_ \_**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace64)
-   [**\_ \_ en-tête de filtre d’événement**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_header)
-   [**\_informations de filtre du fournisseur \_**](/windows/desktop/api/Tdh/ns-tdh-provider_filter_info)

Les énumérations suivantes ont été ajoutées dans cette version :

-   [**\_classe d’informations de trace \_**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

Les classes MOF suivantes ont été ajoutées dans cette version :

-   [**StackWalk**](stackwalk.md)
-   [**\_Événement StackWalk**](stackwalk-event.md)

 

 
