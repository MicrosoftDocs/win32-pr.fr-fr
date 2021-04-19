---
description: Décrit le contenu d’un flux élémentaire au sein d’un flux de transport MPEG-2. Cette énumération est utilisée dans l’interface IMPEG2PIDMap, qui est implémentée sur les broches de sortie du démultiplexeur MPEG-2.
ms.assetid: 989ad56b-b5af-4811-889e-c79fcd3f7f01
title: Énumération MEDIA_SAMPLE_CONTENT (Bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SAMPLE_CONTENT
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 9065f2af948ff28d181b24842673b086882837bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528040"
---
# <a name="media_sample_content-enumeration"></a><span data-ttu-id="b196b-104">Énumération du contenu de l’exemple de média \_ \_</span><span class="sxs-lookup"><span data-stu-id="b196b-104">MEDIA\_SAMPLE\_CONTENT enumeration</span></span>

<span data-ttu-id="b196b-105">Décrit le contenu d’un flux élémentaire au sein d’un flux de transport MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="b196b-105">Describes the contents of an elementary stream within an MPEG-2 transport stream.</span></span> <span data-ttu-id="b196b-106">Cette énumération est utilisée dans l’interface [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) , qui est implémentée sur les broches de sortie du [démultiplexeur MPEG-2](mpeg-2-demultiplexer.md).</span><span class="sxs-lookup"><span data-stu-id="b196b-106">This enumeration is used in the [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) interface, which is implemented on the output pins of the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b196b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b196b-107">Syntax</span></span>


```C++
typedef enum  { 
  MEDIA_TRANSPORT_PACKET,
  MEDIA_ELEMENTARY_STREAM,
  MEDIA_MPEG2_PSI,
  MEDIA_TRANSPORT_PAYLOAD
} MEDIA_SAMPLE_CONTENT;
```



## <a name="constants"></a><span data-ttu-id="b196b-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="b196b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b196b-109"><span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**\_paquet de transport multimédia \_**</span><span class="sxs-lookup"><span data-stu-id="b196b-109"><span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**MEDIA\_TRANSPORT\_PACKET**</span></span>
</dt> <dd>

<span data-ttu-id="b196b-110">Spécifie un paquet de flux de transport complet à passer sans traitement.</span><span class="sxs-lookup"><span data-stu-id="b196b-110">Specifies a complete transport stream packet to be passed through without processing.</span></span>

</dd> <dt>

<span data-ttu-id="b196b-111"><span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**\_flux élémentaire du média \_**</span><span class="sxs-lookup"><span data-stu-id="b196b-111"><span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**MEDIA\_ELEMENTARY\_STREAM**</span></span>
</dt> <dd>

<span data-ttu-id="b196b-112">Spécifie une charge utile audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="b196b-112">Specifies an audio or video PES payload.</span></span>

</dd> <dt>

<span data-ttu-id="b196b-113"><span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA \_ MPEG2 \_ psi**</span><span class="sxs-lookup"><span data-stu-id="b196b-113"><span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA\_MPEG2\_PSI**</span></span>
</dt> <dd>

<span data-ttu-id="b196b-114">Spécifie un flux de données PAT, VPM, CAT ou Private.</span><span class="sxs-lookup"><span data-stu-id="b196b-114">Specifies a PAT, PMT, CAT, or Private data stream.</span></span> <span data-ttu-id="b196b-115">Il s’agit de sections PSI complètes qui n’ont pas besoin d’être réassemblées.</span><span class="sxs-lookup"><span data-stu-id="b196b-115">These are complete PSI sections which do not need to be reassembled.</span></span>

</dd> <dt>

<span data-ttu-id="b196b-116"><span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**\_charge utile de transport multimédia \_**</span><span class="sxs-lookup"><span data-stu-id="b196b-116"><span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**MEDIA\_TRANSPORT\_PAYLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="b196b-117">Spécifie les charges utiles des paquets TS collectés, tels que les paquets PES.</span><span class="sxs-lookup"><span data-stu-id="b196b-117">Specifies gathered TS packet payloads, such as PES packets.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b196b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b196b-118">Requirements</span></span>



| <span data-ttu-id="b196b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b196b-119">Requirement</span></span> | <span data-ttu-id="b196b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b196b-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b196b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="b196b-121">Header</span></span><br/> | <dl> <span data-ttu-id="b196b-122"><dt>Bdatypes. h (inclure Bdaiface. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b196b-122"><dt>Bdatypes.h (include Bdaiface.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b196b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b196b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b196b-124">Types énumérés DirectShow</span><span class="sxs-lookup"><span data-stu-id="b196b-124">DirectShow Enumerated Types</span></span>](directshow-enumerated-types.md)
</dt> </dl>

 

 




