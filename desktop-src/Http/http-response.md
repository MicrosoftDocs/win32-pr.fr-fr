---
title: HTTP_RESPONSE (http. h)
description: 'La version de la \_ structure de réponse http dépend de la version de la file d’attente des demandes utilisée comme suit : API de serveur http version 1,0 de la file d’attente de demandes. il s’agit d’une \_ structure de requête HTTP \_ v1. API serveur HTTP version 2,0 file d’attente de demandes il s’agit d’une \_ structure de requête HTTP \_ v2.'
ms.assetid: F94646C0-7293-4543-842B-F08D8C7E2247
keywords:
- HTTP_RESPONSE
- HTTP_RESPONSE
- PHTTP_RESPONSE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a8445021aa61b94ae83a55937b1db5ca4e3c577
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384399"
---
# <a name="http_response"></a><span data-ttu-id="27de4-106">\_réponse http</span><span class="sxs-lookup"><span data-stu-id="27de4-106">HTTP\_RESPONSE</span></span>

<span data-ttu-id="27de4-107">La version de la structure de **\_ réponse http** dépend de la version de la file d’attente de demandes utilisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="27de4-107">The version of the **HTTP\_RESPONSE** structure is dependent on the version of the request queue used as follows:</span></span>

-   <span data-ttu-id="27de4-108">API de serveur HTTP version 1,0 file d’attente de requêtes : il s’agit d’une structure de [**\_ requête HTTP \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) .</span><span class="sxs-lookup"><span data-stu-id="27de4-108">HTTP Server API Version 1.0 request queue: This is an [**HTTP\_REQUEST\_V1**](/windows/desktop/api/Http/ns-http-http_request_v1) structure.</span></span>
-   <span data-ttu-id="27de4-109">API de serveur HTTP version 2,0 file d’attente de requêtes : il s’agit d’une structure de [**\_ requête HTTP \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) .</span><span class="sxs-lookup"><span data-stu-id="27de4-109">HTTP Server API Version 2.0 request queue: This is an [**HTTP\_REQUEST\_V2**](/windows/desktop/api/Http/ns-http-http_request_v2) structure.</span></span>

<span data-ttu-id="27de4-110">N’utilisez pas [**la \_ requête HTTP \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) et la [**\_ requête HTTP \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) directement dans votre code ; à la place, l’utilisation de la **\_ réponse http** garantit que la version appropriée de la structure est utilisée en fonction de la version de la file d’attente des demandes.</span><span class="sxs-lookup"><span data-stu-id="27de4-110">Do not use [**HTTP\_REQUEST\_V1**](/windows/desktop/api/Http/ns-http-http_request_v1) and [**HTTP\_REQUEST\_V2**](/windows/desktop/api/Http/ns-http-http_request_v2) directly in your code; using **HTTP\_RESPONSE** instead ensures the proper version of the structure is used based on the version of the request queue.</span></span>


```C++
typedef HTTP_REQUEST_V1 HTTP_RESPONSE;
typedef HTTP_REQUEST_V2 HTTP_RESPONSE;
typedef HTTP_RESPONSE* PHTTP_RESPONSE;
```



<dl> <dt>

<span data-ttu-id="27de4-111">**\_réponse http**</span><span class="sxs-lookup"><span data-stu-id="27de4-111">**HTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="27de4-112">La demande provient d’une file d’attente de demandes v1.</span><span class="sxs-lookup"><span data-stu-id="27de4-112">Request was from a v1 request queue.</span></span>

</dd> <dt>

<span data-ttu-id="27de4-113">**\_réponse http**</span><span class="sxs-lookup"><span data-stu-id="27de4-113">**HTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="27de4-114">La demande provient d’une file d’attente de demandes v2.</span><span class="sxs-lookup"><span data-stu-id="27de4-114">Request was from a v2 request queue.</span></span>

</dd> <dt>

<span data-ttu-id="27de4-115">**\_réponse PHTTP**</span><span class="sxs-lookup"><span data-stu-id="27de4-115">**PHTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="27de4-116">Pointeur vers une structure de **\_ réponse http** .</span><span class="sxs-lookup"><span data-stu-id="27de4-116">Pointer to an **HTTP\_RESPONSE** structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27de4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27de4-117">Requirements</span></span>



| <span data-ttu-id="27de4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27de4-118">Requirement</span></span> | <span data-ttu-id="27de4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="27de4-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="27de4-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27de4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="27de4-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27de4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="27de4-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27de4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="27de4-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27de4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="27de4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="27de4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="27de4-125"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="27de4-125"><dt>Http.h</dt></span></span> </dl> |



 

 





