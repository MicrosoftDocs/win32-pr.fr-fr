---
description: L’API de distribution d’homologue définit les types de données suivants.
ms.assetid: 5a378965-696c-4205-b9de-bdf93f00018f
title: Types de données de l’API de distribution d’homologue (Peerdist. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a7bff6fe75c8f4632248c92af37aea6e00c3052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544866"
---
# <a name="peer-distribution-api-data-types"></a><span data-ttu-id="2bfe4-103">Types de données de l’API de distribution d’homologue</span><span class="sxs-lookup"><span data-stu-id="2bfe4-103">Peer Distribution API Data Types</span></span>

<span data-ttu-id="2bfe4-104">L’API de distribution d’homologue définit les types de données suivants.</span><span class="sxs-lookup"><span data-stu-id="2bfe4-104">The Peer Distribution API defines the following data types.</span></span>


```C++
typedef HANDLE PEERDIST_INSTANCE_HANDLE;
typedef HANDLE PEERDIST_CONTENT_HANDLE;
typedef HANDLE PEERDIST_CONTENTINFO_HANDLE;
typedef HANDLE PEERDIST_STREAM_HANDLE;
```





| <span data-ttu-id="2bfe4-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="2bfe4-105">Data type</span></span>                                                                                                                     | <span data-ttu-id="2bfe4-106">Description</span><span class="sxs-lookup"><span data-stu-id="2bfe4-106">Description</span></span>                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bfe4-107"><span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**\_handle d’instance PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="2bfe4-107"><span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**PEERDIST\_INSTANCE\_HANDLE**</span></span>          | <span data-ttu-id="2bfe4-108">Handle associé à l’instance de distribution d’homologue.</span><span class="sxs-lookup"><span data-stu-id="2bfe4-108">A handle associated with the Peer Distribution instance.</span></span> <span data-ttu-id="2bfe4-109">Ce handle est créé par [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)et utilisé dans la plupart des opérations de distribution d’homologue.</span><span class="sxs-lookup"><span data-stu-id="2bfe4-109">This handle is created by [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup), and used in most Peer Distribution operations.</span></span><br/>                                          |
| <span data-ttu-id="2bfe4-110"><span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**\_descripteur de contenu PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="2bfe4-110"><span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**PEERDIST\_CONTENT\_HANDLE**</span></span>             | <span data-ttu-id="2bfe4-111">Handle associé au contenu.</span><span class="sxs-lookup"><span data-stu-id="2bfe4-111">A handle associated with content.</span></span> <span data-ttu-id="2bfe4-112">Ce handle est créé par [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) et est référencé lors de l’ouverture, de la fermeture, de l’ajout ou de la publication de contenu.</span><span class="sxs-lookup"><span data-stu-id="2bfe4-112">This handle is created by [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) and is referenced when opening, closing, adding, or publishing content.</span></span><br/>                     |
| <span data-ttu-id="2bfe4-113"><span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**\_descripteur PEERDIST CONTENTINFO \_**</span><span class="sxs-lookup"><span data-stu-id="2bfe4-113"><span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**PEERDIST\_CONTENTINFO\_HANDLE**</span></span> | <span data-ttu-id="2bfe4-114">Handle associé aux informations de contenu.</span><span class="sxs-lookup"><span data-stu-id="2bfe4-114">A handle associated with content information.</span></span> <span data-ttu-id="2bfe4-115">Ce handle est créé par [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)et est utilisé lors de la récupération des informations de contenu encodé.</span><span class="sxs-lookup"><span data-stu-id="2bfe4-115">This handle is created by [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation), and is used when retrieving encoded content information.</span></span><br/> |
| <span data-ttu-id="2bfe4-116"><span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**\_handle de flux PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="2bfe4-116"><span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**PEERDIST\_STREAM\_HANDLE**</span></span>                | <span data-ttu-id="2bfe4-117">Handle associé à un flux de données.</span><span class="sxs-lookup"><span data-stu-id="2bfe4-117">A handle associated with a data stream.</span></span> <span data-ttu-id="2bfe4-118">Ce handle est créé par [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) et est référencé lors de la publication, de la fermeture ou de l’ajout du contenu diffusé en continu.</span><span class="sxs-lookup"><span data-stu-id="2bfe4-118">This handle is created by [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) and is referenced when publishing, closing, or adding to streamed content.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="2bfe4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2bfe4-119">Requirements</span></span>



| <span data-ttu-id="2bfe4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2bfe4-120">Requirement</span></span> | <span data-ttu-id="2bfe4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2bfe4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2bfe4-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bfe4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2bfe4-123">Applications de bureau Windows 7 professionnel \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2bfe4-123">Windows 7 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2bfe4-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bfe4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2bfe4-125">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2bfe4-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2bfe4-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="2bfe4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bfe4-127"><dt>Peerdist. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bfe4-127"><dt>Peerdist.h</dt></span></span> </dl> |



 

 




