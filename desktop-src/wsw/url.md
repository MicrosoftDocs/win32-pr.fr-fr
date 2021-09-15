---
title: Url
description: Les éléments de l’API d’URL WWSAPI fournissent des mécanismes pour fractionner et annuler l’échappement des URL dans des composants, et pour échapper et combiner des composants de composant dans une URL.
ms.assetid: 2904fee0-d92b-4054-8ad9-51c409756f33
keywords:
- Services Web URL pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8511bf755f80f124071f658a65249243dc2f2af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294363"
---
# <a name="url"></a>Url

Les éléments de l’API d’URL WWSAPI fournissent des mécanismes pour fractionner et annuler l’échappement des URL dans des composants, et pour échapper et combiner des composants de composant dans une URL.

-   Pour fractionner et annuler l’échappement des URL dans des composants, utilisez la fonction [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) .
-   Pour échapper et combiner des composants de composant dans une URL, utilisez la fonction [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) .
-   Pour combiner des URL relatives avec une URL de base absolue formant une URL absolue, utilisez la fonction [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) .

Les énumérations suivantes font partie de l’URL :

-   [**\_indicateurs d’URL WS \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_writer_encoding_type)
-   [**\_type de \_ modèle d’URL WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_url_scheme_type)

Les fonctions suivantes font partie de l’URL :

-   [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl)
-   [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl)
-   [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl)

Les structures suivantes font partie de l’URL :

-   [**\_URL WS https \_**](/windows/desktop/api/WebServices/ns-webservices-ws_https_url)
-   [**\_URL http \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_url)
-   [**\_URL WS NETpipe \_**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [**\_URL WS NETTCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_nettcp_url)
-   [**\_URL WS SOAPUDP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_soapudp_url)
-   [**\_URL WS**](/windows/desktop/api/WebServices/ns-webservices-ws_url)

 

 




