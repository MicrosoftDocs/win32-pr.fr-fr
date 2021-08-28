---
description: Types de média du démultiplexeur MPEG-2
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: Types de média du démultiplexeur MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef3c7006f13b07394da7d9dc92e9295beda816c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982602"
---
# <a name="mpeg-2-demultiplexer-media-types"></a>Types de média du démultiplexeur MPEG-2

Le filtre de [démultiplexage MPEG-2](mpeg-2-demultiplexer.md) reconnaît les types de média suivants.

### <a name="input-types"></a>Types d’entrée

Le type principal est toujours **un \_ flux de MediaType**. Le sous-type peut être l’un des éléments suivants.



| GUID                                             | Description                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_Sous-type \_ KSDATAFORMAT \_ transport MPEG2 BDA \_** | Flux de transport à partir d’un filtre d’appareil d’architecture de pilote de diffusion (BDA). Le démultiplexeur MPEG-2 traite ce sous-type de la même façon que le **\_ \_ transport MEDIASUBTYPE MPEG2**.                                |
| **\_Programme MEDIASUBTYPE MPEG2 \_**                 | Flux de programme                                                                                                                                                                                            |
| **\_Transport MEDIASUBTYPE MPEG2 \_**               | Flux de transport (TS), avec paquets de 188 octets                                                                                                                                                              |
| **\_Stride de \_ transport MEDIASUBTYPE MPEG2 \_**       | Flux de transport avec des paquets « strided ». Ce sous-type indique que les paquets TS peuvent être remplis avec des octets supplémentaires. Pour plus d’informations, [**consultez \_ \_ Stride transport Stride**](mpeg2-transport-stride.md). |



 

Pour les paquets de transport strided (**MEDIASUBTYPE \_ MPEG2 \_ transport \_ Stride**), chaque échantillon de support doit contenir un nombre entier de paquets de transport, comme décrit dans [**MPEG2 \_ transport \_ Stride**](mpeg2-transport-stride.md). Pour tous les autres types d’entrée, il n’existe aucune restriction sur les limites de l’échantillon. les paquets individuels peuvent s’étendre sur des limites d’échantillon.

### <a name="output-types"></a>Types de sortie

Le démultiplexeur MPEG-2 ne valide pas les types de sortie ; le filtre en aval est chargé d’analyser les données qu’il reçoit du démultiplexeur. Toutefois, les types suivants sont généralement acceptés par les filtres en aval comme sortie du démultiplexeur.

### <a name="mpeg-2-sections"></a>Sections MPEG-2




| Étiquette | Valeur |
|--------|-------|
| Type principal | <strong>MEDIATYPE_MPEG2_SECTIONS</strong> | 
| Subtype | Un des éléments suivants :<br /><ul><li><strong>MEDIASUBTYPE_ATSC_SI</strong>: informations sur le service ATSC.</li><li><strong>MEDIASUBTYPE_DVB_SI</strong>: informations sur le service DVB.</li><li><strong>MEDIASUBTYPE_ISDB_SI</strong>: informations sur le service de diffusion numérique de services intégrés (ISDB).</li><li><strong>MEDIASUBTYPE_MPEG2DATA</strong>: données de la section MPEG-2.</li></ul> | 
| Type de format | Aucun | 




 

### <a name="mpeg-2-video"></a>Vidéo MPEG-2



| Étiquette | Valeur |
|------------------|------------------------------------------|
| Type principal       | **Vidéo de MEDIATYPE \_**                     |
| Subtype          | **\_Vidéo MEDIASUBTYPE MPEG2 \_**           |
| Type de format      | **FORMAT \_ mpeg2video**                   |
| Structure de format | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a>Audio MPEG-2



| Étiquette | Valeur |
|------------------|--------------------------------------|
| Type principal       | **Audio de MEDIATYPE \_**                 |
| Subtype          | **MEDIASUBTYPE \_ MPEG2 \_ audio**       |
| Type de format      | **FORMAT \_ WaveFormatEx**             |
| Structure de format | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de média MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 
