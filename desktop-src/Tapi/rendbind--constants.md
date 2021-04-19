---
description: 'Les constantes RENDBIND sont des indicateurs utilisés par la méthode ITDirectory :: bind pour indiquer les types d’authentification fournis.'
ms.assetid: 27bcf36a-1826-4603-9821-22fcc5c1e186
title: Constantes RENDBIND_ (rend. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badd2a48b2ae0632e317522533c664d4f74a6c77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525558"
---
# <a name="rendbind_-constants"></a><span data-ttu-id="d704b-103">\_Constantes RENDBIND</span><span class="sxs-lookup"><span data-stu-id="d704b-103">RENDBIND\_ Constants</span></span>

<span data-ttu-id="d704b-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d704b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d704b-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="d704b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d704b-106">Les constantes RENDBIND sont des indicateurs utilisés par la méthode [**ITDirectory :: bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) pour indiquer les types d’authentification fournis.</span><span class="sxs-lookup"><span data-stu-id="d704b-106">The RENDBIND constants are flags used by the [**ITDirectory::Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) method to indicate types of authentication supplied.</span></span>

<dl> <dt>

<span data-ttu-id="d704b-107"><span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**\_authentification RENDBIND**</span><span class="sxs-lookup"><span data-stu-id="d704b-107"><span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**RENDBIND\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="d704b-108">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d704b-108">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="d704b-109">Authentifier l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d704b-109">Authenticate user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d704b-110"><span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**RENDBIND \_ DEFAULTDOMAINNAME**</span><span class="sxs-lookup"><span data-stu-id="d704b-110"><span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**RENDBIND\_DEFAULTDOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="d704b-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d704b-111">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="d704b-112">Utilisez le nom de domaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="d704b-112">Use default domain name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d704b-113"><span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**RENDBIND \_ DEFAULTUSERNAME**</span><span class="sxs-lookup"><span data-stu-id="d704b-113"><span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**RENDBIND\_DEFAULTUSERNAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="d704b-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="d704b-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="d704b-115">Utilisez le nom d’utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="d704b-115">Use default user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d704b-116"><span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**RENDBIND \_ DEFAULTPASSWORD**</span><span class="sxs-lookup"><span data-stu-id="d704b-116"><span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**RENDBIND\_DEFAULTPASSWORD**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="d704b-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d704b-117">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="d704b-118">Utilisez le mot de passe par défaut.</span><span class="sxs-lookup"><span data-stu-id="d704b-118">Use default password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d704b-119"><span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**RENDBIND \_ DEFAULTCREDENTIALS**</span><span class="sxs-lookup"><span data-stu-id="d704b-119"><span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**RENDBIND\_DEFAULTCREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="d704b-120">0x0000000e</span><span class="sxs-lookup"><span data-stu-id="d704b-120">0x0000000e</span></span>
</dt> <dt>



<span data-ttu-id="d704b-121">Les trois précédents, ensemble, pour des raisons pratiques.</span><span class="sxs-lookup"><span data-stu-id="d704b-121">The previous three ORed together for convenience.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d704b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d704b-122">Requirements</span></span>



| <span data-ttu-id="d704b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d704b-123">Requirement</span></span> | <span data-ttu-id="d704b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d704b-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d704b-125">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="d704b-125">TAPI version</span></span><br/> | <span data-ttu-id="d704b-126">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="d704b-126">Requires TAPI 3.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d704b-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="d704b-127">Header</span></span><br/>       | <dl> <span data-ttu-id="d704b-128"><dt>Rend. h</dt></span><span class="sxs-lookup"><span data-stu-id="d704b-128"><dt>Rend.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d704b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d704b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d704b-130">**ITDirectory**</span><span class="sxs-lookup"><span data-stu-id="d704b-130">**ITDirectory**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[<span data-ttu-id="d704b-131">**ITDirectory :: bind**</span><span class="sxs-lookup"><span data-stu-id="d704b-131">**ITDirectory::Bind**</span></span>](/windows/desktop/api/Rend/nf-rend-itdirectory-bind)
</dt> </dl>

 

 




