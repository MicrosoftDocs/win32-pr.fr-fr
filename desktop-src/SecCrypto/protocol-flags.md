---
description: Constantes prédéfinies pour les protocoles de chiffrement. Ces valeurs sont définies dans wincrypt. h.
ms.assetid: 61dc0eff-2033-464a-a558-1798a92d48a2
title: Indicateurs de protocole (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25804763e407ff2a12e5657878e343f483d353e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952621"
---
# <a name="protocol-flags"></a><span data-ttu-id="615f1-104">Indicateurs de protocole</span><span class="sxs-lookup"><span data-stu-id="615f1-104">Protocol Flags</span></span>

<span data-ttu-id="615f1-105">Les éléments suivants sont des constantes prédéfinies pour les protocoles de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="615f1-105">The following are predefined constants for cryptography protocols.</span></span> <span data-ttu-id="615f1-106">Ces valeurs sont définies dans wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="615f1-106">These values are defined in Wincrypt.h.</span></span>



| <span data-ttu-id="615f1-107">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="615f1-107">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="615f1-108">Description</span><span class="sxs-lookup"><span data-stu-id="615f1-108">Description</span></span>                                                           |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="CRYPT_FLAG_IPSEC"></span><span id="crypt_flag_ipsec"></span><dl> <span data-ttu-id="615f1-109"><dt>**Crypt \_ BALIser \_ IPSec**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="615f1-109"><dt>**CRYPT\_FLAG\_IPSEC**</dt> <dt>0x0010</dt></span></span> </dl>       | <span data-ttu-id="615f1-110">Protocole IPsec (Internet Protocol Security).</span><span class="sxs-lookup"><span data-stu-id="615f1-110">Internet protocol security (IPsec) protocol.</span></span><br/>               |
| <span id="CRYPT_FLAG_PCT1"></span><span id="crypt_flag_pct1"></span><dl> <span data-ttu-id="615f1-111"><dt>**Crypt \_ INDICATEUR \_ PCT1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="615f1-111"><dt>**CRYPT\_FLAG\_PCT1**</dt> <dt>0x0001</dt></span></span> </dl>          | <span data-ttu-id="615f1-112">Protocole PCT (Private communications transport) version 1.</span><span class="sxs-lookup"><span data-stu-id="615f1-112">Private communications transport (PCT) version 1 protocol.</span></span><br/> |
| <span id="CRYPT_FLAG_SIGNING"></span><span id="crypt_flag_signing"></span><dl> <span data-ttu-id="615f1-113"><dt>**Crypt \_ SIGNALER la \_ signature**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="615f1-113"><dt>**CRYPT\_FLAG\_SIGNING**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="615f1-114">Protocole de signature.</span><span class="sxs-lookup"><span data-stu-id="615f1-114">Signing protocol.</span></span><br/>                                          |
| <span id="CRYPT_FLAG_SSL2"></span><span id="crypt_flag_ssl2"></span><dl> <span data-ttu-id="615f1-115"><dt>**Crypt \_ INDICATEUR \_ SSL2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="615f1-115"><dt>**CRYPT\_FLAG\_SSL2**</dt> <dt>0x0002</dt></span></span> </dl>          | <span data-ttu-id="615f1-116">Protocole SSL (Secure Sockets Layer) version 2.</span><span class="sxs-lookup"><span data-stu-id="615f1-116">Secure sockets layer (SSL) version 2 protocol.</span></span><br/>             |
| <span id="CRYPT_FLAG_SSL3"></span><span id="crypt_flag_ssl3"></span><dl> <span data-ttu-id="615f1-117"><dt>**Crypt \_ SIGNALER \_ SSL3**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="615f1-117"><dt>**CRYPT\_FLAG\_SSL3**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="615f1-118">Protocole SSL version 3.</span><span class="sxs-lookup"><span data-stu-id="615f1-118">SSL version 3 protocol.</span></span><br/>                                    |
| <span id="CRYPT_FLAG_TLS1"></span><span id="crypt_flag_tls1"></span><dl> <span data-ttu-id="615f1-119"><dt>**Crypt \_ INDICATEUR \_ TLS1**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="615f1-119"><dt>**CRYPT\_FLAG\_TLS1**</dt> <dt>0x0008</dt></span></span> </dl>          | <span data-ttu-id="615f1-120">Protocole TLS (Transport Layer Security) version 1.</span><span class="sxs-lookup"><span data-stu-id="615f1-120">Transport layer security (TLS) version 1 protocol.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="615f1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="615f1-121">Requirements</span></span>



| <span data-ttu-id="615f1-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="615f1-122">Requirement</span></span> | <span data-ttu-id="615f1-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="615f1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="615f1-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="615f1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="615f1-125">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="615f1-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="615f1-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="615f1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="615f1-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="615f1-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="615f1-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="615f1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="615f1-129"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="615f1-129"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="615f1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="615f1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="615f1-131">**PROV \_ ENUMALGS \_ ex**</span><span class="sxs-lookup"><span data-stu-id="615f1-131">**PROV\_ENUMALGS\_EX**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex)
</dt> </dl>

 

 




