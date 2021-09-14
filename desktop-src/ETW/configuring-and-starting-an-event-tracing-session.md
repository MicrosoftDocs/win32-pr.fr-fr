---
description: Pour configurer une session de suivi d’événements, utilisez \_ la \_ structure des propriétés de la trace d’événements pour spécifier les propriétés de la session.
ms.assetid: 8a6aa39c-ec81-42ac-a26e-29f1f6960220
title: Configuration et démarrage d’une session de suivi d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f86ec57975e8f12ede17e5e2cda962c010aa1af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007446"
---
# <a name="configuring-and-starting-an-event-tracing-session"></a>Configuration et démarrage d’une session de suivi d’événements

Pour configurer une session de suivi d’événements, utilisez la structure des [**\_ \_ Propriétés**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) de la trace d’événements pour spécifier les propriétés de la session. La mémoire que vous allouez pour la structure des **\_ \_ Propriétés de trace d’événements** doit être suffisamment grande pour contenir également les noms de session et de fichier journal qui suivent la structure en mémoire.

Une fois que vous avez spécifié les propriétés de la session, appelez la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) pour démarrer la session. Si la fonction est réussie, le paramètre *SessionHandle* contient le handle de session et la propriété **LoggerNameOffset** contient l’offset du nom de la session.

Pour activer les fournisseurs qui doivent enregistrer des événements dans votre session, appelez la fonction [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) pour activer les fournisseurs classiques et la fonction [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) pour activer les fournisseurs [basés sur un manifeste](about-event-tracing.md) . pour permettre aux fournisseurs de journaliser des événements de journal sur des conditions spécifiques sur Windows 8.1, Windows Server 2012 R2 et versions ultérieures, appelez la fonction [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) .

En outre, vous pouvez également suivre des informations supplémentaires sur un événement à l’aide d’un appel à la fonction [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) . **TraceSetInformation** place des informations de traçage supplémentaires dans la section des données étendues d’un événement et peut inclure des informations telles que les informations de version de la trace ou les fournisseurs actuellement inscrits sur le système. Pour plus d’informations, consultez [récupération de données de suivi d’événements supplémentaires](retrieving-additional-event-tracing-data.md).

Jusqu’à huit sessions de suivi peuvent activer et recevoir des événements du même fournisseur [basé sur un manifeste](about-event-tracing.md) . Toutefois, une seule session de suivi peut activer un fournisseur [classique](about-event-tracing.md) . Si plusieurs sessions de suivi essaient d’activer un fournisseur classique, la première session cesse de recevoir des événements lorsque la deuxième session active le fournisseur. Par exemple, si la session A activé le fournisseur 1, puis le fournisseur 1 de la session B, seule la session B recevrait les événements du fournisseur 1.

Vous pouvez utiliser l’une des trois fonctions pour activer un fournisseur, mais vous risquez de perdre des fonctionnalités si vous utilisez [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) pour activer un fournisseur basé sur un manifeste, car vous ne pouvez pas fournir une valeur MatchAllKeyword, spécifier des éléments de données étendus à inclure dans l’événement ou fournir des données de filtre définies par le fournisseur. Pour plus d’informations, consultez la section Notes de chaque fonction.

sur Windows 8.1, Windows Server 2012 R2 et versions ultérieures, la charge utile d’événement, la portée et les filtres de parcours de pile peuvent être utilisés par la fonction [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) et les structures [**activer les \_ \_ paramètres de TRACE**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) et [**\_ \_ descripteurs de filtre d’événement**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) pour filtrer sur des conditions spécifiques dans une session de journalisation. Pour plus d’informations sur les filtres de charge utile d’événement, consultez les fonctions [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)et [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) , ainsi que les structures de prédicat **activer les \_ \_ paramètres de trace**, **\_ \_ descripteur de filtre d’événement** et de [**\_ filtre \_ de charge utile**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) .

Pour déterminer le niveau et les mots clés utilisés pour activer un fournisseur basé sur un manifeste, utilisez l’une des commandes suivantes :

-   **Logman** **query** *Provider-nom*
-    *Fournisseur de stratégie de nom* **wevtutil**

