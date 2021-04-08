---
description: La surveillance et le contrôle de l’état de l’agent ACD sur les stations est pris en charge par le biais de ces fonctions lineGetAgentCaps lineGetAgentStatus lineGetAgentGroupList lineGetAgentActivityList lineSetAgentGroup lineSetAgentState et lineSetAgentActivity.
ms.assetid: 2851fe54-f807-4cef-b6ca-2dcc7e1ae6fb
title: Surveillance et contrôle de l’agent ACD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52d3cf9387819bada069920099b19da65e6a1e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034939"
---
# <a name="acd-agent-monitoring-and-control"></a>Surveillance et contrôle de l’agent ACD

La surveillance et le contrôle de l’état de l’agent ACD sur les stations sont pris en charge via les fonctions suivantes : [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa), [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa), [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista), [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista), [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup), [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)et [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).

Le [**message \_ AGENTSTATUS de ligne**](line-agentstatus.md) est utilisé pour indiquer à quel moment les informations de l’agent ont été modifiées.

Ces contrôles sont associés à une adresse au lieu d’une ligne, car de nombreux systèmes ACD sont implémentés avec différentes files d’attente ACD associées à des boutons sur le terminal de téléphone (et des apparences d’appel distinctes). En outre, les téléphones de l’agent ACD peuvent souvent avoir des apparences d’appel distinctes pour les appels personnels.

De l’architecture, les fonctionnalités ACD doivent être implémentées dans une application serveur. Les fonctions client mentionnées ci-dessus, au lieu d’être mappées au fournisseur de services de téléphonie, sont transmises à une application serveur qui s’est inscrite (à l’aide de l’option [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)) comme gestionnaire de ces fonctions. Le message de [**ligne \_ PROXYREQUEST**](line-proxyrequest.md) est utilisé pour signaler à l’application de gestionnaire lorsqu’une demande a été effectuée ; elle appelle la fonction [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) pour retourner les résultats et les données. Les applications de gestionnaire peuvent également appeler [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) pour générer des messages de AGENTSTATUS de ligne quand cela est \_ nécessaire. Dans le cas d’un PBX hérité ou d’un ACD autonome qui implémente la fonctionnalité ACD lui-même, le fournisseur de services de téléphonie du commutateur doit inclure une application de serveur proxy qui accepte les requêtes et les achemine (éventuellement à l’aide de fonctions [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) ou d’une interface privée) au fournisseur de services, qui les achemine vers le commutateur.

 

 



