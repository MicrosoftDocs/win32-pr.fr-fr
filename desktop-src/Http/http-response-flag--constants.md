---
title: Constantes HTTP_RESPONSE_FLAG_ (http. h)
description: Définissez les options de configuration des réponses dans l’API du serveur HTTP.
ms.assetid: bcb59457-fd22-4166-8a72-ba85209ec8c7
topic_type:
- apiref
api_name:
- HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96b7c34d453c1b9bbe45cf2c85ad268b414f3439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509518"
---
# <a name="http_response_flag_-constants"></a><span data-ttu-id="caa22-103">\_ \_ Constantes d’indicateur de réponse http \_</span><span class="sxs-lookup"><span data-stu-id="caa22-103">HTTP\_RESPONSE\_FLAG\_ Constants</span></span>

<span data-ttu-id="caa22-104">Les constantes de l' **\_ \_ \_ indicateur de réponse http** définissent les options permettant de configurer les réponses dans l’API du serveur http.</span><span class="sxs-lookup"><span data-stu-id="caa22-104">The **HTTP\_RESPONSE\_FLAG\_** constants define options to configure responses in the HTTP Server API.</span></span>

<span data-ttu-id="caa22-105">Ces constantes sont utilisées dans le membre **Flags** de la structure de [**\_ réponse http \_ v1**](/windows/desktop/api/Http/ns-http-http_response_v1) .</span><span class="sxs-lookup"><span data-stu-id="caa22-105">These constants are used in the **Flags** member of the [**HTTP\_RESPONSE\_V1**](/windows/desktop/api/Http/ns-http-http_response_v1) structure.</span></span>

<dl> <dt>

<span data-ttu-id="caa22-106"><span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**indicateur de réponse HTTP- \_ \_ \_ plusieurs \_ encodages \_ disponibles**</span><span class="sxs-lookup"><span data-stu-id="caa22-106"><span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**HTTP\_RESPONSE\_FLAG\_MULTIPLE\_ENCODINGS\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="caa22-107">Les encodages autres que le format d’identité sont disponibles pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="caa22-107">Encodings other than identity form are available for this resource.</span></span> <span data-ttu-id="caa22-108">Cet indicateur est ignoré si l’application n’a pas demandé la mise en cache de la réponse.</span><span class="sxs-lookup"><span data-stu-id="caa22-108">This flag is ignored if the application has not asked for the response to be cached.</span></span> <span data-ttu-id="caa22-109">Il est utilisé comme indicateur de l’API du serveur HTTP pour la négociation de contenu lors de la fourniture à partir du cache de réponse du noyau.</span><span class="sxs-lookup"><span data-stu-id="caa22-109">It's used as a hint to the HTTP Server API for content negotiation when serving from the kernel response cache.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="caa22-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="caa22-110">Requirements</span></span>



| <span data-ttu-id="caa22-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="caa22-111">Requirement</span></span> | <span data-ttu-id="caa22-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="caa22-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="caa22-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caa22-113">Minimum supported client</span></span><br/> | <span data-ttu-id="caa22-114">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="caa22-114">Windows 7 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="caa22-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caa22-115">Minimum supported server</span></span><br/> | <span data-ttu-id="caa22-116">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="caa22-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="caa22-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="caa22-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="caa22-118"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="caa22-118"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caa22-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="caa22-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caa22-120">Constantes de la version 2,0 de l’API du serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="caa22-120">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="caa22-121">**\_Réponse http \_ v1**</span><span class="sxs-lookup"><span data-stu-id="caa22-121">**HTTP\_RESPONSE\_V1**</span></span>](/windows/desktop/api/Http/ns-http-http_response_v1)
</dt> </dl>

 

 





