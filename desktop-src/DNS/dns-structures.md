---
title: Structures DNS
description: Page de navigation structures DNS (Domain Name System).
ms.assetid: 636399be-43a5-4ddf-b652-f8efb81fbf42
keywords:
- Structures du système de noms de domaine
- Structures DNS
- Domain Name System, référence, structures
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 65da2f26026ef1d9fe443fc3cfc05736459a3743
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031637"
---
# <a name="dns-structures"></a><span data-ttu-id="f20b2-106">Structures DNS</span><span class="sxs-lookup"><span data-stu-id="f20b2-106">DNS Structures</span></span>

<span data-ttu-id="f20b2-107">Les structures suivantes sont définies pour une utilisation avec DNS :</span><span class="sxs-lookup"><span data-stu-id="f20b2-107">The following structures are defined for use with DNS:</span></span>

- [<span data-ttu-id="f20b2-108">**DNS_ADDR**</span><span class="sxs-lookup"><span data-stu-id="f20b2-108">**DNS_ADDR**</span></span>](/windows/win32/api/windns/ns-windns-dns_addr)
- [<span data-ttu-id="f20b2-109">**DNS_ADDR_ARRAY**</span><span class="sxs-lookup"><span data-stu-id="f20b2-109">**DNS_ADDR_ARRAY**</span></span>](/windows/win32/api/windns/ns-windns-dns_addr_array)
- [<span data-ttu-id="f20b2-110">**DNS_HEADER**</span><span class="sxs-lookup"><span data-stu-id="f20b2-110">**DNS_HEADER**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_header)
- [<span data-ttu-id="f20b2-111">**DNS_MESSAGE_BUFFER**</span><span class="sxs-lookup"><span data-stu-id="f20b2-111">**DNS_MESSAGE_BUFFER**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_message_buffer)
- [<span data-ttu-id="f20b2-112">**DNS_PROXY_INFORMATION**</span><span class="sxs-lookup"><span data-stu-id="f20b2-112">**DNS_PROXY_INFORMATION**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_proxy_information)
- [<span data-ttu-id="f20b2-113">**DNS_QUERY_REQUEST**</span><span class="sxs-lookup"><span data-stu-id="f20b2-113">**DNS_QUERY_REQUEST**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_query_request)
- [<span data-ttu-id="f20b2-114">**DNS_RECORD**</span><span class="sxs-lookup"><span data-stu-id="f20b2-114">**DNS_RECORD**</span></span>](/windows/win32/api/windns/ns-windns-dns_recorda)
- [<span data-ttu-id="f20b2-115">**DNS_RECORD_FLAGS**</span><span class="sxs-lookup"><span data-stu-id="f20b2-115">**DNS_RECORD_FLAGS**</span></span>](/windows/win32/api/windns/ns-windns-dns_record_flags)
- [<span data-ttu-id="f20b2-116">**DNS_SERVICE_BROWSE_REQUEST**</span><span class="sxs-lookup"><span data-stu-id="f20b2-116">**DNS_SERVICE_BROWSE_REQUEST**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_service_browse_request)
- [<span data-ttu-id="f20b2-117">**DNS_SERVICE_CANCEL**</span><span class="sxs-lookup"><span data-stu-id="f20b2-117">**DNS_SERVICE_CANCEL**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_service_cancel)
- [<span data-ttu-id="f20b2-118">**DNS_SERVICE_INSTANCE**</span><span class="sxs-lookup"><span data-stu-id="f20b2-118">**DNS_SERVICE_INSTANCE**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_service_instance)
- [<span data-ttu-id="f20b2-119">**DNS_SERVICE_REGISTER_REQUEST**</span><span class="sxs-lookup"><span data-stu-id="f20b2-119">**DNS_SERVICE_REGISTER_REQUEST**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_service_register_request)
- [<span data-ttu-id="f20b2-120">**DNS_SERVICE_RESOLVE_REQUEST**</span><span class="sxs-lookup"><span data-stu-id="f20b2-120">**DNS_SERVICE_RESOLVE_REQUEST**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_service_resolve_request)
- [<span data-ttu-id="f20b2-121">**IP4_ARRAY**</span><span class="sxs-lookup"><span data-stu-id="f20b2-121">**IP4_ARRAY**</span></span>](/windows/desktop/api/Windns/ns-windns-ip4_array)
- [<span data-ttu-id="f20b2-122">**IP6_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="f20b2-122">**IP6_ADDRESS**</span></span>](/windows/win32/api/windns/ns-windns-ip6_address)
- [<span data-ttu-id="f20b2-123">**MDNS_QUERY_HANDLE**</span><span class="sxs-lookup"><span data-stu-id="f20b2-123">**MDNS_QUERY_HANDLE**</span></span>](/windows/desktop/api/Windns/ns-windns-mdns_query_handle)
- [<span data-ttu-id="f20b2-124">**MDNS_QUERY_REQUEST**</span><span class="sxs-lookup"><span data-stu-id="f20b2-124">**MDNS_QUERY_REQUEST**</span></span>](/windows/desktop/api/Windns/ns-windns-mdns_query_request)

