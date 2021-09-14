---
title: Opération de service
description: L’opération de service est le code et les métadonnées associés à une opération spécifique d’un service.
ms.assetid: 788940a0-b1d9-45d7-a4b5-6f0926026c7d
keywords:
- Services Web de l’opération de service pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e7883c0988189db3d977a78615c024dc92df36
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295146"
---
# <a name="service-operation"></a>Opération de service

L’opération de service est le code et les métadonnées associés à une opération spécifique d’un service.


En termes de WSDL, chaque wsdl : Operation définie dans le document WSDL pour un portType donné est une opération de service.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="http://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

Chaque opération de service au sein du modèle de service est fournie sous la forme d’une [**\_ \_ Description d’opération WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description). La \_ \_ Description de l’opération WS est générée par [wsutil.exe](web-service-compiler-tool.md).

Pour chaque wsdl : opération, l’outil génère une [**\_ \_ Description d’opération WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)distincte.

![Diagramme montrant comment wsutil.exe génère une WS_CONTRACT_DESCRIPTION.](images/porttypetocontract.png)

``` syntax
static WS_OPERATION_DESCRIPTION serviceOperationsICalculator[] =
{
    {
        // Add Method
        &messageDescriptionAddICalculator,
        &messageDescriptionAddResponseICalculator,
        WsCountOf(parametersAddICalculator),
        ICalculator_Add_Stub 
    }
};
```

En termes de code, chaque opération de service est associée à une fonction. La définition de cette fonction est différente pour le client et les serveurs.

Les opérations de service sont classées dans,

-   [Opérations de service côté client](client-side-service-operations.md)
-   [Opérations de service côté serveur](server-side-service-operations.md)

Cette classification est principalement basée sur la disposition des signatures du serveur et les implémentations côté client des opérations de service.

Voir aussi la [section prise en charge de WSDL](wsdl-support.md).

Les énumérations suivantes sont utilisées avec les opérations de service :

-   [**\_type de paramètre WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_parameter_type)
-   [**raison de l' \_ annulation du service WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_cancel_reason)
-   [**OPTION de message de l' \_ opération WS service \_ \_ \_**](/windows/win32/api/webservices/ne-webservices-ws_charset)

Les structures suivantes sont utilisées avec les opérations de service :

-   [**\_Description du message WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)
-   [**Description de l' \_ opération WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)
-   [**\_Description du paramètre WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description)

 

 




