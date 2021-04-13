---
title: Méthode GetDistinguishedName de la classe MicrosoftDNS_Server
description: La méthode GetDistinguishedName récupère le nom unique du service d’annuaire pour la zone. | Méthode GetDistinguishedName de la classe MicrosoftDNS_Server
ms.assetid: b8c7fc18-87d6-4653-b837-760d6584d9e7
keywords:
- Méthode GetDistinguishedName DNS
- Méthode GetDistinguishedName DNS, classe MicrosoftDNS_Server
- MicrosoftDNS_Server de la classe DNS, méthode GetDistinguishedName
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8caf66c318b0a00973f287513ae495cdf3479edc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321857"
---
# <a name="getdistinguishedname-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="e3d4c-107">Méthode GetDistinguishedName de la \_ classe de serveur MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="e3d4c-107">GetDistinguishedName method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="e3d4c-108">La méthode **GetDistinguishedName** récupère le nom unique du service d’annuaire pour la zone.</span><span class="sxs-lookup"><span data-stu-id="e3d4c-108">The **GetDistinguishedName** method retrieves the DS distinguished name for the zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3d4c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3d4c-109">Syntax</span></span>


```mof
string GetDistinguishedName();
```



## <a name="parameters"></a><span data-ttu-id="e3d4c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3d4c-110">Parameters</span></span>

<span data-ttu-id="e3d4c-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e3d4c-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e3d4c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e3d4c-112">Return value</span></span>

<span data-ttu-id="e3d4c-113">Retourne le nom unique des services de domaine pour la zone.</span><span class="sxs-lookup"><span data-stu-id="e3d4c-113">Returns the DS distinguished name for the zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3d4c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3d4c-114">Requirements</span></span>



| <span data-ttu-id="e3d4c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3d4c-115">Requirement</span></span> | <span data-ttu-id="e3d4c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3d4c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3d4c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3d4c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e3d4c-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3d4c-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e3d4c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3d4c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e3d4c-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3d4c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e3d4c-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e3d4c-121">Namespace</span></span><br/>                | <span data-ttu-id="e3d4c-122">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="e3d4c-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e3d4c-123">MOF</span><span class="sxs-lookup"><span data-stu-id="e3d4c-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3d4c-124"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3d4c-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3d4c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3d4c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3d4c-126">**\_Serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e3d4c-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="e3d4c-127">**Méthode StartService de la \_ classe de serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e3d4c-127">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="e3d4c-128">**Méthode StartScavenging de la \_ classe de serveur MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e3d4c-128">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> </dl>

 

 





