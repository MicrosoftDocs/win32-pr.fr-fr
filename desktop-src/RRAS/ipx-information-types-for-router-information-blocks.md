---
title: Types d’informations IPX pour les blocs d’informations de routeur
description: Les types d’informations suivants sont répertoriés dans Ipxrtdef. h. Utilisez ces types d’informations avec les fonctions de bloc d’informations de routeur lors de l’exécution du transport IPX.
ms.assetid: 6cbc8415-f5ba-4f84-a23f-dd4f4a54d118
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab4494da951c04433da2cf9b1da20db7ea5f3119
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031605"
---
# <a name="ipx-information-types-for-router-information-blocks"></a><span data-ttu-id="bc6b6-104">Types d’informations IPX pour les blocs d’informations de routeur</span><span class="sxs-lookup"><span data-stu-id="bc6b6-104">IPX Information Types for Router Information Blocks</span></span>

<span data-ttu-id="bc6b6-105">Les types d’informations suivants sont répertoriés dans Ipxrtdef. h.</span><span class="sxs-lookup"><span data-stu-id="bc6b6-105">The following information types are listed in Ipxrtdef.h.</span></span> <span data-ttu-id="bc6b6-106">Utilisez ces types d’informations avec les fonctions de bloc d’informations de routeur lors de l’exécution du transport IPX.</span><span class="sxs-lookup"><span data-stu-id="bc6b6-106">Use these information types with the router information block functions when running the IPX transport.</span></span>



