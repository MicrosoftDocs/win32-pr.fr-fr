---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 40d26ea1-3081-4afd-8b12-bc6521fad390
ms.tgt_platform: multiple
title: E (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbd1ce4685ee9901dfedca2a4b3a1b948d91c8f5b56def28494eb6c4c63e726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319218"
---
# <a name="e-wmi"></a>E (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) e [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**Event, classe**
</dt> <dd>

Classe WMI à laquelle les *consommateurs d’événements* peuvent s’abonner par une requête d' *événement*. La classe signale un type spécifique d’occurrence. Par exemple, la [**classe \_ ProcessStopTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) signale qu’un processus spécifique s’est arrêté.

</dd> <dt>

<span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**consommateur d’événements**
</dt> <dd>

Destinataire des notifications qui font état de l'occurrence d'un événement. Un consommateur d’événements est [*temporaire*](gloss-t.md) ou [*permanent*](gloss-p.md).

</dd> <dt>

<span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**fournisseur de consommateur d’événements**
</dt> <dd>

Fournisseur qui détermine quel consommateur d'événements permanent gère un événement donné. Un fournisseur de consommateur d’événements est inscrit auprès de WMI par une instance de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md), qui contient une liste des classes de [*consommateur logiques*](gloss-l.md) prises en charge par le fournisseur de consommateur d’événements. Un fournisseur de consommateur d’événements est un serveur COM qui mappe des [*consommateurs physiques*](gloss-p.md) à des *consommateurs logiques*. Un fournisseur de consommateur d’événements prend en charge l’interface [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) et est un composant de l’architecture du consommateur permanent.

</dd> <dt>

<span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**filtre d’événement**
</dt> <dd>

Instance de la classe système [**\_ \_ EventFilter**](--eventfilter.md) qui décrit un type d’événement et les conditions pour la transmission d’une notification. Un consommateur utilise un filtre d’événement pour s’inscrire afin de recevoir une notification d’un type spécifique d’événement.

</dd> <dt>

<span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**fournisseur d’événements**
</dt> <dd>

Fournisseur WMI qui surveille une source d’événements et notifie WMI lorsque des événements se produisent. Un fournisseur d’événements implémente les interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) et [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) , et parfois [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).

</dd> <dt>

<span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**requête d’événement**
</dt> <dd>

Instruction [*langage de requêtes WMI (WQL)*](gloss-w.md) que les consommateurs d’événements utilisent pour s’inscrire afin de recevoir des notifications d’événements spécifiques. Un fournisseur d'événements utilise une requête d'événement pour s'inscrire afin de générer des notifications d'événements spécifiques.

</dd> <dt>

<span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**schéma d’extension**
</dt> <dd>

troisième couche du [*schéma cim*](gloss-c.md), qui comprend des extensions spécifiques à la plateforme du schéma cim, telles que Windows, UNIX et Exchange Server. Voir aussi modèle [*commun*](gloss-c.md) et modèle principal.

</dd> <dt>

<span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**événement extrinsèque**
</dt> <dd>

Notification d’événement d’un fournisseur. La plupart des fournisseurs créent une instance d’une classe d’événements définie dans les fichiers MOF du fournisseur. Un événement extrinsèque hérite de [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md). Par exemple, le [fournisseur du journal des événements](/previous-versions/windows/desktop/eventlogprov/event-log-provider) définit la classe d’événements [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). Consultez également [*événement intrinsèque*](gloss-i.md).

</dd> </dl>

 

 
