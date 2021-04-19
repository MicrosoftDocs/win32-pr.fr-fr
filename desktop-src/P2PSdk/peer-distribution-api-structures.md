---
description: Le service de distribution d’homologue Microsoft prend en charge les structures suivantes.
ms.assetid: 26badfe6-3a5a-4c2e-9ef1-534c2e8573d0
title: Structures de l’API de distribution d’homologue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc9fbf86c242406aa86b7dd30497ba4c5085488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527478"
---
# <a name="peer-distribution-api-structures"></a><span data-ttu-id="21ea4-103">Structures de l’API de distribution d’homologue</span><span class="sxs-lookup"><span data-stu-id="21ea4-103">Peer Distribution API Structures</span></span>

<span data-ttu-id="21ea4-104">Le service de distribution d’homologue Microsoft prend en charge les structures suivantes.</span><span class="sxs-lookup"><span data-stu-id="21ea4-104">The Microsoft Peer Distribution service supports the following structures.</span></span>



| <span data-ttu-id="21ea4-105">Structure</span><span class="sxs-lookup"><span data-stu-id="21ea4-105">Structure</span></span>                                                              | <span data-ttu-id="21ea4-106">Description</span><span class="sxs-lookup"><span data-stu-id="21ea4-106">Description</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21ea4-107">**\_informations de \_ base du client PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="21ea4-107">**PEERDIST\_CLIENT\_BASIC\_INFO**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_client_basic_info)    | <span data-ttu-id="21ea4-108">Indique si de nombreux clients téléchargent simultanément le même contenu.</span><span class="sxs-lookup"><span data-stu-id="21ea4-108">Indicates whether or not there are many clients simultaneously downloading the same content.</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="21ea4-109">**\_étiquette de contenu PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="21ea4-109">**PEERDIST\_CONTENT\_TAG**</span></span>](/windows/win32/api/peerdist/ns-peerdist-peerdist_content_tag)                 | <span data-ttu-id="21ea4-110">Contient une balise fournie par le client qui est une valeur d’entrée pour [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent).</span><span class="sxs-lookup"><span data-stu-id="21ea4-110">Contains a client supplied tag which is an input value for [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent).</span></span> <span data-ttu-id="21ea4-111">La balise est associée au segment de contenu et est utilisée dans les API de gestion de contenu, comme [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent).</span><span class="sxs-lookup"><span data-stu-id="21ea4-111">The tag is associated with the content segment and is used in content management APIs, like [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent).</span></span> |
| [<span data-ttu-id="21ea4-112">**\_options de publication PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="21ea4-112">**PEERDIST\_PUBLICATION\_OPTIONS**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_publication_options) | <span data-ttu-id="21ea4-113">Contient les options de publication, y compris les informations de version de l’API et les indicateurs d’option possibles.</span><span class="sxs-lookup"><span data-stu-id="21ea4-113">Contains publication options, including the API version information and possible option flags.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="21ea4-114">**OPTIONS de récupération d’HOMOLOGUe \_ \_**</span><span class="sxs-lookup"><span data-stu-id="21ea4-114">**PEER\_RETRIEVAL\_OPTIONS**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_retrieval_options)         | <span data-ttu-id="21ea4-115">Contient la version des informations de contenu à récupérer.</span><span class="sxs-lookup"><span data-stu-id="21ea4-115">Contains version of the content information to retrieve.</span></span>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="21ea4-116">**\_informations sur l’État PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="21ea4-116">**PEERDIST\_STATUS\_INFO**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_status_info)                 | <span data-ttu-id="21ea4-117">Contient des informations sur l’état actuel et les fonctionnalités du service BranchCache sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="21ea4-117">Contains information about the current status and capabilities of the BranchCache service on the local computer.</span></span>                                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="21ea4-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="21ea4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21ea4-119">Informations de référence sur l’API de distribution d’homologue</span><span class="sxs-lookup"><span data-stu-id="21ea4-119">Peer Distribution API Reference</span></span>](peer-distribution-api-reference.md)
</dt> </dl>

 

 



