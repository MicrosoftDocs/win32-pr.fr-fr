---
description: 'Il s’agit d’une vue d’ensemble de ce qui doit s’attendre pour le trajet de bout en bout d’un événement pour chacune des quatre technologies de suivi fournies par Microsoft : TraceLogging, basé sur un manifeste, WPP et MOF.'
ms.assetid: 6102593C-C6D5-4BDB-A0EF-067AF91DE00B
title: Vue d’ensemble des métadonnées d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c16853ef2639fd560f5b5da30447556119ec877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484361"
---
# <a name="event-metadata-overview"></a>Vue d’ensemble des métadonnées d’événement

Il s’agit d’une vue d’ensemble de ce qui doit s’attendre pour le trajet de bout en bout d’un événement pour chacune des quatre technologies de suivi fournies par Microsoft : [TraceLogging](../tracelogging/trace-logging-about.md), [basé sur un manifeste](writing-manifest-based-events.md), [WPP](windows-software-trace-preprocessor.md)et [MOF](tracing-events.md). Il aborde le problème lié à la charge utile d’un événement individuel et aux métadonnées associées qui décrivent sa structure, ce qui permet de décoder ultérieurement l’événement en éléments de données sensibles. Il est important de comprendre le parcours de chaque élément d’un événement lors du choix de la technologie de suivi appropriée pour un projet. Il n’y a pas de solution unique et adaptée à la trace.

## <a name="event-payloads"></a>Charges utiles d’événement

Pour l’une des technologies de suivi fournies par Microsoft, lors de l’appel de la commande Write (par exemple, [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) pour un manifeste ou [**TraceLoggingWrite**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) pour TraceLogging), les données fournies pour l’événement au moment de l’exécution sont repliées en un objet blob binaire contigu appelé la charge utile d’événement. Cela est indépendant du schéma d’événement ou des métadonnées d’événement (voir ci-dessous), qui décrit la disposition de cet objet blob binaire pour le décodage d’outils. La façon dont la génération de la charge utile d’événement se produit dépend de la technologie de suivi utilisée et de la fin de l’événement classique (style [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) ) ou moderne (style **EventWrite** ).

Pour les événements classiques, l’indicateur dans l' [**\_ \_ en-tête de trace**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) de l’événement est passé dans [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) qui détermine la façon dont cela se produit :

\- Si **l' \_ indicateur WNODE \_ use \_ MOF \_ ptr** est spécifié, un tableau [**de \_ champs MOF**](/windows/win32/api/evntrace/ns-evntrace-mof_field) suit [**l' \_ \_ en-tête de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) en mémoire. Le runtime ETW concatène les données d’événement telles qu’elles sont spécifiées dans ces champs pour former la charge utile d’événement.

\- Si **l' \_ indicateur WNODE \_ use \_ MOF \_ ptr** n’est pas spécifié, la charge utile d’événement est construite par l’utilisateur directement en mémoire après l' [**\_ \_ en-tête de suivi d’événement**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).

MOF et WPP sont des fournisseurs classiques. Toutefois, l’implémentation WPP s’occupe de tout cela pour vous.

Pour les événements non classiques, un certain nombre [**de \_ \_ descripteurs de données d’événement**](/windows/desktop/api/Evntprov/ns-evntprov-event_data_descriptor) sont passés dans [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite). Le runtime ETW concatène les données d’événement telles qu’elles sont spécifiées dans ces descripteurs pour former la charge utile d’événement.

Les technologies basées sur un manifeste et les technologies TraceLogging sont généralement des fournisseurs modernes. Avec un manifeste, si vous laissez mc.exe générer un code de journalisation pour vous (la MU ou le commutateur de km), la génération de charge utile est prise en charge pour vous. La génération de charge utile est toujours prise en charge par TraceLogging.

Le résultat final est qu’une charge utile pour un événement est générée au moment de l’exécution. Toutes les charges utiles sont fondamentalement similaires en ce qu’il s’agit d’objets BLOB binaires de données contenant uniquement les données de champ pour cet événement particulier, quelle que soit la technologie de suivi utilisée et les types de champ pris en charge par cette technologie de suivi. Sans les métadonnées d’événement, la charge utile d’événement est sans signification et tiennent.

Le droit du runtime ETW est ensuite de transporter cet objet blob d’événements du fournisseur au consommateur, où il est à nouveau associé à ses métadonnées et devient décodable. Le runtime ETW ajoute un peu de métadonnées supplémentaires indiquant les circonstances de la charge utile (par exemple, l’horodatage, l’ID de thread et les mots clés de l’événement). Ces informations s’appliquent à la façon dont l’événement a été routé via le runtime, et elles sont également utiles pour comprendre l’identité et le contexte de l’événement au moment du décodage. Elle est finalement exposée dans le cadre du [**\_ suivi d’événement**](/windows/win32/api/evntrace/ns-evntrace-event_trace) ou de l' [**\_ enregistrement d’événement**](/windows/win32/api/evntcons/ns-evntcons-event_record) pour le consommateur.

