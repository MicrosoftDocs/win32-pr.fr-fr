---
description: SystemTraceProvider est un fournisseur de noyaux avec un ensemble prédéfini d’événements de noyau pris en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Configuration et démarrage d’une session SystemTraceProvider
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 66e9d672a7c8e6358c2a92e7661e0d4e2a5878ab
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386739"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a>Configuration et démarrage d’une session SystemTraceProvider

SystemTraceProvider est un fournisseur de noyaux avec un ensemble prédéfini d’événements de noyau pris en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures. Sur Windows 7 et Windows Server 2008 R2, SystemTraceProvider ne peut être utilisé que pour la session de journalisation du noyau NT.

Sur Windows 8, Windows Server 2012 et versions ultérieures, les SystemTraceProvider peuvent être multiplexés pour jusqu’à 8 sessions d’enregistreur d’événements. Les deux premiers emplacements pour les sessions de journalisation sont réservés pour l’enregistreur d’événements de noyau NT et le journal de contexte de noyau circulaire.

Pour plus d’informations sur l’utilisation de la session de journalisation du noyau NT en tant que fournisseur de trace, consultez [configuration et démarrage de la session de journalisation du noyau NT](configuring-and-starting-the-nt-kernel-logger-session.md).

Dans le kit de développement logiciel (SDK) Windows 10 version 20348 et versions ultérieures, les SystemTraceProvider peuvent être configurés via des fournisseurs système distincts, qui peuvent être contrôlés avec [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) comme des fournisseurs d’événements suivi d’v nements pour Windows standard. Pour obtenir la liste complète des fournisseurs système, des mots clés et des groupes et indicateurs hérités correspondants, consultez [fournisseurs système](system-providers.md) .

## <a name="enable-a-systemtraceprovider-session"></a>Activer une session SystemTraceProvider

Pour permettre à SystemTraceProvider de démarrer une session autre que l’enregistreur d’événements de noyau NT, exécutez la commande suivante :

**tracelog-Start MySession-f c : \\ Kernel1. etl-EFLAG Proc \_ thread + Loader + CSWITCH**

Pour activer par programmation le SystemTraceProvider pour démarrer une session autre que l’enregistreur d’événements de noyau NT, procédez comme suit.

-   Définissez un nom de journal privé.

    **\#définir le nom d’enregistreur d’événements privé \_ \_ L "session de trace privée"**

-   Au niveau du contrôleur, définissez les membres suivants de la structure des [**\_ \_ Propriétés**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) de la trace d’événements.

    Définissez **LogFileMode** sur **Event \_ trace \_ système \_ logger \_ mode**.

    Définissez **LoggerName** sur Logger privé, au lieu **de \_ \_ nom d’enregistreur de noyau**.

    Assurez-vous que le membre **Wnode. Guid** de la structure des [**\_ \_ Propriétés de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) n’a pas la valeur **SystemTraceControlGuid**. Vous devez assigner un nouveau **GUID** à ce membre.

-   Au niveau du consommateur, définissez le membre **LoggerName** de la structure du [**\_ \_ fichier journal de suivi d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) sur cet enregistreur d’événements privé.

> [!Note]  
> Si vous souhaitez qu’un non-administrateur ou un processus non-TCB puisse démarrer une session de suivi de profilage à l’aide de SystemTraceProvider pour le compte d’applications tierces, vous devez accorder le privilège de profil utilisateur, puis ajouter cet utilisateur au **GUID** de session (créé pour la session de journalisation) et au **GUID** du fournisseur de trace système pour activer le fournisseur de trace système. Pour plus d’informations, consultez la fonction [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) .

 

## <a name="related-topics"></a>Rubriques connexes

[Configuration et démarrage d’une session de journalisation privée](configuring-and-starting-a-private-logger-session.md)

[Configuration et démarrage d’une session de journalisation automatique](configuring-and-starting-an-autologger-session.md)

[Configuration et démarrage d’une session de suivi d’événements](configuring-and-starting-an-event-tracing-session.md)

[Configuration et démarrage de la session de journalisation du noyau NT](configuring-and-starting-the-nt-kernel-logger-session.md)

[Fournisseurs système](system-providers.md)

[Mise à jour d’une session de suivi d’événements](updating-an-event-tracing-session.md)

 

 
