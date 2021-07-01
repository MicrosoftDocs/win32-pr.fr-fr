---
description: Types de média MPEG-2 Splitter
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Types de média MPEG-2 Splitter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4e025fafabdeb8c437cc1d1cd6fbb843cf63e3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119974"
---
# <a name="mpeg-2-splitter-media-types"></a>Types de média MPEG-2 Splitter

Le filtre de [séparateur MPEG-2](mpeg-2-splitter.md) prend actuellement en charge l’audio et la vidéo. Dolby AC-3 est pris en charge en tant que sous-flux, comme défini par DVD. Le filtre prend également en charge le format audio MPEG-2. Les types de médias varient selon que le séparateur MPEG-2 fournit des paquets PES ou des charges utiles PES.

### <a name="video"></a>Vidéo

Pour les vidéos MPEG-2, les types de médias sont les suivants.


|                | Sortie PES | Sortie de la charge utile
|------------------|------------------------------------------|--------------------------------|
| **Type principal**       | **\_PES MPEG2 de MediaType \_**                | **Vidéo de MEDIATYPE \_**           |
| **Sous-type**          | **\_Vidéo MEDIASUBTYPE MPEG2 \_**           | **\_Vidéo MEDIASUBTYPE MPEG2 \_** |
| **Type de format**      | **FORMAT \_ mpeg2video**                   | **FORMAT \_ mpeg2video**         |
| **Structure de format** | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | **MPEG2VIDEOINFO**             |



 

### <a name="ac-3-audio"></a>Audio AC-3

Pour le son AC-3, les types de médias sont les suivants.

| | Sortie PES | Sortie de la charge utile |
|------------------|--------------------------------------|------------------------------|
| **Type principal**       | **\_PES MPEG2 de MediaType \_**                | **Audio de MEDIATYPE \_**         |
| **Sous-type**          | **MEDIASUBTYPE \_ Dolby \_ AC3**             | **MEDIASUBTYPE \_ Dolby \_ AC3** |
| **Type de format**      | FORMAT \_ WaveFormatEx                 | **FORMAT \_ WaveFormatEx**     |
| **Structure de format** | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) | **WAVEFORMATEX**             |



 

Le membre **wFormatTag** de la structure **WAVEFORMATEX** pour AC-3 est **actuellement \_ \_ inconnu**, mais cela peut changer.

### <a name="mpeg-2-audio"></a>Audio MPEG-2

Pour le son MPEG-2, les types de médias sont les suivants.



|  | Sortie PES | Sortie de la charge utile |
|------------------|-------------------------------|--------------------------------|
| **Type principal**       | **\_PES MPEG2 de MediaType \_**     | **Audio de MEDIATYPE \_**           |
| **Sous-type**          | **MEDIASUBTYE \_ MPEG2 \_ audio** | **MEDIASUBTYPE \_ MPEG2 \_ audio** |
| **Type de format**      | **FORMAT \_ WaveFormatEx**      | **FORMAT \_ WaveFormatEx**       |
| **Structure de format** | **WAVEFORMATEX**              | **WAVEFORMATEX**               |



 

Le membre **wFormatTag** de la structure **WAVEFORMATEX** pour le format audio MPEG-2 est actuellement **\_ \_ inconnu**, mais cela peut changer.

Le séparateur MPEG-2 suppose que les flux D0 à DF sont utilisés pour le flux d’extension multicanaux, comme c’est le cas pour le DVD MPEG-2. Par conséquent, chaque fois que Stream C *x* est sélectionné, le séparateur transfère également les paquets pour le flux D *x* .

### <a name="lpcm-audio"></a>LPCM audio

Pour les LPCM audio, les types de médias sont les suivants.



|  | Sortie PES | Sortie de la charge utile |
|------------------|------------------------------------|------------------------------------|
| **Type principal**       | **\_PES MPEG2 de MediaType \_**          | **Audio de MEDIATYPE \_**               |
| **Sous-type**          | **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio** | **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio** |
| **Type de format**      | **FORMAT \_ WaveFormatEx**           | **FORMAT \_ WaveFormatEx**           |
| **Structure de format** | **WAVEFORMATEX**                   | **WAVEFORMATEX**                   |



 

Le membre **wFormatTag** de la structure **WAVEFORMATEX** pour l’audio LPCM est actuellement **\_ \_ inconnu**, mais cela peut changer.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de média MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 
