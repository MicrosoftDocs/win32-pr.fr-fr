---
title: Méthode StartScavenging de la classe MicrosoftDNS_Server
description: La méthode StartScavenging démarre le nettoyage des enregistrements obsolètes dans les zones soumises au nettoyage.
ms.assetid: ee1bc0e0-9334-4971-a524-4bb8a9015b5b
keywords:
- Méthode StartScavenging DNS
- Méthode StartScavenging DNS, classe MicrosoftDNS_Server
- MicrosoftDNS_Server de la classe DNS, méthode StartScavenging
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartScavenging
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8e1927ed069d3e3e3cf27fd94b1ffd54e6bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942278"
---
# <a name="startscavenging-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="13c03-106">Méthode StartScavenging de la \_ classe de serveur MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="13c03-106">StartScavenging method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="13c03-107">La méthode **StartScavenging** démarre le nettoyage des enregistrements obsolètes dans les zones soumises au nettoyage.</span><span class="sxs-lookup"><span data-stu-id="13c03-107">The **StartScavenging** method starts scavenging stale records in the zones subjected to scavenging.</span></span>

## <a name="syntax"></a><span data-ttu-id="13c03-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13c03-108">Syntax</span></span>


```mof
uint32 StartScavenging();
```



## <a name="parameters"></a><span data-ttu-id="13c03-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13c03-109">Parameters</span></span>

<span data-ttu-id="13c03-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="13c03-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="13c03-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="13c03-111">Return value</span></span>

<span data-ttu-id="13c03-112">ERREUR \_ : la réussite indique que le nettoyage a été correctement démarré.</span><span class="sxs-lookup"><span data-stu-id="13c03-112">ERROR\_SUCCESS indicates the scavenging was successfully started.</span></span> <span data-ttu-id="13c03-113">Toute autre valeur est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="13c03-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="13c03-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13c03-114">Requirements</span></span>



| <span data-ttu-id="13c03-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13c03-115">Requirement</span></span> | <span data-ttu-id="13c03-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="13c03-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13c03-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13c03-117">Minimum supported client</span></span><br/> | <span data-ttu-id="13c03-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="13c03-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="13c03-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13c03-119">Minimum supported server</span></span><br/> | <span data-ttu-id="13c03-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13c03-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="13c03-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="13c03-121">Namespace</span></span><br/>                | <span data-ttu-id="13c03-122">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="13c03-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="13c03-123">MOF</span><span class="sxs-lookup"><span data-stu-id="13c03-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13c03-124"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13c03-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13c03-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13c03-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13c03-126">**\_Serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="13c03-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="13c03-127">**Méthode StartService de la \_ classe de serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="13c03-127">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="13c03-128">**Méthode StopService de la \_ classe de serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="13c03-128">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="13c03-129">**Méthode GetDistinguishedName de la \_ classe de serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="13c03-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





