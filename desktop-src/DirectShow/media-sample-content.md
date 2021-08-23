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
ms.openlocfilehash: 1dead22b2c8ea3cf7da665e01a4b36554b8282922a1d2b2a12d59f429f2acac4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684989"
---
# <a name="media_sample_content-enumeration"></a>Énumération du contenu de l’exemple de média \_ \_

Décrit le contenu d’un flux élémentaire au sein d’un flux de transport MPEG-2. Cette énumération est utilisée dans l’interface [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) , qui est implémentée sur les broches de sortie du [démultiplexeur MPEG-2](mpeg-2-demultiplexer.md).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  MEDIA_TRANSPORT_PACKET,
  MEDIA_ELEMENTARY_STREAM,
  MEDIA_MPEG2_PSI,
  MEDIA_TRANSPORT_PAYLOAD
} MEDIA_SAMPLE_CONTENT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**\_paquet de transport multimédia \_**
</dt> <dd>

Spécifie un paquet de flux de transport complet à passer sans traitement.

</dd> <dt>

<span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**\_flux élémentaire du média \_**
</dt> <dd>

Spécifie une charge utile audio ou vidéo.

</dd> <dt>

<span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA \_ MPEG2 \_ psi**
</dt> <dd>

Spécifie un flux de données PAT, VPM, CAT ou Private. Il s’agit de sections PSI complètes qui n’ont pas besoin d’être réassemblées.

</dd> <dt>

<span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**\_charge utile de transport multimédia \_**
</dt> <dd>

Spécifie les charges utiles des paquets TS collectés, tels que les paquets PES.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Bdatypes. h (inclure Bdaiface. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DirectShow Types énumérés](directshow-enumerated-types.md)
</dt> </dl>

 

 




