---
title: ODJ_POLICY_DNS_DOMAIN_INFO
description: Définition du ODJ_POLICY_DNS_DOMAIN_INFO IDL
ms.assetid: 44b1145f-3bdd-42cd-a88f-9b41888cc644
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 36b7759451811844a91b3ee66ff3460fa4c4db34
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "103734692"
---
# <a name="odj_policy_dns_domain_info-structure"></a><span data-ttu-id="78073-103">Structure ODJ_POLICY_DNS_DOMAIN_INFO</span><span class="sxs-lookup"><span data-stu-id="78073-103">ODJ_POLICY_DNS_DOMAIN_INFO structure</span></span>

<span data-ttu-id="78073-104">Contient des informations sur le domaine et la forêt auxquels un client doit être joint.</span><span class="sxs-lookup"><span data-stu-id="78073-104">Contains information about the domain and forest that a client should be joined to.</span></span>

## <a name="syntax"></a><span data-ttu-id="78073-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78073-105">Syntax</span></span>

```C++
typedef struct _ODJ_POLICY_DNS_DOMAIN_INFO
{
    ODJ_UNICODE_STRING Name;
    ODJ_UNICODE_STRING DnsDomainName;
    ODJ_UNICODE_STRING DnsForestName;
    GUID DomainGuid;
    PODJ_SID Sid;
} ODJ_POLICY_DNS_DOMAIN_INFO;
```

## <a name="members"></a><span data-ttu-id="78073-106">Membres</span><span class="sxs-lookup"><span data-stu-id="78073-106">Members</span></span>

### <a name="name"></a><span data-ttu-id="78073-107">Nom</span><span class="sxs-lookup"><span data-stu-id="78073-107">Name</span></span>

<span data-ttu-id="78073-108">Doit être défini sur un nom de domaine NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="78073-108">Must be set to a Netbios domain name.</span></span>

### <a name="dnsdomainname"></a><span data-ttu-id="78073-109">DnsDomainName</span><span class="sxs-lookup"><span data-stu-id="78073-109">DnsDomainName</span></span>

<span data-ttu-id="78073-110">Doit être défini sur un nom de domaine au format DNS.</span><span class="sxs-lookup"><span data-stu-id="78073-110">Must be set to a domain name in DNS format.</span></span>

### <a name="dnsforestname"></a><span data-ttu-id="78073-111">DnsForestName</span><span class="sxs-lookup"><span data-stu-id="78073-111">DnsForestName</span></span>

<span data-ttu-id="78073-112">Doit être défini sur un nom de forêt au format DNS.</span><span class="sxs-lookup"><span data-stu-id="78073-112">Must be set to a forest name in DNS format.</span></span>

### <a name="domainguid"></a><span data-ttu-id="78073-113">DomainGuid</span><span class="sxs-lookup"><span data-stu-id="78073-113">DomainGuid</span></span>

<span data-ttu-id="78073-114">Doit être défini sur le GUID du domaine.</span><span class="sxs-lookup"><span data-stu-id="78073-114">Must be set to the domain guid.</span></span>

### <a name="sid"></a><span data-ttu-id="78073-115">SID</span><span class="sxs-lookup"><span data-stu-id="78073-115">Sid</span></span>

<span data-ttu-id="78073-116">Doit être défini sur le SID du domaine.</span><span class="sxs-lookup"><span data-stu-id="78073-116">Must be set to the domain sid.</span></span>

## <a name="see-also"></a><span data-ttu-id="78073-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78073-117">See also</span></span>

[<span data-ttu-id="78073-118">**Définitions IDL de jonction de domaine hors connexion**</span><span class="sxs-lookup"><span data-stu-id="78073-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="78073-119">**\_chaîne Unicode \_ ODJ**</span><span class="sxs-lookup"><span data-stu-id="78073-119">**ODJ\_UNICODE\_STRING**</span></span>](odj-odj_unicode_string.md)

[<span data-ttu-id="78073-120">**\_sid ODJ**</span><span class="sxs-lookup"><span data-stu-id="78073-120">**ODJ\_SID**</span></span>](odj-odj_sid.md)