## <a name="event-metadata"></a>Métadonnées d’événement

Le parcours des métadonnées d’événement est différent selon la technologie de suivi utilisée, et il s’agit de l’une des plus grandes considérations à prendre en compte lors de la comparaison de chaque technologie.

### <a name="mof"></a>MOF

Les métadonnées d’événement sont créées manuellement par le créateur de l’événement sous la forme d’un schéma MOF spécial dans un fichier. mof. Le schéma créé doit correspondre à la charge utile enregistrée pour que l’événement soit correctement décodé par les consommateurs. Les décodeurs d’événements requièrent que le fichier. mof soit enregistré sur le système à l’aide de [mofcomp.exe](../wmisdk/mofcomp.md). Pour plus d’informations sur la publication de schémas MOF, consultez [publication de votre schéma d’événement pour un fournisseur classique](publishing-your-event-schema-for-a-classic-provider.md).

### <a name="wpp"></a>WPP

Les métadonnées d’événement sont automatiquement générées et stockées dans le fichier. pdb de votre fichier binaire par tracewpp.exe pendant le processus de génération. Ces métadonnées peuvent être extraites ultérieurement sous la forme d’un fichier. TMF autonome par le biais de tracepdb.exe. Les décodeurs d’événements requièrent généralement le fichier. pdb ou. TMF. Pour plus d’informations sur les tracepdb.exe, consultez [vue d’ensemble de Tracepdb](/windows-hardware/drivers/devtest/tracepdb-overview), et pour plus d’informations sur tracewpp.exe, consultez [tâche TraceWPP](/windows-hardware/drivers/devtest/tracewpp-task).

### <a name="manifest-based"></a>Basé sur un manifeste

Les définitions d’événements sont créées dans un fichier. Man. Les manifestes d’événements sont exécutés par le compilateur du manifeste ([mc.exe](../wes/message-compiler--mc-exe-.md)), générant les en-têtes nécessaires à la compilation source ainsi qu’à plusieurs fichiers de ressources binaires. bin. Ces fichiers de ressources doivent ensuite être compilés en tant que ressources dans un fichier binaire et le fichier binaire résultant placé sur le système qui envisage de décoder les événements de ce fournisseur basé sur un manifeste. En outre, le manifeste doit être installé sur le système à l’aide de [wevtutil.exe](../wes/windows-event-log-tools.md) le plus important, les attributs **resourceFileName** et **messageFileName** de l’élément XML du fournisseur dans le manifeste d’événements installé doivent identifier correctement le chemin d’accès absolu complet au fichier binaire dans lequel les fichiers de ressources ont été placés. Notez que ces chemins d’accès peuvent être remplacés au moment de l’installation du manifeste à l’aide des commutateurs wevtutil.exe/RF et/MF. Un système qui n’a pas été correctement et entièrement exécuté ces étapes ne pourra pas décoder les événements de ce fournisseur. Les décodeurs d’événements nécessitent donc un manifeste installé et le fichier binaire avec les ressources associées installées à l’emplacement spécifié par les chemins d’accès aux ressources et aux fichiers de messages. Pour plus d’informations sur la publication de schémas basés sur un manifeste, consultez [publication de votre schéma d’événement pour un fournisseur basé sur un manifeste](publishing-your-event-schema-for-a-manifest-base-provider.md).

### <a name="tracelogging"></a>TraceLogging

Tous les événements TraceLogging sont autodescriptifs. Les métadonnées d’événement nécessaires au décodage de l’événement sont automatiquement générées et transmises avec la charge utile dans un format binaire compact. Les décodeurs d’événements ont uniquement besoin de l’événement TraceLogging et d’une compréhension du format de métadonnées TraceLogging.

## <a name="configuring-tdh-for-decoding"></a>Configuration de TDH pour le décodage

Il y a de nombreux outils de décodage. Toutefois, il est recommandé d’utiliser TDH dans la mesure du possible, car il décode toutes les technologies de suivi avec une API unifiée. Selon le type de suivi que vous souhaitez décoder, TDH peut nécessiter une configuration explicite.

### <a name="mof"></a>MOF

TDH utilise les données de décodage MOF enregistrées sur le système à l’aide de mofcomp.exe. Pour plus d’informations, consultez [publication de votre schéma d’événement pour un fournisseur classique](publishing-your-event-schema-for-a-classic-provider.md).

### <a name="wpp"></a>WPP

TDH doit être pointé vers le fichier. pdb ou le associé. TMF du fournisseur WPP que vous essayez de décoder. Cela peut être effectué en appelant [**TdhSetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter). Dans le cas contraire, le moteur de décodage revient au chemin de recherche du format de TRACE de la variable \_ \_ d’environnement \_ .

### <a name="manifest-based"></a>Basé sur un manifeste

TDH utilise tous les fournisseurs basés sur un manifeste inscrits sur le système à l’aide de wevtutil.exe.

### <a name="tracelogging"></a>TraceLogging

Les versions les plus récentes de TDH détectent et décodent automatiquement les événements TraceLogging sans étapes supplémentaires.

 

 
