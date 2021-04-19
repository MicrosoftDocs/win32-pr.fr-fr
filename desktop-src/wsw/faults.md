---
title: Pannes
description: Un message d’erreur est utilisé pour communiquer les informations d’erreur relatives à un échec au niveau d’un point de terminaison distant.
ms.assetid: d2bada50-2ddd-4f7f-9b25-7bbec77b431b
keywords:
- Services Web des erreurs pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2ecad1b63335b7f2bfc81c099b4f920d9de21c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106508966"
---
# <a name="faults"></a>Pannes

Un message d’erreur est utilisé pour communiquer les informations d’erreur relatives à un échec au niveau d’un point de terminaison distant. Un message d’erreur est semblable à tout autre message, sauf que le format du corps du message a un format standard. Les erreurs peuvent être utilisées à la fois par les protocoles d’infrastructure, tels que WS-Addressing et par les protocoles d’application de niveau supérieur.

-   [Vue d’ensemble](#overview)
-   [Génération d’erreurs dans un service](#generating-faults-in-a-service)
-   [Gestion des erreurs sur un client](#handling-faults-on-a-client)
-   [Utilisation d’erreurs avec des messages](#using-faults-with-messages)

## <a name="overview"></a>Vue d’ensemble

Le contenu du corps d’un message d’erreur est représenté dans cette API à l’aide de la structure d' [**\_ erreur WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) . Bien qu’une erreur ait un ensemble fixe de champs utilisés pour fournir des informations sur l’échec (par exemple, le [**\_ \_ code d’erreur WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code) qui identifie le type d’erreur et la raison de l' [**\_ erreur \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason) qui contient le texte décrivant l’erreur), elle contient également un champ de détail qui peut être utilisé pour spécifier le contenu XML arbitraire relatif à l’erreur.

## <a name="generating-faults-in-a-service"></a>Génération d’erreurs dans un service

En général, un service envoie une erreur en raison d’une erreur rencontrée lors du traitement de la demande. Le modèle utilisé par cette API est que le code du service qui rencontre l’erreur de traitement capture les informations d’erreur nécessaires dans l’objet [WS \_ Error](ws-error.md) , puis le code à un niveau supérieur dans la chaîne d’appel envoie en fait l’erreur à l’aide des informations capturées au niveau de la couche inférieure. Ce schéma permet au code qui envoie l’erreur d’être isolé de la façon dont les situations d’erreur sont mappées à des erreurs, tout en autorisant l’envoi d’informations d’erreur enrichies.

Les propriétés suivantes peuvent être utilisées avec [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) pour capturer les informations d’erreur d’un objet [WS \_ Error](ws-error.md) :

-   [**WS \_ \_action de \_ propriété \_ erreur d’erreur**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Spécifie l’action à utiliser pour le message d’erreur. Si ce paramètre n’est pas spécifié, une action par défaut est fournie.
-   [**WS \_ \_erreur de \_ propriété \_ d’erreur d’erreur**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Contient la structure de l' [**\_ erreur WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) qui est envoyée dans le corps du message d’erreur.
-   [**WS \_ \_ \_ \_ en-tête de propriété d’erreur d’erreur**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Certaines erreurs incluent des en-têtes de message qui sont ajoutés au message d’erreur pour acheminer les échecs de traitement relatifs aux en-têtes du message de demande. Cette propriété peut être utilisée pour spécifier une [ \_ \_ mémoire tampon XML WS](ws-xml-buffer.md) contenant un en-tête à ajouter au message d’erreur.

Toutes les chaînes d’erreur ajoutées à l’objet [WS \_ Error](ws-error.md) sont utilisées comme texte dans l’erreur envoyée. Des chaînes d’erreur peuvent être ajoutées à l’objet d’erreur à l’aide de [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring).

La fonction [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) peut être utilisée pour définir les propriétés de l’objet [WS \_ Error](ws-error.md) .

Pour définir les détails de l’erreur stockée dans l’objet [WS \_ Error](ws-error.md) , utilisez la fonction [**WsSetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail) . Cette fonction peut être utilisée pour associer du contenu XML arbitraire à l’erreur.

L' [hôte de service](service-host.md) enverra automatiquement des erreurs en utilisant les informations ci-dessus dans l’objet [WS \_ Error](ws-error.md) . La propriété de [**Divulgation d’erreur de \_ propriété de service \_ \_ \_ Web**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) peut être utilisée pour contrôler la façon dont l’erreur est envoyée.

Si vous travaillez au niveau de la couche de canal, des erreurs peuvent être envoyées pour un objet [WS \_ Error](ws-error.md) à l’aide de [**WsSendFaultMessageForError**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror).

## <a name="handling-faults-on-a-client"></a>Gestion des erreurs sur un client

Si un client reçoit une erreur lors de l’utilisation d’un [proxy de service](service-proxy.md) ou via [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) ou [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage), l’erreur de **point de terminaison WS \_ E \_ \_ \_ received** est retournée. (Pour plus d’informations, consultez [valeurs de retour des services Web Windows](windows-web-services-return-values.md).) Ces fonctions remplissent également l’objet [WS \_ Error](ws-error.md) fourni à l’appel avec des informations sur l’erreur reçue.

Les propriétés suivantes d’un objet [WS \_ Error](ws-error.md) peuvent être interrogées à l’aide de [**WsGetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty) pour obtenir des informations sur une erreur qui a été reçue :

-   [**WS \_ \_action de \_ propriété \_ erreur d’erreur**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Spécifie la valeur de l’action du message d’erreur.
-   [**WS \_ \_erreur de \_ propriété \_ d’erreur d’erreur**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Contient la structure [**d' \_ erreur WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) qui a été désérialisée à partir du corps du message d’erreur.

Une erreur peut contenir du contenu XML supplémentaire arbitraire dans le détail de l’erreur. Vous pouvez y accéder à l’aide de la fonction [**WsGetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail) .

## <a name="using-faults-with-messages"></a>Utilisation d’erreurs avec des messages

La section suivante s’applique lors de la gestion directe du contenu du corps d’un message d’erreur.

Le contenu du corps d’un message d’erreur est représenté par la structure de l' [**\_ erreur WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) standard, qui dispose d’une prise en charge intégrée pour la sérialisation.

Par exemple, le code suivant peut être utilisé pour écrire une erreur dans le corps d’un message :

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault = { ... };
hr = WsWriteBody(message, &faultDescription, WS_WRITE_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

Le code suivant peut être utilisé pour lire une erreur à partir d’un corps de message :

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault;
hr = WsReadBody(message, &faultDescription, WS_READ_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

Pour savoir si un message reçu est une erreur ou non, la propriété du [**\_ message WS \_ est \_ l' \_ erreur**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) peut être consultée. Cette propriété est définie selon que le premier élément du corps est un élément Fault pendant [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) ou [**WsReadEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart).

Pour créer une erreur [**WS \_ en raison**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) d’une [ \_ erreur WS](ws-error.md), utilisez la fonction [**WsCreateFaultFromError**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror) .

Les énumérations suivantes font partie des erreurs :

-   [**\_Divulgation d’erreurs WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure)
-   [**\_ID de \_ propriété d’erreur WS Fault \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)

Les fonctions suivantes font partie des erreurs :

-   [**WsCreateFaultFromError**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror)
-   [**WsGetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail)
-   [**WsGetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty)
-   [**WsSetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail)
-   [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty)

Les structures suivantes font partie des erreurs :

-   [**\_erreur WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)
-   [**\_code d’erreur WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)
-   [**\_ \_ Description détaillée de l’erreur WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_detail_description)
-   [**raison de l' \_ erreur WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)

 

 