| <span data-ttu-id="bc6b6-107">Type d’informations</span><span class="sxs-lookup"><span data-stu-id="bc6b6-107">Information type</span></span>                              | <span data-ttu-id="bc6b6-108">Structure des informations</span><span class="sxs-lookup"><span data-stu-id="bc6b6-108">Information structure</span></span>                                          |
|-----------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="bc6b6-109">TYPE d’informations de l' \_ adaptateur IPX \_ \_</span><span class="sxs-lookup"><span data-stu-id="bc6b6-109">IPX\_ADAPTER\_INFO\_TYPE</span></span>                      | <span data-ttu-id="bc6b6-110">\_informations sur l’adaptateur IPX \_</span><span class="sxs-lookup"><span data-stu-id="bc6b6-110">IPX\_ADAPTER\_INFO</span></span>                                             |
| <span data-ttu-id="bc6b6-111">\_type d' \_ informations GLOBALes IPX \_</span><span class="sxs-lookup"><span data-stu-id="bc6b6-111">IPX\_GLOBAL\_INFO\_TYPE</span></span>                       | <span data-ttu-id="bc6b6-112">\_informations globales IPX \_</span><span class="sxs-lookup"><span data-stu-id="bc6b6-112">IPX\_GLOBAL\_INFO</span></span>                                              |
| <span data-ttu-id="bc6b6-113">TYPE d’informations de l' \_ interface IPX \_ \_</span><span class="sxs-lookup"><span data-stu-id="bc6b6-113">IPX\_INTERFACE\_INFO\_TYPE</span></span>                    | [<span data-ttu-id="bc6b6-114">**\_informations IPX si \_**</span><span class="sxs-lookup"><span data-stu-id="bc6b6-114">**IPX\_IF\_INFO**</span></span>](/windows/desktop/api/Ipxrtdef/ns-ipxrtdef-ipx_if_info)                           |
| <span data-ttu-id="bc6b6-115">\_type d' \_ \_ \_ informations globales du filtre de \_ trafic IPX \_</span><span class="sxs-lookup"><span data-stu-id="bc6b6-115">IPX\_IN\_TRAFFIC\_FILTER\_GLOBAL\_INFO\_TYPE</span></span>  | <span data-ttu-id="bc6b6-116">\_ \_ \_ informations globales sur le filtre de trafic IPX \_</span><span class="sxs-lookup"><span data-stu-id="bc6b6-116">IPX\_TRAFFIC\_FILTER\_GLOBAL\_INFO</span></span>                             |
| <span data-ttu-id="bc6b6-117">\_type d' \_ \_ \_ informations globales du filtre \_ de trafic \_ IPX out</span><span class="sxs-lookup"><span data-stu-id="bc6b6-117">IPX\_OUT\_TRAFFIC\_FILTER\_GLOBAL\_INFO\_TYPE</span></span> | <span data-ttu-id="bc6b6-118">\_ \_ \_ informations globales sur le filtre de trafic IPX \_</span><span class="sxs-lookup"><span data-stu-id="bc6b6-118">IPX\_TRAFFIC\_FILTER\_GLOBAL\_INFO</span></span>                             |
| <span data-ttu-id="bc6b6-119">\_type d' \_ informations du filtre de trafic \_ \_ IPX \_</span><span class="sxs-lookup"><span data-stu-id="bc6b6-119">IPX\_IN\_TRAFFIC\_FILTER\_INFO\_TYPE</span></span>          | <span data-ttu-id="bc6b6-120">\_ \_ informations sur le filtre de trafic IPX \_</span><span class="sxs-lookup"><span data-stu-id="bc6b6-120">IPX\_TRAFFIC\_FILTER\_INFO</span></span>                                     |
| <span data-ttu-id="bc6b6-121">\_type d' \_ informations du filtre de trafic IPX out \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="bc6b6-121">IPX\_OUT\_TRAFFIC\_FILTER\_INFO\_TYPE</span></span>         | <span data-ttu-id="bc6b6-122">\_ \_ informations sur le filtre de trafic IPX \_</span><span class="sxs-lookup"><span data-stu-id="bc6b6-122">IPX\_TRAFFIC\_FILTER\_INFO</span></span>                                     |
| <span data-ttu-id="bc6b6-123">\_type d' \_ \_ informations du nom NetBIOS statique \_ IPX \_</span><span class="sxs-lookup"><span data-stu-id="bc6b6-123">IPX\_STATIC\_NETBIOS\_NAME\_INFO\_TYPE</span></span>        | <span data-ttu-id="bc6b6-124">\_informations de \_ \_ nom NetBIOS statique IPX \_</span><span class="sxs-lookup"><span data-stu-id="bc6b6-124">IPX\_STATIC\_NETBIOS\_NAME\_INFO</span></span>                               |
| <span data-ttu-id="bc6b6-125">\_type d' \_ informations d’itinéraire statique \_ IPX \_</span><span class="sxs-lookup"><span data-stu-id="bc6b6-125">IPX\_STATIC\_ROUTE\_INFO\_TYPE</span></span>                | <span data-ttu-id="bc6b6-126">\_informations d' \_ itinéraire \_ statique IPX</span><span class="sxs-lookup"><span data-stu-id="bc6b6-126">IPX\_STATIC\_ROUTE\_INFO</span></span>                                       |
| <span data-ttu-id="bc6b6-127">\_type d' \_ informations de service statique \_ IPX \_</span><span class="sxs-lookup"><span data-stu-id="bc6b6-127">IPX\_STATIC\_SERVICE\_INFO\_TYPE</span></span>              | <span data-ttu-id="bc6b6-128">[**\_ \_ informations sur le service statique IPX \_**](/previous-versions/windows/desktop/legacy/aa374456(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bc6b6-128">[**IPX\_STATIC\_SERVICE\_INFO**](/previous-versions/windows/desktop/legacy/aa374456(v=vs.85))</span></span> |
| <span data-ttu-id="bc6b6-129">TYPE d’informations de l' \_ interface ipxwan \_ \_</span><span class="sxs-lookup"><span data-stu-id="bc6b6-129">IPXWAN\_INTERFACE\_INFO\_TYPE</span></span>                 | [<span data-ttu-id="bc6b6-130">**IPXWAN \_ si \_ info**</span><span class="sxs-lookup"><span data-stu-id="bc6b6-130">**IPXWAN\_IF\_INFO**</span></span>](/windows/desktop/api/Ipxrtdef/ns-ipxrtdef-ipxwan_if_info)                     |



 

 

 