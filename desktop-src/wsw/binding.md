---
title: liaison de canal
description: Les liaisons spécifient le protocole câble et le comportement local pour un canal.
ms.assetid: 82d465c5-b23d-4403-b360-8c710fbc6e1c
keywords:
- Liaison de services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723a729b87dc26849dbd1f84038805c5e47a0ea4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310289"
---
# <a name="channel-binding"></a><span data-ttu-id="a192c-106">liaison de canal</span><span class="sxs-lookup"><span data-stu-id="a192c-106">Channel Binding</span></span>

<span data-ttu-id="a192c-107">Les liaisons spécifient le protocole câble et le comportement local pour un canal.</span><span class="sxs-lookup"><span data-stu-id="a192c-107">Bindings specify the wire protocol and local behavior for a channel.</span></span> <span data-ttu-id="a192c-108">Les liaisons sont composées des composants suivants :</span><span class="sxs-lookup"><span data-stu-id="a192c-108">Bindings are made up of the following components:</span></span>

-   <span data-ttu-id="a192c-109">Une [**\_ \_ liaison WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), qui identifie le protocole de transfert à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a192c-109">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), which identifies the transfer protocol to use.</span></span>
-   <span data-ttu-id="a192c-110">Une [**\_ \_ Description de la sécurité WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), qui spécifie comment sécuriser le canal.</span><span class="sxs-lookup"><span data-stu-id="a192c-110">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), which specifies how to secure the channel.</span></span>
-   <span data-ttu-id="a192c-111">Un ensemble [**de \_ \_ Propriétés WS Channel**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property), qui spécifient des paramètres facultatifs supplémentaires (voir aussi [**\_ \_ \_ ID de propriété de canal WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)).</span><span class="sxs-lookup"><span data-stu-id="a192c-111">A set [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, which specify additional optional settings (see also [**WS\_CHANNEL\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)).</span></span>

 

 




