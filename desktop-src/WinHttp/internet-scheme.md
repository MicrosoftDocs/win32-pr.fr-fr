---
description: Schémas Internet pris en charge par WinHTTP.
ms.assetid: 31e45879-807e-4dd5-9f99-94a46011e55e
title: INTERNET_SCHEME (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7b73dcc13b2623e3a6f28d2d49d1965464070f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867793"
---
# <a name="internet_scheme"></a><span data-ttu-id="6093f-103">\_schéma Internet</span><span class="sxs-lookup"><span data-stu-id="6093f-103">INTERNET\_SCHEME</span></span>

<span data-ttu-id="6093f-104">Schémas Internet pris en charge par WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="6093f-104">Internet schemes supported by WinHTTP.</span></span>

<dl> <dt>

<span data-ttu-id="6093f-105"><span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**\_schéma Internet \_ http**</span><span class="sxs-lookup"><span data-stu-id="6093f-105"><span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**INTERNET\_SCHEME\_HTTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6093f-106">1</span><span class="sxs-lookup"><span data-stu-id="6093f-106">1</span></span>
</dt> <dt>



<span data-ttu-id="6093f-107">Schéma Internet HTTP.</span><span class="sxs-lookup"><span data-stu-id="6093f-107">An HTTP internet scheme.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6093f-108"><span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**\_https du schéma Internet \_**</span><span class="sxs-lookup"><span data-stu-id="6093f-108"><span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**INTERNET\_SCHEME\_HTTPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6093f-109">2</span><span class="sxs-lookup"><span data-stu-id="6093f-109">2</span></span>
</dt> <dt>



<span data-ttu-id="6093f-110">Schéma Internet HTTPs (SSL).</span><span class="sxs-lookup"><span data-stu-id="6093f-110">An HTTPS (SSL) internet scheme.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6093f-111"><span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**\_FTP de schéma Internet \_**</span><span class="sxs-lookup"><span data-stu-id="6093f-111"><span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**INTERNET\_SCHEME\_FTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6093f-112">3</span><span class="sxs-lookup"><span data-stu-id="6093f-112">3</span></span>
</dt> <dt>



<span data-ttu-id="6093f-113">Schéma Internet FTP.</span><span class="sxs-lookup"><span data-stu-id="6093f-113">An FTP internet scheme.</span></span> <span data-ttu-id="6093f-114">Ce schéma est pris en charge uniquement pour une utilisation dans [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) et [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="6093f-114">This scheme is only supported for use in [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) and [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6093f-115"><span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**\_Socks de schéma Internet \_**</span><span class="sxs-lookup"><span data-stu-id="6093f-115"><span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**INTERNET\_SCHEME\_SOCKS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6093f-116">4</span><span class="sxs-lookup"><span data-stu-id="6093f-116">4</span></span>
</dt> <dt>



<span data-ttu-id="6093f-117">Un schéma d’Internet SOCKS.</span><span class="sxs-lookup"><span data-stu-id="6093f-117">A SOCKS internet scheme.</span></span> <span data-ttu-id="6093f-118">Ce schéma est pris en charge uniquement pour une utilisation dans l' [**\_ entrée de \_ résultat \_ de proxy WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry).</span><span class="sxs-lookup"><span data-stu-id="6093f-118">This scheme is only supported for use in [**WINHTTP\_PROXY\_RESULT\_ENTRY**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6093f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6093f-119">Requirements</span></span>



| <span data-ttu-id="6093f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6093f-120">Requirement</span></span> | <span data-ttu-id="6093f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="6093f-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6093f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6093f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6093f-123">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6093f-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="6093f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6093f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6093f-125">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6093f-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>   |
| <span data-ttu-id="6093f-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="6093f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6093f-127"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="6093f-127"><dt>Winhttp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6093f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6093f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6093f-129">**\_entrée des \_ résultats du proxy WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="6093f-129">**WINHTTP\_PROXY\_RESULT\_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> </dl>

 

 




