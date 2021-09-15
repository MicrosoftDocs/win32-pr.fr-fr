---
title: Contrat
description: Un contrat de service transporte des métadonnées qui définissent la façon dont un service gère les messages de canal.
ms.assetid: 670530bf-344b-4480-8357-8984d80c0c68
keywords:
- Services Web contractuels pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7120346dac4d11c21955cd2430ed0a7dc277e88c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520964"
---
# <a name="contract"></a>Contrat

Un contrat de service transporte des métadonnées qui définissent la façon dont un service gère les messages de canal.


Un [**\_ \_ contrat de service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) transporte des métadonnées pour qu’un service gère un [ \_ message WS](ws-message.md).

![Diagramme montrant WS_SERVICE_CONTRACT métadonnées dans un message à un point de terminaison de service.](images/servicecontractintro.png)

Il possède une [**\_ \_ Description de contrat WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) et une table de fonctions. Une application peut éventuellement spécifier le [**\_ rappel de \_ \_ réception \_ d’un message WS service**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback).

Si une [**\_ \_ Description de contrat WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) et une table de fonctions ne sont pas spécifiées, l’application doit spécifier le [**\_ \_ \_ \_ rappel de réception de message WS service**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback).

![Diagramme montrant les opérations d’ajout et de soustraction du service dans le contrat de service ICalculator.](images/servicecontract.png)


``` syntax
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, 
    NULL, 
    &calculatorFunctions, 
};
```

Pour plus d’informations, consultez l’exemple [Calculator](httpcalculatorserviceexample.md) .

Description du contrat

[**WS \_ La \_ Description de contrat**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) est une métadonnée qui définit le contrat de type du service. Généré par [wsutil.exe](web-service-compiler-tool.md).

En termes de WSDL, une [**\_ \_ Description du contrat WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) est mappée à un wsdl : portType. Pour chaque wsdl : portType dans le document WSDL, une **\_ \_ Description de contrat WS** distincte est générée.

Une description de contrat est constituée d’une ou plusieurs [opérations de service](service-operation.md). Ces opérations sont fournies sous la forme d’un tableau de [**\_ \_ Description de l’opération WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).

![Diagramme montrant un WS_CONTRACT_DESCRIPTION sous la forme d’un tableau de WS_OPERATION_DESCRIPTIONs.](images/porttypetocontract.png)

``` syntax
<wsdl:definitions xmlns:soap="https://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="https://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="https://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="https://Example.org" 
xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="https://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="https://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="https://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="https://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="https://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="https://www.w3.org/2005/08/addressing" 
xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="https://Example.org" 
xmlns:wsdl="https://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="https://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="https://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

Pour plus d’informations sur WSDL : portType à la conversion de la [**\_ \_ Description de contrat WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) , consultez la [section sortie WSDL](wsdl-support.md).

Exemple : [ **\_ \_ Description de contrat WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)

``` syntax
static WS_CONTRACT_DESCRIPTION contractDescriptionICalculator =
{
    WsCountOf(serviceOperationsICalculator),
    serviceOperationsICalculator
};
```

Table de fonctions

La table de fonctions est un struct de pointeurs de fonction représentant chacune des [opérations de service](service-operation.md) dans le contrat de service. La définition de la table de fonctions est également générée par [wsutil.exe](web-service-compiler-tool.md).

Exemple : table de fonctions

``` syntax
 // Function Table
struct CalculatorServiceFunctionTable
{
      AddOperation Add;
      SubtractOperation Subtract;
};

// Populate the Function Table
static const CalculatorServiceFunctionTable calculatorFunctions = {Add, Subtract};
```

Utilisation du [ **\_ rappel de \_ \_ réception \_ d’un message WS service**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)

[**WS \_ Le \_ \_ \_ rappel de réception des messages de service**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) a un rôle double mutuellement exclusif.

Si une [**\_ \_ Description de contrat WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) est spécifiée sur [**le \_ \_ contrat de service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract), il devient le gestionnaire de messages par défaut pour toutes les actions qui ne sont pas prises en charge par la **\_ \_ Description de contrat WS** spécifiée. Sinon, si **WS \_ contrat \_ Description** n’est pas spécifié dans **le \_ \_ contrat de service WS** et que le [**\_ \_ \_ \_ rappel de réception du message WS service**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) est spécifié sur le **\_ \_ contrat de service** WS, tous les [messages](ws-message.md) sont passés à ce rappel.

Pour plus d’exemples, consultez

-   [Exemple de service non typé](untypedserviceexample.md)
-   [Exemple de service Calculator](httpcalculatorserviceexample.md)
-   [Opérations de service](service-operation.md)

Les rappels suivants font partie du contrat :

-   [**rappel de réception d’un \_ message WS service \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**\_rappel de \_ stub de service Web \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)

Les structures suivantes font partie du contrat :

-   [**\_Description du contrat WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)
-   [**\_contrat de service WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)

 

 




