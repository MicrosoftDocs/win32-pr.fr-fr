---
title: Structures RPC
description: Cette section décrit les structures définies et utilisées par Microsoft RPC.
ms.assetid: 8d2f31f6-21d3-402c-b84b-960a2d03ff40
keywords:
- Appel de procédure distante RPC, référence, structures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94d03209af8b14f87cd8b15929389b6eb524833
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729404"
---
# <a name="rpc-structures"></a><span data-ttu-id="58bd0-104">Structures RPC</span><span class="sxs-lookup"><span data-stu-id="58bd0-104">RPC Structures</span></span>

<span data-ttu-id="58bd0-105">Cette section décrit les structures définies et utilisées par Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="58bd0-105">This section explains the structures defined and used by Microsoft RPC.</span></span>

-   <span data-ttu-id="58bd0-106">[**rapport de non-remise \_ SCONTEXT**](/previous-versions/aa374336(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="58bd0-106">[**NDR\_SCONTEXT**](/previous-versions/aa374336(v=vs.80))</span></span>
-   [<span data-ttu-id="58bd0-107">**UNIQUES**</span><span class="sxs-lookup"><span data-stu-id="58bd0-107">**GUID**</span></span>](/windows/win32/api/guiddef/ns-guiddef-guid)
-   [<span data-ttu-id="58bd0-108">**\_informations de \_ marshaling d’utilisateur NDR \_**</span><span class="sxs-lookup"><span data-stu-id="58bd0-108">**NDR\_USER\_MARSHAL\_INFO**</span></span>](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info)
-   [<span data-ttu-id="58bd0-109">**\_Informations de marshaling d’utilisateur de rapport de non- \_ \_ \_ niveau1**</span><span class="sxs-lookup"><span data-stu-id="58bd0-109">**NDR\_USER\_MARSHAL\_INFO\_LEVEL1**</span></span>](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info_level1)
-   [<span data-ttu-id="58bd0-110">**\_informations de \_ notification RPC asynchrone \_**</span><span class="sxs-lookup"><span data-stu-id="58bd0-110">**RPC\_ASYNC\_NOTIFICATION\_INFO**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_notification_info)
-   [<span data-ttu-id="58bd0-111">**\_état RPC asynchrone \_**</span><span class="sxs-lookup"><span data-stu-id="58bd0-111">**RPC\_ASYNC\_STATE**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_state)
-   [<span data-ttu-id="58bd0-112">**\_Options de handle de liaison RPC \_ \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="58bd0-112">**RPC\_BINDING\_HANDLE\_OPTIONS\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_options_v1)
-   [<span data-ttu-id="58bd0-113">**Gestion de la liaison RPC de la \_ \_ \_ sécurité \_ v1**</span><span class="sxs-lookup"><span data-stu-id="58bd0-113">**RPC\_BINDING\_HANDLE\_SECURITY\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_security_v1_a)
-   [<span data-ttu-id="58bd0-114">**\_Modèle de handle de liaison RPC \_ \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="58bd0-114">**RPC\_BINDING\_HANDLE\_TEMPLATE\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_template_v1_a)
-   [<span data-ttu-id="58bd0-115">**\_vecteur de liaison RPC \_**</span><span class="sxs-lookup"><span data-stu-id="58bd0-115">**RPC\_BINDING\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_vector)
-   [<span data-ttu-id="58bd0-116">**\_descripteur d’authentification de cookie RPC C \_ OPT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="58bd0-116">**RPC\_C\_OPT\_COOKIE\_AUTH\_DESCRIPTOR**</span></span>](/windows/win32/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor)
-   [<span data-ttu-id="58bd0-117">**\_Attributs d’appel RPC \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="58bd0-117">**RPC\_CALL\_ATTRIBUTES\_V1**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v1_a)
-   [<span data-ttu-id="58bd0-118">**\_Attributs d’appel RPC \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="58bd0-118">**RPC\_CALL\_ATTRIBUTES\_V2**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v2_a)
-   [<span data-ttu-id="58bd0-119">**\_Adresse locale d’appel RPC \_ \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="58bd0-119">**RPC\_CALL\_LOCAL\_ADDRESS\_V1**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_call_local_address_v1)
-   [<span data-ttu-id="58bd0-120">**\_interface client \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="58bd0-120">**RPC\_CLIENT\_INTERFACE**</span></span>](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_client_interface)
-   [<span data-ttu-id="58bd0-121">**\_table de dispatch RPC \_**</span><span class="sxs-lookup"><span data-stu-id="58bd0-121">**RPC\_DISPATCH\_TABLE**</span></span>](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_dispatch_table)
-   [<span data-ttu-id="58bd0-122">**\_ \_ param info RPC \_ EE**</span><span class="sxs-lookup"><span data-stu-id="58bd0-122">**RPC\_EE\_INFO\_PARAM**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_ee_info_param)
-   [<span data-ttu-id="58bd0-123">**\_modèle de point de terminaison RPC \_**</span><span class="sxs-lookup"><span data-stu-id="58bd0-123">**RPC\_ENDPOINT\_TEMPLATE**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_endpoint_template)
-   [<span data-ttu-id="58bd0-124">**HANDLE de l' \_ énumération des erreurs RPC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="58bd0-124">**RPC\_ERROR\_ENUM\_HANDLE**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_error_enum_handle)
-   [<span data-ttu-id="58bd0-125">**\_ \_ informations sur l’erreur étendue RPC \_**</span><span class="sxs-lookup"><span data-stu-id="58bd0-125">**RPC\_EXTENDED\_ERROR\_INFO**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info)
-   [<span data-ttu-id="58bd0-126">**\_ \_ informations d’identification du transport RPC HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="58bd0-126">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_a)
-   [<span data-ttu-id="58bd0-127">**\_ \_ Informations d’identification de transport RPC HTTP \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="58bd0-127">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS\_V2**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v2_a)
-   [<span data-ttu-id="58bd0-128">**\_ \_ Informations d’identification de transport RPC HTTP \_ \_ v3**</span><span class="sxs-lookup"><span data-stu-id="58bd0-128">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS\_V3**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v3_a)
-   [<span data-ttu-id="58bd0-129">**\_ID RPC si \_**</span><span class="sxs-lookup"><span data-stu-id="58bd0-129">**RPC\_IF\_ID**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id)
-   [<span data-ttu-id="58bd0-130">**\_vecteur RPC si \_ ID \_**</span><span class="sxs-lookup"><span data-stu-id="58bd0-130">**RPC\_IF\_ID\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id_vector)
-   [<span data-ttu-id="58bd0-131">**\_modèle d’interface RPC \_**</span><span class="sxs-lookup"><span data-stu-id="58bd0-131">**RPC\_INTERFACE\_TEMPLATE**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_interface_template)
-   [<span data-ttu-id="58bd0-132">**\_stratégie RPC**</span><span class="sxs-lookup"><span data-stu-id="58bd0-132">**RPC\_POLICY**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_policy)
-   [<span data-ttu-id="58bd0-133">**\_vecteur PROTSEQ \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="58bd0-133">**RPC\_PROTSEQ\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_protseq_vector)
-   [<span data-ttu-id="58bd0-134">**\_QoS de sécurité RPC \_**</span><span class="sxs-lookup"><span data-stu-id="58bd0-134">**RPC\_SECURITY\_QOS**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos)
-   [<span data-ttu-id="58bd0-135">**\_QoS de sécurité RPC \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="58bd0-135">**RPC\_SECURITY\_QOS\_V2**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v2_a)
-   [<span data-ttu-id="58bd0-136">**\_QoS de sécurité RPC \_ \_ v3**</span><span class="sxs-lookup"><span data-stu-id="58bd0-136">**RPC\_SECURITY\_QOS\_V3**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v3_a)
-   [<span data-ttu-id="58bd0-137">**\_QoS de sécurité RPC \_ \_ v4**</span><span class="sxs-lookup"><span data-stu-id="58bd0-137">**RPC\_SECURITY\_QOS\_V4**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v4_a)
-   [<span data-ttu-id="58bd0-138">**\_QoS de sécurité RPC \_ \_ v5**</span><span class="sxs-lookup"><span data-stu-id="58bd0-138">**RPC\_SECURITY\_QOS\_V5**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v5_a)
-   [<span data-ttu-id="58bd0-139">**\_vecteur des statistiques RPC \_**</span><span class="sxs-lookup"><span data-stu-id="58bd0-139">**RPC\_STATS\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_stats_vector)
-   [<span data-ttu-id="58bd0-140">**s \_ \_ identité d’authentification Winnt \_**</span><span class="sxs-lookup"><span data-stu-id="58bd0-140">**SEC\_WINNT\_AUTH\_IDENTITY**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a)
-   [<span data-ttu-id="58bd0-141">**UUID**</span><span class="sxs-lookup"><span data-stu-id="58bd0-141">**UUID**</span></span>](./rpcdce/ns-rpcdce-uuid.md)
-   [<span data-ttu-id="58bd0-142">**\_vecteur UUID**</span><span class="sxs-lookup"><span data-stu-id="58bd0-142">**UUID\_VECTOR**</span></span>](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)

 

 