---
title: Élément DownloadStatus (msfeeds. h)
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | Élément DownloadStatus (msfeeds. h)
ms.assetid: 08d9719a-390d-454a-935e-27812c0f3599
keywords:
- Élément DownloadStatus Windows Media Player
topic_type:
- apiref
api_name:
- DownloadStatus Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431da810a9591d891fca914a9ecb6d3146a651d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532673"
---
# <a name="downloadstatus-element"></a><span data-ttu-id="56800-105">Élément DownloadStatus</span><span class="sxs-lookup"><span data-stu-id="56800-105">DownloadStatus Element</span></span>

> [!Note]  
> <span data-ttu-id="56800-106">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="56800-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="56800-107">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="56800-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="56800-108">L’élément **DownloadStatus** spécifie une URL que le lecteur Windows Media affiche sous la forme d’un lien pour permettre aux utilisateurs d’afficher l’état du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="56800-108">The **DownloadStatus** element specifies a URL the Windows Media Player displays as a link to enable users to view download status.</span></span>

``` syntax
<DownloadStatus
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="56800-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="56800-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="56800-110"><span id="URL"></span><span id="url"></span>URL</span><span class="sxs-lookup"><span data-stu-id="56800-110"><span id="URL"></span><span id="url"></span>URL</span></span>
</dt> <dd>

<span data-ttu-id="56800-111">URL de la page Web que le magasin en ligne affiche pour afficher l’état du téléchargement à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56800-111">URL for the webpage that the online store displays to show download status to the user.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="56800-112">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="56800-112">Parent/Child Elements</span></span>



| <span data-ttu-id="56800-113">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="56800-113">Hierarchy</span></span>       | <span data-ttu-id="56800-114">Élément</span><span class="sxs-lookup"><span data-stu-id="56800-114">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="56800-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="56800-115">Parent elements</span></span> | <span data-ttu-id="56800-116">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="56800-116">**ServiceInfo**</span></span> |
| <span data-ttu-id="56800-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="56800-117">Child elements</span></span>  | <span data-ttu-id="56800-118">Aucune</span><span class="sxs-lookup"><span data-stu-id="56800-118">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="56800-119">Notes</span><span class="sxs-lookup"><span data-stu-id="56800-119">Remarks</span></span>

<span data-ttu-id="56800-120">Le lecteur Windows Media affiche un message aux utilisateurs lorsqu’un téléchargement est en cours.</span><span class="sxs-lookup"><span data-stu-id="56800-120">Windows Media Player displays a message to users when a download is in progress.</span></span> <span data-ttu-id="56800-121">Si les services actifs actuels définissent une URL d’état de téléchargement, l’utilisateur peut cliquer sur le texte du message.</span><span class="sxs-lookup"><span data-stu-id="56800-121">If the current active services defines a download status URL, the user can click the message text.</span></span> <span data-ttu-id="56800-122">Lorsque l’utilisateur clique sur le message, le lecteur accède à l’URL spécifiée par l’élément **DownloadStatus** afin que le magasin actif actuel puisse fournir des détails sur les téléchargements en cours.</span><span class="sxs-lookup"><span data-stu-id="56800-122">When the user clicks the message, the Player navigates to the URL specified by the **DownloadStatus** element so the current active store can provide details about downloads in progress.</span></span>

## <a name="requirements"></a><span data-ttu-id="56800-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56800-123">Requirements</span></span>



| <span data-ttu-id="56800-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56800-124">Requirement</span></span> | <span data-ttu-id="56800-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="56800-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="56800-126">Version</span><span class="sxs-lookup"><span data-stu-id="56800-126">Version</span></span><br/> | <span data-ttu-id="56800-127">Lecteur Windows Media 10 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="56800-127">Windows Media Player 10 or later</span></span><br/>                                          |
| <span data-ttu-id="56800-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="56800-128">Header</span></span><br/>  | <dl> <span data-ttu-id="56800-129"><dt>Msfeeds. h</dt></span><span class="sxs-lookup"><span data-stu-id="56800-129"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56800-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56800-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56800-131">**Exemple de document ServiceInfo pour une boutique en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="56800-131">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="56800-132">**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="56800-132">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="56800-133">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="56800-133">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