Les commandes répertorient uniquement le niveau et les mots clés, le fournisseur doit documenter les exigences de données de filtre pour les contrôleurs potentiels.

Pour énumérer les fournisseurs basés sur un manifeste, utilisez **wevtutil** **EP**.

Pour les fournisseurs classiques, il revient au fournisseur de documenter et de mettre à la disposition des contrôleurs potentiels les niveaux de gravité ou d’activer les indicateurs qu’il prend en charge. Si le fournisseur souhaite être activé par n’importe quel contrôleur, le fournisseur doit accepter 0 comme niveau de gravité et activer les indicateurs et interpréter 0 comme une requête d’exécution de la journalisation par défaut (tout ce qui peut être).

Vous pouvez activer le fournisseur avant ou après que le fournisseur s’est inscrit lui-même. Une fois le fournisseur activé, ETW appelle la fonction de rappel du fournisseur. Si le fournisseur n’est pas inscrit, ETW appellera la fonction de rappel du fournisseur une fois qu’il s’est inscrit lui-même.

Vous pouvez également utiliser la fonction [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) pour désactiver le fournisseur (l’arrêter à partir de l’enregistrement des événements dans votre session) ou pour mettre à jour le niveau de journalisation ou activer les indicateurs du fournisseur. Avec la fonction [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) , vous pouvez désactiver le fournisseur ou mettre à jour le niveau, les mots clés, les données étendues et les données de filtre. Chaque fois que vous appelez la fonction **EnableTrace** ou **EnableTraceEx** , ETW appelle la fonction de rappel du fournisseur. Le fournisseur reste activé pour la session jusqu’à ce que la session désactive le fournisseur.

Pour arrêter la session de suivi après avoir collecté des événements, appelez la fonction [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) et transmettez l' \_ arrêt du contrôle de trace d’événements \_ \_ en tant que code de contrôle. Pour spécifier la session à arrêter, vous pouvez passer le descripteur de session de suivi d’événements obtenu à partir d’un appel antérieur à la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) , ou le nom d’une session démarrée précédemment. Veillez à désactiver tous les fournisseurs avant d’arrêter la session. Si vous arrêtez la session avant de désactiver le fournisseur pour la première fois, ETW désactive le fournisseur et tente d’appeler la fonction de rappel de contrôle du fournisseur. Si l’application qui a démarré la session se termine sans désactiver le fournisseur ou en appelant la fonction **ControlTrace** , le fournisseur reste activé.

Si [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) réussit, les propriétés de session sont mises à jour pour refléter les valeurs de propriété finales et exécuter des statistiques pour la session de suivi d’événements.

Pour obtenir un exemple de démarrage d’une session de suivi d’événements, consultez les rubriques suivantes :

-   [Exemple qui crée une session et active un fournisseur basé sur un manifeste](example-that-creates-a-session-and-enables-a-manifest-based-provider.md) -démarre une session de suivi, active un fournisseur basé sur un manifeste, désactive le fournisseur, puis arrête la session.

Pour plus d’informations sur le démarrage d’une session de suivi, consultez l’une des rubriques suivantes :

-   [Configuration et démarrage d’une session SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
-   [Configuration et démarrage de la session de journalisation du noyau NT](configuring-and-starting-the-nt-kernel-logger-session.md)
-   [Configuration et démarrage d’une session de journalisation automatique](configuring-and-starting-an-autologger-session.md)
-   [Configuration et démarrage de la session de journalisation globale](configuring-and-starting-the-global-logger-session.md)
-   [Configuration et démarrage d’une session de journalisation privée](configuring-and-starting-a-private-logger-session.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration et démarrage d’une session de journalisation privée](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configuration et démarrage d’une session SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configuration et démarrage d’une session de journalisation automatique](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configuration et démarrage de la session de journalisation du noyau NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea)
</dt> <dt>

[**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace)
</dt> <dt>

[**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**ACTIVER \_ les \_ paramètres de trace**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**descripteur de filtre d’événements \_ \_**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**Propriétés de la trace d’événements \_ \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**\_prédicat de filtre de charge utile \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Mise à jour d’une session de suivi d’événements](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
