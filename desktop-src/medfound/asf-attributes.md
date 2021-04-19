---
description: Attributs ASF
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: Attributs ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ccf09542c8b96cc262cbe029111d3cb74e5b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517216"
---
# <a name="asf-attributes"></a><span data-ttu-id="509af-103">Attributs ASF</span><span class="sxs-lookup"><span data-stu-id="509af-103">ASF Attributes</span></span>

### <a name="profile-attributes"></a><span data-ttu-id="509af-104">Attributs de profil</span><span class="sxs-lookup"><span data-stu-id="509af-104">Profile Attributes</span></span>

<span data-ttu-id="509af-105">Les attributs suivants s’appliquent aux profils ASF.</span><span class="sxs-lookup"><span data-stu-id="509af-105">The following attributes apply to ASF profiles.</span></span>



| <span data-ttu-id="509af-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="509af-106">Attribute</span></span>                                                                      | <span data-ttu-id="509af-107">Description</span><span class="sxs-lookup"><span data-stu-id="509af-107">Description</span></span>                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="509af-108">**\_ASFPROFILE \_ MaxPacketSize**</span><span class="sxs-lookup"><span data-stu-id="509af-108">**MF\_ASFPROFILE\_MAXPACKETSIZE**</span></span>](mf-asfprofile-maxpacketsize-attribute.md) | <span data-ttu-id="509af-109">Spécifie la taille maximale des paquets pour un fichier ASF, en octets.</span><span class="sxs-lookup"><span data-stu-id="509af-109">Specifies the maximum packet size for an ASF file, in bytes.</span></span> |
| [<span data-ttu-id="509af-110">**\_MINPACKETSIZE ASFPROFILE \_ MF**</span><span class="sxs-lookup"><span data-stu-id="509af-110">**MF\_ASFPROFILE\_MINPACKETSIZE**</span></span>](mf-asfprofile-minpacketsize-attribute.md) | <span data-ttu-id="509af-111">Spécifie la taille minimale des paquets pour un fichier ASF, en octets.</span><span class="sxs-lookup"><span data-stu-id="509af-111">Specifies the minimum packet size for an ASF file, in bytes.</span></span> |



 

### <a name="stream-configuration-attributes"></a><span data-ttu-id="509af-112">Attributs de configuration de flux</span><span class="sxs-lookup"><span data-stu-id="509af-112">Stream Configuration Attributes</span></span>

<span data-ttu-id="509af-113">Les attributs suivants s’appliquent à l’objet de configuration de flux ASF.</span><span class="sxs-lookup"><span data-stu-id="509af-113">The following attributes apply to the ASF stream configuration object.</span></span>



| <span data-ttu-id="509af-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="509af-114">Attribute</span></span>                                                                              | <span data-ttu-id="509af-115">Description</span><span class="sxs-lookup"><span data-stu-id="509af-115">Description</span></span>                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="509af-116">**\_LEAKYBUCKET1 ASFSTREAMCONFIG \_ MF**</span><span class="sxs-lookup"><span data-stu-id="509af-116">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md) | <span data-ttu-id="509af-117">Définit les paramètres de « compartiment perdu » moyens pour l’encodage d’un fichier Windows Media.</span><span class="sxs-lookup"><span data-stu-id="509af-117">Sets the average "leaky bucket" parameters for encoding a Windows Media file.</span></span> |
| [<span data-ttu-id="509af-118">**\_LEAKYBUCKET2 ASFSTREAMCONFIG \_ MF**</span><span class="sxs-lookup"><span data-stu-id="509af-118">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md) | <span data-ttu-id="509af-119">Définit le pic des paramètres « compartiment perdu » pour l’encodage d’un fichier Windows Media.</span><span class="sxs-lookup"><span data-stu-id="509af-119">Sets the peak "leaky bucket" parameters for encoding a Windows Media file.</span></span>    |



 

### <a name="media-buffer-attributes"></a><span data-ttu-id="509af-120">Attributs du tampon de média</span><span class="sxs-lookup"><span data-stu-id="509af-120">Media Buffer Attributes</span></span>

<span data-ttu-id="509af-121">Les attributs suivants s’appliquent aux mémoires tampons de média pour les paquets ASF.</span><span class="sxs-lookup"><span data-stu-id="509af-121">The following attributes apply to media buffers for ASF packets.</span></span>



| <span data-ttu-id="509af-122">Attribut</span><span class="sxs-lookup"><span data-stu-id="509af-122">Attribute</span></span>                                                                          | <span data-ttu-id="509af-123">Description</span><span class="sxs-lookup"><span data-stu-id="509af-123">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="509af-124">**\_limite du paquet MFASFSPLITTER \_**</span><span class="sxs-lookup"><span data-stu-id="509af-124">**MFASFSPLITTER\_PACKET\_BOUNDARY**</span></span>](mfasfsplitter-packet-boundary-attribute.md) | <span data-ttu-id="509af-125">Spécifie si une mémoire tampon contient le début d’un paquet ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="509af-125">Specifies whether a buffer contains the start of an Advanced Systems Format (ASF) packet.</span></span> |



 

### <a name="presentation-descriptor-attributes"></a><span data-ttu-id="509af-126">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="509af-126">Presentation Descriptor Attributes</span></span>

<span data-ttu-id="509af-127">Pour obtenir la liste des attributs qui s’appliquent aux descripteurs de présentation ASF, consultez attributs du descripteur de [Présentation](presentation-descriptor-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="509af-127">For a list of attributes that apply to ASF presentation descriptors, see [Presentation Descriptor Attributes](presentation-descriptor-attributes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="509af-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="509af-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="509af-129">**IMFASFProfile**</span><span class="sxs-lookup"><span data-stu-id="509af-129">**IMFASFProfile**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
</dt> <dt>

[<span data-ttu-id="509af-130">**IMFASFStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="509af-130">**IMFASFStreamConfig**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
</dt> <dt>

[<span data-ttu-id="509af-131">Attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="509af-131">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



