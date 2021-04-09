---
description: Pour un type de média qui décrit un flux de transport MPEG-2 (TS), spécifie si les paquets de transport contiennent des en-têtes de paquets de contenu.
ms.assetid: 527B965D-4330-4DCB-B6DA-32D6BCDF5515
title: Attribut MF_MT_MPEG2_CONTENT_PACKET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acb297081a150ab3aa5b842be9b5792d849e2457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866573"
---
# <a name="mf_mt_mpeg2_content_packet-attribute"></a><span data-ttu-id="740a7-103">\_Attribut de \_ \_ paquet de contenu MPEG2 MT MT \_</span><span class="sxs-lookup"><span data-stu-id="740a7-103">MF\_MT\_MPEG2\_CONTENT\_PACKET attribute</span></span>

<span data-ttu-id="740a7-104">Pour un type de média qui décrit un flux de transport MPEG-2 (TS), spécifie si les paquets de transport contiennent des en-têtes de paquets de contenu.</span><span class="sxs-lookup"><span data-stu-id="740a7-104">For a media type that describes an MPEG-2 transport stream (TS), specifies whether the transport packets contain Content Packet headers.</span></span>

## <a name="data-type"></a><span data-ttu-id="740a7-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="740a7-105">Data type</span></span>

<span data-ttu-id="740a7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="740a7-106">**UINT32**</span></span>



| <span data-ttu-id="740a7-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="740a7-107">Value</span></span>                                                                                                | <span data-ttu-id="740a7-108">Signification</span><span class="sxs-lookup"><span data-stu-id="740a7-108">Meaning</span></span>                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="740a7-109"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="740a7-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="740a7-110">Aucun en-tête de paquet de contenu n’est ajouté.</span><span class="sxs-lookup"><span data-stu-id="740a7-110">No Content Packet headers are added.</span></span><br/>                                                                                                                                                                    |
| <span id="1"></span><dl> <span data-ttu-id="740a7-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="740a7-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="740a7-112">À des intervalles de 200 à 1 000 millisecondes, un en-tête de paquet de contenu de 14 octets est ajouté au début du paquet de transport, tel que défini par l’Association de la norme ARIB (Radio Industries and Business).</span><span class="sxs-lookup"><span data-stu-id="740a7-112">At 200–1000 millisecond intervals, a 14-byte Content Packet header is added to the beginning of the transport packet, as defined by the Association of Radio Industries and Businesses (ARIB) standard.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="740a7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="740a7-113">Requirements</span></span>



| <span data-ttu-id="740a7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="740a7-114">Requirement</span></span> | <span data-ttu-id="740a7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="740a7-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="740a7-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="740a7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="740a7-117">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="740a7-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="740a7-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="740a7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="740a7-119">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="740a7-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="740a7-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="740a7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="740a7-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="740a7-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="740a7-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="740a7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="740a7-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="740a7-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




