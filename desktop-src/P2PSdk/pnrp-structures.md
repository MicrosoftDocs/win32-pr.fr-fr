---
description: 'L’API du fournisseur d’espace de noms PNRP utilise les structures suivantes :'
ms.assetid: 697fb99a-259f-429c-8818-0d725255bc86
title: Structures PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e2ee85f3673395ade31417c79c010354f16b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518482"
---
# <a name="pnrp-structures"></a><span data-ttu-id="6f9e8-103">Structures PNRP</span><span class="sxs-lookup"><span data-stu-id="6f9e8-103">PNRP Structures</span></span>

<span data-ttu-id="6f9e8-104">L’API du fournisseur d’espace de noms PNRP utilise les structures suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f9e8-104">The PNRP Namespace Provider API uses the following structures:</span></span>



| <span data-ttu-id="6f9e8-105">Structure</span><span class="sxs-lookup"><span data-stu-id="6f9e8-105">Structure</span></span>                                                             | <span data-ttu-id="6f9e8-106">Description</span><span class="sxs-lookup"><span data-stu-id="6f9e8-106">Description</span></span>                                                                                                                                                         |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f9e8-107">**\_ \_ informations sur le point de terminaison PNRP homologue \_**</span><span class="sxs-lookup"><span data-stu-id="6f9e8-107">**PEER\_PNRP\_ENDPOINT\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_endpoint_info)         | <span data-ttu-id="6f9e8-108">Contient les adresses IP et les données associées à un point de terminaison homologue.</span><span class="sxs-lookup"><span data-stu-id="6f9e8-108">Contains the IP addresses and data associated with a peer endpoint.</span></span>                                                                                                 |
| [<span data-ttu-id="6f9e8-109">**\_ \_ informations sur le Cloud PNRP homologue \_**</span><span class="sxs-lookup"><span data-stu-id="6f9e8-109">**PEER\_PNRP\_CLOUD\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_cloud_info)               | <span data-ttu-id="6f9e8-110">Contient des informations sur un Cloud PNRP (Peer Name Resolution Protocol).</span><span class="sxs-lookup"><span data-stu-id="6f9e8-110">Contains information about a Peer Name Resolution Protocol (PNRP) cloud.</span></span>                                                                                            |
| [<span data-ttu-id="6f9e8-111">**\_ \_ informations d’inscription PNRP de l’homologue \_**</span><span class="sxs-lookup"><span data-stu-id="6f9e8-111">**PEER\_PNRP\_REGISTRATION\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_registration_info) | <span data-ttu-id="6f9e8-112">Contient les informations fournies par une identité d’homologue lorsqu’elle s’inscrit auprès d’un Cloud PNRP.</span><span class="sxs-lookup"><span data-stu-id="6f9e8-112">Contains the information provided by a peer identity when it registers with a PNRP cloud.</span></span>                                                                           |
| [<span data-ttu-id="6f9e8-113">PNRP et objet BLOB</span><span class="sxs-lookup"><span data-stu-id="6f9e8-113">PNRP and BLOB</span></span>](pnrp-and-blob.md)                                    | <span data-ttu-id="6f9e8-114">Transmet des données à la structure [**WSAQUERYSET**](winsock-nsp-reference-links.md) lors des appels à plusieurs fonctions.</span><span class="sxs-lookup"><span data-stu-id="6f9e8-114">Passes data to the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure during calls to several functions.</span></span>                                                  |
| [<span data-ttu-id="6f9e8-115">PNRP et WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="6f9e8-115">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)                      | <span data-ttu-id="6f9e8-116">Facilite la résolution des noms et l’énumération des noms et des clouds.</span><span class="sxs-lookup"><span data-stu-id="6f9e8-116">Facilitates the resolving of names and the enumeration of names and clouds.</span></span>                                                                                         |
| [<span data-ttu-id="6f9e8-117">**\_ID de Cloud PNRP \_**</span><span class="sxs-lookup"><span data-stu-id="6f9e8-117">**PNRP\_CLOUD\_ID**</span></span>](/windows/desktop/api/Pnrpdef/ns-pnrpdef-pnrp_cloud_id)                              | <span data-ttu-id="6f9e8-118">Contient les valeurs qui définissent un Cloud réseau.</span><span class="sxs-lookup"><span data-stu-id="6f9e8-118">Contains the values that define a network cloud.</span></span>                                                                                                                    |
| [<span data-ttu-id="6f9e8-119">**PNRPCLOUDINFO**</span><span class="sxs-lookup"><span data-stu-id="6f9e8-119">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)                                | <span data-ttu-id="6f9e8-120">Pointé par le membre **lpBlob** de la structure [**WSAQUERYSET**](winsock-nsp-reference-links.md) .</span><span class="sxs-lookup"><span data-stu-id="6f9e8-120">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure.</span></span>                                                            |
| [<span data-ttu-id="6f9e8-121">**PNRPINFO \_ v1**</span><span class="sxs-lookup"><span data-stu-id="6f9e8-121">**PNRPINFO\_V1**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)                                      | <span data-ttu-id="6f9e8-122">Pointé par le membre **lpBlob** de la structure [**WSAQUERYSET**](winsock-nsp-reference-links.md)</span><span class="sxs-lookup"><span data-stu-id="6f9e8-122">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure</span></span>                                                             |
| <span data-ttu-id="6f9e8-123">[**PNRPINFO \_ v2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6f9e8-123">[**PNRPINFO\_V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))</span></span>                                   | <span data-ttu-id="6f9e8-124">Pointé par le membre **lpBlob** de la structure [**WSAQUERYSET**](winsock-nsp-reference-links.md) , et fournit la prise en charge des données opaques spécifiques à l’application.</span><span class="sxs-lookup"><span data-stu-id="6f9e8-124">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure, and provides support for application-specific opaque data.</span></span> |



 

 

 
