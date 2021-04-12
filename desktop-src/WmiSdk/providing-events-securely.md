---
description: Vous pouvez empêcher des utilisateurs non autorisés de recevoir des événements auxquels ils ne devraient pas avoir accès.
ms.assetid: 59788643-f57d-458f-91ab-26552218523b
ms.tgt_platform: multiple
title: Fournir des événements en toute sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2c92ed1de08dde4891365440f559544a0b26de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209648"
---
# <a name="providing-events-securely"></a>Fournir des événements en toute sécurité

Vous pouvez empêcher des utilisateurs non autorisés de recevoir des événements auxquels ils ne devraient pas avoir accès. Votre fournisseur d’événements peut fournir des instances de ses propres classes d’événements, tout comme le [fournisseur de Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider) fournit des classes telles que [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). Votre fournisseur d’événements peut également fournir des événements intrinsèques tels que [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md). Pour plus d’informations, consultez [écriture d’un fournisseur d’événements](writing-an-event-provider.md).

Un fournisseur d’événements peut contrôler l’accès aux destinataires des événements des manières suivantes :

-   L’utilisation du contrôle d’accès en implémentant [**IWbemEventProviderSecurity :: AccessCheck**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) est le moyen le plus efficace.

    Le fournisseur détermine si le consommateur dispose des privilèges nécessaires pour recevoir un événement demandé. Si le consommateur ne dispose pas des privilèges suffisants pour s’inscrire, WMI renvoie une erreur d’accès refusé. Utilisez ce mode lorsque le fournisseur peut décider qui peut recevoir des événements. Par exemple, un fournisseur peut fournir des événements liés à la sécurité et peut exiger que le consommateur dispose de privilèges d’administrateur avec le privilège **SeSecurityPrivilege** activé.

-   L’implémentation de [**IWbemEventSink :: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) sur le récepteur utilisé pour déclencher des événements permet de définir un descripteur de sécurité (SD) sur un récepteur pour tous les événements passés.

    WMI effectue des vérifications d’accès basées sur le SD. Utilisez ce mode lorsque le fournisseur ne peut pas prendre la décision concernant les personnes autorisées à utiliser ses événements, mais peut choisir un SD pour un récepteur spécifique. Par exemple, utilisez [**IWbemEventSink :: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) si votre fournisseur d’événements a obtenu plusieurs récepteurs par des appels à [**IWbemEventSink :: GetRestrictedSink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink) et que vous souhaitez un descripteur de sécurité pour chaque récepteur.

-   La définition de la propriété **\_ descripteur de sécurité** d’un événement permet de définir un SD pour chaque événement.

    Utilisez cette approche lorsque chaque événement remis au récepteur peut avoir des descripteurs de sécurité différents. Pour utiliser cette approche, dérivez les classes d’événements extrinsèques définies par votre fournisseur de [**\_ \_ Event**](--event.md) ou [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) afin que votre classe contienne la propriété **\_ descripteur de sécurité** . Par exemple, votre fournisseur d’événements peut publier des événements sécurisés et normaux via un récepteur. Dans ce cas, utilisez le descripteur de sécurité de compte administrateurs pour les événements sécurisés et un descripteur de sécurité **null** pour les événements normaux qui peuvent être reçus par n’importe qui.

## <a name="securing-events-by-decoupled-event-providers"></a>Sécurisation des événements par des fournisseurs d’événements découplé

Les fournisseurs d’événements découplés diffèrent des fournisseurs d’événements nondecoupled de la façon dont ils s’inscrivent auprès de WMI. L’appel à [**IWbemEventProviderSecurity :: AccessCheck**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovidersecurity-accesscheck) pour les événements d’un fournisseur découplé ne propage jamais le jeton d’accès client. WMI gère le contrôle d’accès de la même manière que pour les fournisseurs d’événements nondecoupled. Pour plus d’informations sur l’écriture d’un fournisseur découplé, consultez [incorporation d’un fournisseur dans une application](incorporating-a-provider-in-an-application.md).

Seuls les administrateurs disposant du privilège d' **\_ écriture complet** défini dans le **contrôle WMI** du **panneau de configuration** sont autorisés à déclencher des événements pour un espace de noms. Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms avec le contrôle WMI](setting-namespace-security-with-the-wmi-control.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurisation des événements WMI](securing-wmi-events.md)
</dt> </dl>

 

 
