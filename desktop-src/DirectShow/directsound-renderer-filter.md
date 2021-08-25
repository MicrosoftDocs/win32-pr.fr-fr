---
description: Filtre de convertisseur DirectSound
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: Filtre de convertisseur DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b601c0e85169857cd628b3b3e55b5c00af8ea11
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481575"
---
# <a name="directsound-renderer-filter"></a>Filtre de convertisseur DirectSound

Ce filtre restitue l’audio à l’aide de DirectSound. Ce filtre est actuellement le convertisseur audio par défaut pour le son de forme d’onde.

Outre ses fonctionnalités de rendu de son de base, ce filtre peut traiter les appels d’API DirectSound. Utilisez les méthodes [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) pour définir et récupérer la fenêtre qui gérera la lecture audio. Le convertisseur audio DirectSound est le filtre de rendu audio par défaut pour DirectShow.




| | | Filtrer les interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a> | | Types de média de broche d’entrée | Type majeur : MEDIATYPE_AudioSubtypes :<br /><ul><li>MEDIASUBTYPE_PCM</li><li>MEDIASUBTYPE_IEEE_FLOAT</li><li>MEDIASUBTYPE_DOLBY_AC3_SPDIF</li><li>MEDIASUBTYPE_RAW_SPORT</li><li>MEDIASUBTYPE_SPDIF_TAG_241h</li><li>MEDIASUBTYPE_DRM_Audio</li></ul>Type de format : FORMAT_WaveFormatEx<br /> | | Interfaces pin d’entrée | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Types de média de broche de sortie | Non applicable. | | Interfaces de broche de sortie | Non applicable. | | CLSID du filtre | CLSID_DSoundRender | | CLSID de page de propriétés | CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties | | Fichier exécutable | quartz.dll | | <a href="merit.md">Mérite</a> | MERIT_PREFERRED | | <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_AudioRendererCategory | 




 

## <a name="remarks"></a>Remarques

Ce filtre sert de wrapper pour un périphérique audio. Pour énumérer les périphériques audio disponibles sur le système de l’utilisateur, utilisez l’interface [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) avec la catégorie de convertisseur audio (CLSID \_ AudioRendererCategory). Pour chaque périphérique audio, la catégorie de convertisseur audio contient deux instances de filtre. L’une d’entre elles correspond au convertisseur DirectSound, tandis que l’autre correspond au filtre de [convertisseur audio (WaveOut)](audio-renderer--waveout--filter.md) . L’instance DirectSound porte le nom convivial « DirectSound : *DeviceName*», où *DeviceName* est le nom de l’appareil. L’instance WaveOut a le nom convivial *DeviceName*.

La catégorie de convertisseur audio contient deux instances de filtre supplémentaires, nommées « appareil DirectSound par défaut » et « appareil WaveOut par défaut ». Celles-ci correspondent au périphérique audio par défaut, tel qu’il est choisi par l’utilisateur via le panneau de configuration. Elles sont en réalité mappées à l’une des paires décrites dans le paragraphe précédent. Par exemple, si le système a deux périphériques audio, l’appareil A et l’appareil B, la catégorie de convertisseur audio contient ce qui suit :

-   Appareil A
-   DirectSound : appareil A
-   Appareil B
-   DirectSound : appareil B
-   Appareil DirectSound par défaut
-   Appareil WaveOut par défaut

Si l’utilisateur A sélectionné l’appareil A comme périphérique par défaut, « appareil DirectSound par défaut » est équivalent à « DirectSound : Device A » et « appareil WaveOut par défaut » est équivalent à « périphérique A ». Si l’utilisateur sélectionne l’appareil B comme périphérique par défaut, ces mappages sont modifiés.

« Appareil DirectSound par défaut » est affecté d’un mérite de mérite \_ . Les autres ont des mérites à \_ ne \_ pas \_ utiliser. par conséquent, Intelligent Connecter choisira toujours l’appareil DirectSound par défaut.

Le filtre de convertisseur DirectSound prend en charge le son en 3D via les interfaces DirectSound **IDirectSound3DBuffer** et **IDirectSound3dListener** . Vous pouvez également interroger le filtre sur les versions actuelles de ces interfaces, **IDirectSound3DBuffer8** et **IDirectSound3dListener8**. Exécutez le graphique avant d’appeler des méthodes sur ces interfaces.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 




