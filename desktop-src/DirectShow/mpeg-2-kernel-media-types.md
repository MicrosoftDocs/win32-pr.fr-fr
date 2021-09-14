---
description: pour plusieurs guid de type de média MPEG-2, le DDK Windows définit des noms qui diffèrent de ceux utilisés dans DirectShow. le tableau suivant indique les noms de DirectShow (définis dans Ksuuids. h) et les noms en mode noyau correspondants (définis dans Ksmedia. h).
ms.assetid: ecf94552-5a0f-464c-9f9b-4861faa38d05
title: Types de média de noyau MPEG-2 (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b03e6d3cbc32c987110ceac98e6aeef6617d6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999006"
---
# <a name="mpeg-2-kernel-media-types"></a>Types de média de noyau MPEG-2

pour plusieurs guid de type de média MPEG-2, le DDK Windows définit des noms qui diffèrent de ceux utilisés dans DirectShow. le tableau suivant indique les noms de DirectShow (définis dans Ksuuids. h) et les noms en mode noyau correspondants (définis dans Ksmedia. h).



| Nom dans Ksuuids. h              | Nom dans Ksmedia. h                          |
|--------------------------------|--------------------------------------------|
| FORMAT \_ WaveFormatEx           | \_spécificateur KSDATAFORMAT \_ WAVEFORMATEX      |
| FORMAT \_ mpeg2video             | Vidéo sur le \_ spécificateur KSDATAFORMAT \_ MPEG2 \_      |
| MEDIASUBTYPE \_ ATSC \_ si         | KSDATAFORMAT \_ sous-type \_ ATSC \_ si            |
| MEDIASUBTYPE \_ Dolby \_ AC3       | KSDATAFORMAT \_ sous-type \_ AC3 \_ audio          |
| MEDIASUBTYPE \_ DVB \_ si          | KSDATAFORMAT \_ sous-type \_ DVB \_ si             |
| MEDIASUBTYPE \_ DVD \_ LPCM \_ audio | KSDATAFORMAT \_ sous-type \_ LPCM \_ audio         |
| MEDIASUBTYPE \_ MPEG2 \_ audio     | KSDATAFORMAT \_ sous-type \_ MPEG2 \_ audio        |
| \_Programme MEDIASUBTYPE MPEG2 \_   | \_ \_ Programme MPEG2 de type KSDATAFORMAT \_ statique \_ |
| \_Transport MEDIASUBTYPE MPEG2 \_ | \_ \_ Transport MPEG2 de type KSDATAFORMAT \_       |
| \_Vidéo MEDIASUBTYPE MPEG2 \_     | \_Vidéo MPEG2 de sous-type KSDATAFORMAT \_ \_        |
| SECTIONS de MEDIATYPE \_ MPEG2 \_     | KSDATAFORMAT, \_ type, \_ \_ sections MPEG2        |
| Audio de MEDIATYPE \_               | KSDATAFORMAT \_ type \_ audio                  |
| \_PES MPEG2 de MediaType \_          | KSDATAFORMAT \_ type \_ MPEG2 \_ PES             |
| Vidéo de MEDIATYPE \_               | \_vidéo de type KSDATAFORMAT \_                  |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de média MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 




