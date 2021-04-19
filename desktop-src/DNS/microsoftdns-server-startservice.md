---
title: Méthode StartService de la classe MicrosoftDNS_Server
description: La méthode StartService démarre le serveur DNS.
ms.assetid: f6343a34-9d1b-4f82-897e-289650af6be9
keywords:
- Méthode StartService DNS
- Méthode StartService DNS, classe MicrosoftDNS_Server
- MicrosoftDNS_Server de la classe DNS, StartService, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e103b3d2648bf2c061eb047090cfdfeb907518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106544171"
---
# <a name="startservice-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="4bb12-106">Méthode StartService de la \_ classe de serveur MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="4bb12-106">StartService method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="4bb12-107">La méthode **StartService** démarre le serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="4bb12-107">The **StartService** method starts the DNS Server.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bb12-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4bb12-108">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="4bb12-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4bb12-109">Parameters</span></span>

<span data-ttu-id="4bb12-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4bb12-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4bb12-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4bb12-111">Return value</span></span>

<span data-ttu-id="4bb12-112">ERREUR \_ : la réussite indique que le service a été correctement démarré.</span><span class="sxs-lookup"><span data-stu-id="4bb12-112">ERROR\_SUCCESS indicates the service was successfully started.</span></span> <span data-ttu-id="4bb12-113">Toute autre valeur est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4bb12-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bb12-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4bb12-114">Requirements</span></span>



| <span data-ttu-id="4bb12-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4bb12-115">Requirement</span></span> | <span data-ttu-id="4bb12-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bb12-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bb12-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bb12-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4bb12-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bb12-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4bb12-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bb12-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4bb12-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4bb12-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4bb12-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4bb12-121">Namespace</span></span><br/>                | <span data-ttu-id="4bb12-122">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="4bb12-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4bb12-123">MOF</span><span class="sxs-lookup"><span data-stu-id="4bb12-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4bb12-124"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4bb12-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bb12-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bb12-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bb12-126">**\_Serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4bb12-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="4bb12-127">**Méthode StopService de la \_ classe de serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4bb12-127">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="4bb12-128">**Méthode StartScavenging de la \_ classe de serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4bb12-128">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="4bb12-129">**Méthode GetDistinguishedName de la \_ classe de serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4bb12-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





