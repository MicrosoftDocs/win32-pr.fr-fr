---
title: Url
description: Les éléments de l’API d’URL WWSAPI fournissent des mécanismes pour fractionner et annuler l’échappement des URL dans des composants, et pour échapper et combiner des composants de composant dans une URL.
ms.assetid: 2904fee0-d92b-4054-8ad9-51c409756f33
keywords:
- Services Web d’URL pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8511bf755f80f124071f658a65249243dc2f2af
ms.sourcegitcommit: 6f8c895f4d43c4463f6f33fa8014c5de413ece1f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/20/2020
ms.locfileid: "106510058"
---
# <a name="url"></a><span data-ttu-id="d1671-106">Url</span><span class="sxs-lookup"><span data-stu-id="d1671-106">Url</span></span>

<span data-ttu-id="d1671-107">Les éléments de l’API d’URL WWSAPI fournissent des mécanismes pour fractionner et annuler l’échappement des URL dans des composants, et pour échapper et combiner des composants de composant dans une URL.</span><span class="sxs-lookup"><span data-stu-id="d1671-107">The WWSAPI URL API elements provide mechanisms to split and unescape URLs into component parts, and to escape and combine component parts back into a URL.</span></span>

-   <span data-ttu-id="d1671-108">Pour fractionner et annuler l’échappement des URL dans des composants, utilisez la fonction [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) .</span><span class="sxs-lookup"><span data-stu-id="d1671-108">To split and unescape URLs into component parts, use the [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) function.</span></span>
-   <span data-ttu-id="d1671-109">Pour échapper et combiner des composants de composant dans une URL, utilisez la fonction [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) .</span><span class="sxs-lookup"><span data-stu-id="d1671-109">To escape and combine component parts back into a URL, use the [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) function.</span></span>
-   <span data-ttu-id="d1671-110">Pour combiner des URL relatives avec une URL de base absolue formant une URL absolue, utilisez la fonction [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) .</span><span class="sxs-lookup"><span data-stu-id="d1671-110">To combine relative URLs with an absolute base URL forming an absolute URL, use the [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) function.</span></span>

<span data-ttu-id="d1671-111">Les énumérations suivantes font partie de l’URL :</span><span class="sxs-lookup"><span data-stu-id="d1671-111">The following enumerations are part of the URL:</span></span>

-   [<span data-ttu-id="d1671-112">**\_indicateurs d’URL WS \_**</span><span class="sxs-lookup"><span data-stu-id="d1671-112">**WS\_URL\_FLAGS**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_writer_encoding_type)
-   [<span data-ttu-id="d1671-113">**\_type de \_ modèle d’URL WS \_**</span><span class="sxs-lookup"><span data-stu-id="d1671-113">**WS\_URL\_SCHEME\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_url_scheme_type)

<span data-ttu-id="d1671-114">Les fonctions suivantes font partie de l’URL :</span><span class="sxs-lookup"><span data-stu-id="d1671-114">The following functions are part of the URL:</span></span>

-   [<span data-ttu-id="d1671-115">**WsCombineUrl**</span><span class="sxs-lookup"><span data-stu-id="d1671-115">**WsCombineUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscombineurl)
-   [<span data-ttu-id="d1671-116">**WsDecodeUrl**</span><span class="sxs-lookup"><span data-stu-id="d1671-116">**WsDecodeUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl)
-   [<span data-ttu-id="d1671-117">**WsEncodeUrl**</span><span class="sxs-lookup"><span data-stu-id="d1671-117">**WsEncodeUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl)

<span data-ttu-id="d1671-118">Les structures suivantes font partie de l’URL :</span><span class="sxs-lookup"><span data-stu-id="d1671-118">The following structures are part of the URL:</span></span>

-   [<span data-ttu-id="d1671-119">**\_URL WS https \_**</span><span class="sxs-lookup"><span data-stu-id="d1671-119">**WS\_HTTPS\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_https_url)
-   [<span data-ttu-id="d1671-120">**\_URL http \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d1671-120">**WS\_HTTP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_url)
-   [<span data-ttu-id="d1671-121">**\_URL WS NETpipe \_**</span><span class="sxs-lookup"><span data-stu-id="d1671-121">**WS\_NETPIPE\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [<span data-ttu-id="d1671-122">**\_URL WS NETTCP \_**</span><span class="sxs-lookup"><span data-stu-id="d1671-122">**WS\_NETTCP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_nettcp_url)
-   [<span data-ttu-id="d1671-123">**\_URL WS SOAPUDP \_**</span><span class="sxs-lookup"><span data-stu-id="d1671-123">**WS\_SOAPUDP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_soapudp_url)
-   [<span data-ttu-id="d1671-124">**\_URL WS**</span><span class="sxs-lookup"><span data-stu-id="d1671-124">**WS\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_url)

 

 




