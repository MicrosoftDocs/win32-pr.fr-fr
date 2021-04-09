---
description: Représente un handle vers une réponse OCSP associée à une chaîne de certificat de serveur.
ms.assetid: baf173f1-99dc-49f9-9a17-fee79b393db7
title: HCERT_SERVER_OCSP_RESPONSE (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceab319b5d8370dd15ef3dcd288124e4f2adf9ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867414"
---
# <a name="hcert_server_ocsp_response"></a><span data-ttu-id="af815-103">\_ \_ réponse OCSP du serveur HCERT \_</span><span class="sxs-lookup"><span data-stu-id="af815-103">HCERT\_SERVER\_OCSP\_RESPONSE</span></span>

<span data-ttu-id="af815-104">Le type de données de **\_ \_ \_ réponse OCSP du serveur HCERT** représente un handle vers une réponse OCSP associée à une chaîne de certificat de serveur.</span><span class="sxs-lookup"><span data-stu-id="af815-104">The **HCERT\_SERVER\_OCSP\_RESPONSE** data type represents a handle to an OCSP response associated with a server certificate chain.</span></span>

<span data-ttu-id="af815-105">Ce type est utilisé par les API suivantes.</span><span class="sxs-lookup"><span data-stu-id="af815-105">This type is used by the following APIs.</span></span>

-   [<span data-ttu-id="af815-106">**CertOpenServerOcspResponse**</span><span class="sxs-lookup"><span data-stu-id="af815-106">**CertOpenServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenserverocspresponse)
-   [<span data-ttu-id="af815-107">**CertAddRefServerOcspResponse**</span><span class="sxs-lookup"><span data-stu-id="af815-107">**CertAddRefServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponse)
-   [<span data-ttu-id="af815-108">**CertCloseServerOcspResponse**</span><span class="sxs-lookup"><span data-stu-id="af815-108">**CertCloseServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certcloseserverocspresponse)
-   [<span data-ttu-id="af815-109">**CertGetServerOcspResponseContext**</span><span class="sxs-lookup"><span data-stu-id="af815-109">**CertGetServerOcspResponseContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetserverocspresponsecontext)


```C++
typedef VOID* HCERT_SERVER_OCSP_RESPONSE;
```



## <a name="requirements"></a><span data-ttu-id="af815-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af815-110">Requirements</span></span>



| <span data-ttu-id="af815-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af815-111">Requirement</span></span> | <span data-ttu-id="af815-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="af815-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af815-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af815-113">Minimum supported client</span></span><br/> | <span data-ttu-id="af815-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af815-114">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af815-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af815-115">Minimum supported server</span></span><br/> | <span data-ttu-id="af815-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af815-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af815-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="af815-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="af815-118"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="af815-118"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 




