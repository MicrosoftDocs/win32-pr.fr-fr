---
title: Méthode StopService de la classe MicrosoftDNS_Server
description: La méthode StopService arrête le serveur DNS.
ms.assetid: 80637d5b-e43a-4710-b3ab-eec246587788
keywords:
- Méthode StopService DNS
- Méthode StopService DNS, classe MicrosoftDNS_Server
- Classe MicrosoftDNS_Server DNS, méthode StopService
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StopService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f811533c66185304c5c674fdfff2eda8cf5bef69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465675"
---
# <a name="stopservice-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="e3cd4-106">Méthode StopService de la \_ classe de serveur MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="e3cd4-106">StopService method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="e3cd4-107">La méthode **StopService** arrête le serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-107">The **StopService** method stops the DNS Server.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3cd4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3cd4-108">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="e3cd4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3cd4-109">Parameters</span></span>

<span data-ttu-id="e3cd4-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e3cd4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e3cd4-111">Return value</span></span>

<span data-ttu-id="e3cd4-112">ERREUR \_ : la réussite indique que le service a été arrêté avec succès.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-112">ERROR\_SUCCESS indicates the service was successfully stopped.</span></span> <span data-ttu-id="e3cd4-113">Toute autre valeur est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3cd4-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3cd4-114">Requirements</span></span>



| <span data-ttu-id="e3cd4-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3cd4-115">Requirement</span></span> | <span data-ttu-id="e3cd4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3cd4-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3cd4-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3cd4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e3cd4-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3cd4-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e3cd4-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3cd4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e3cd4-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3cd4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e3cd4-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e3cd4-121">Namespace</span></span><br/>                | <span data-ttu-id="e3cd4-122">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="e3cd4-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e3cd4-123">MOF</span><span class="sxs-lookup"><span data-stu-id="e3cd4-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3cd4-124"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3cd4-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3cd4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3cd4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3cd4-126">**\_Serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="e3cd4-127">**Méthode StartService de la \_ classe de serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-127">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="e3cd4-128">**Méthode StartScavenging de la \_ classe de serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-128">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="e3cd4-129">**Méthode GetDistinguishedName de la \_ classe de serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