<span data-ttu-id="f20b2-125">Les structures d’enregistrement de ressource (RR) suivantes sont également incluses dans l’API DNS.</span><span class="sxs-lookup"><span data-stu-id="f20b2-125">The following Resource Record (RR) structures are also included in the DNS API.</span></span> <span data-ttu-id="f20b2-126">Ces structures sont utilisées avec la structure **DNS_RECORD** pour gérer par programme les enregistrements de ressources DNS.</span><span class="sxs-lookup"><span data-stu-id="f20b2-126">These structures are used with the **DNS_RECORD** structure to programmatically manage DNS resource records.</span></span>

- [<span data-ttu-id="f20b2-127">**DNS_A_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-127">**DNS_A_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_a_data)
- [<span data-ttu-id="f20b2-128">**DNS_AAAA_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-128">**DNS_AAAA_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_aaaa_data)
- [<span data-ttu-id="f20b2-129">**DNS_ATMA_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-129">**DNS_ATMA_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_atma_data)
- [<span data-ttu-id="f20b2-130">**DNS_DHCID_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-130">**DNS_DHCID_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_dhcid_data)
- <span data-ttu-id="f20b2-131">[**DNS_DNSKEY_DATA**](/previous-versions/windows/desktop/legacy/dd392295(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f20b2-131">[**DNS_DNSKEY_DATA**](/previous-versions/windows/desktop/legacy/dd392295(v=vs.85))</span></span>
- [<span data-ttu-id="f20b2-132">**DNS_DS_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-132">**DNS_DS_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_ds_data)
- [<span data-ttu-id="f20b2-133">**DNS_KEY_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-133">**DNS_KEY_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_key_data)
- [<span data-ttu-id="f20b2-134">**DNS_LOC_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-134">**DNS_LOC_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_loc_data)
- [<span data-ttu-id="f20b2-135">**DNS_MINFO_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-135">**DNS_MINFO_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_minfo_dataw)
- [<span data-ttu-id="f20b2-136">**DNS_MX_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-136">**DNS_MX_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_mx_dataa)
- [<span data-ttu-id="f20b2-137">**DNS_NAPTR_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-137">**DNS_NAPTR_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_naptr_dataw)
- [<span data-ttu-id="f20b2-138">**DNS_NSEC_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-138">**DNS_NSEC_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_nsec_dataw)
- [<span data-ttu-id="f20b2-139">**DNS_NULL_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-139">**DNS_NULL_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_null_data)
- [<span data-ttu-id="f20b2-140">**DNS_NXT_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-140">**DNS_NXT_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_nxt_dataw)
- [<span data-ttu-id="f20b2-141">**DNS_OPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-141">**DNS_OPT_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_opt_data)
- [<span data-ttu-id="f20b2-142">**DNS_PTR_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-142">**DNS_PTR_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_ptr_dataw)
- [<span data-ttu-id="f20b2-143">**DNS_RRSET**</span><span class="sxs-lookup"><span data-stu-id="f20b2-143">**DNS_RRSET**</span></span>](/windows/win32/api/windns/ns-windns-dns_rrset)
- [<span data-ttu-id="f20b2-144">**DNS_RRSIG_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-144">**DNS_RRSIG_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_sig_dataw)
- <span data-ttu-id="f20b2-145">[**DNS_SIG_DATA**](/previous-versions/windows/desktop/legacy/ms682094(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f20b2-145">[**DNS_SIG_DATA**](/previous-versions/windows/desktop/legacy/ms682094(v=vs.85))</span></span>
- [<span data-ttu-id="f20b2-146">**DNS_SOA_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-146">**DNS_SOA_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_soa_dataw)
- [<span data-ttu-id="f20b2-147">**DNS_SRV_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-147">**DNS_SRV_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_srv_dataw)
- [<span data-ttu-id="f20b2-148">**DNS_TKEY_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-148">**DNS_TKEY_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_tkey_dataw)
- [<span data-ttu-id="f20b2-149">**DNS_TSIG_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-149">**DNS_TSIG_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_tsig_dataw)
- [<span data-ttu-id="f20b2-150">**DNS_TXT_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-150">**DNS_TXT_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_txt_dataw)
- [<span data-ttu-id="f20b2-151">**DNS_WINS_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-151">**DNS_WINS_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_wins_data)
- [<span data-ttu-id="f20b2-152">**DNS_WINSR_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-152">**DNS_WINSR_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_winsr_dataw)
- [<span data-ttu-id="f20b2-153">**DNS_WIRE_QUESTION**</span><span class="sxs-lookup"><span data-stu-id="f20b2-153">**DNS_WIRE_QUESTION**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_wire_question)
- [<span data-ttu-id="f20b2-154">**DNS_WIRE_RECORD**</span><span class="sxs-lookup"><span data-stu-id="f20b2-154">**DNS_WIRE_RECORD**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_wire_record)
- [<span data-ttu-id="f20b2-155">**DNS_WKS_DATA**</span><span class="sxs-lookup"><span data-stu-id="f20b2-155">**DNS_WKS_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_wks_data)