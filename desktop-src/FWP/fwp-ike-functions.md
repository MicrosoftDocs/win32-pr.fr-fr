---
title: Fonctions IKE/AuthIP
description: Fonctions (WFP) utilisées pour interagir avec les modules de gestion de clés \ 8212 ; protocole IKE (Internet Key Exchange) (IKE), protocole IKE (Internet Key Exchange) v2 (IKEv2) et protocole Authenticated IP (Authenticated Internet Protocol) (AuthIP).
ms.assetid: df36b6cc-a304-4426-8f16-1bf92fd721e1
keywords:
- API de la plateforme de filtrage Windows protocole IKE (Internet Key Exchange) fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cce5d3e2393bb1a83ebf816375f537318bb4b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310554"
---
# <a name="ikeauthip-functions"></a><span data-ttu-id="45510-104">Fonctions IKE/AuthIP</span><span class="sxs-lookup"><span data-stu-id="45510-104">IKE/AuthIP Functions</span></span>

<span data-ttu-id="45510-105">Les fonctions de plateforme de filtrage Windows (WFP) utilisées pour interagir avec les protocole IKE (Internet Key Exchange) modules de gestion de clés (IKE), protocole IKE (Internet Key Exchange) v2 (IKEv2) et protocole Authenticated IP (Authenticated Internet Protocol) (AuthIP), sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="45510-105">The Windows Filtering Platform (WFP) functions used to interact with keying modules—Internet Key Exchange (IKE), Internet Key Exchange v2 (IKEv2), and Authenticated Internet Protocol (AuthIP)—are as follows.</span></span>

-   <span data-ttu-id="45510-106">IkeextGetStatistics:</span><span class="sxs-lookup"><span data-stu-id="45510-106">IkeextGetStatistics:</span></span>
    -   <span data-ttu-id="45510-107">[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="45510-107">[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0) (Windows Vista)</span></span>
    -   <span data-ttu-id="45510-108">[**IkeextGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics1) (Windows 7 et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="45510-108">[**IkeextGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="45510-109">**IkeextSaCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="45510-109">**IkeextSaCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)
-   [<span data-ttu-id="45510-110">**IkeextSaDbGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="45510-110">**IkeextSaDbGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadbgetsecurityinfo0)
-   [<span data-ttu-id="45510-111">**IkeextSaDbSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="45510-111">**IkeextSaDbSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadbsetsecurityinfo0)
-   [<span data-ttu-id="45510-112">**IkeextSaDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="45510-112">**IkeextSaDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)
-   [<span data-ttu-id="45510-113">**IkeextSaDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="45510-113">**IkeextSaDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadestroyenumhandle0)
-   <span data-ttu-id="45510-114">IkeextSaEnum:</span><span class="sxs-lookup"><span data-stu-id="45510-114">IkeextSaEnum:</span></span>
    -   <span data-ttu-id="45510-115">[**IkeextSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="45510-115">[**IkeextSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum0) (Windows Vista)</span></span>
    -   <span data-ttu-id="45510-116">[**IkeextSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="45510-116">[**IkeextSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum1) (Windows 7)</span></span>
    -   <span data-ttu-id="45510-117">[**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="45510-117">[**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2) (Windows 8)</span></span>
-   <span data-ttu-id="45510-118">IkeextSaGetById:</span><span class="sxs-lookup"><span data-stu-id="45510-118">IkeextSaGetById:</span></span>
    -   <span data-ttu-id="45510-119">[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="45510-119">[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0) (Windows Vista)</span></span>
    -   <span data-ttu-id="45510-120">[**IkeextSaGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="45510-120">[**IkeextSaGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid1) (Windows 7)</span></span>
    -   <span data-ttu-id="45510-121">[**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="45510-121">[**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2) (Windows 8)</span></span>

 

 




