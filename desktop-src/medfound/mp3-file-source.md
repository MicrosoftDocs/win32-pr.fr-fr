---
description: La source de fichier MP3 analyse les fichiers MP3.
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: Source du fichier MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c95e54319fb189fa3bcc366b554b4d6555b2f4a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479835"
---
# <a name="mp3-file-source"></a>Source du fichier MP3

La source de fichier MP3 analyse les fichiers MP3.

La source du fichier MP3 génère des mémoires tampons qui contiennent des images audio MPEG-1. Elle ne décode pas l’audio.

## <a name="file-extensions-and-mime-types"></a>Extensions de fichier et types MIME

La source du fichier MP3 est la source du média par défaut pour l’extension de nom de fichier suivante :

-   .mp3

Il s’agit également de la source du média par défaut pour les types MIME suivants.

-   audio/MPEG
-   audio/x-mp3
-   audio/x-MPEG

## <a name="media-types"></a>Types de médias

Le type de média proposé par la source du fichier MP3 contient les attributs suivants.



| Attribut                                                                                    | Description                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_type de \_ majeurese MF MT \_**](mf-mt-major-type-attribute.md)                                    | Égal à **MFMediaType \_ audio**.                                                                                                                   |
| [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)                                           | Égal à **MFAudioFormat \_ mp3** ou **MFAudioFormat \_ MPEG**.                                                                                        |
| [**\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde**](mf-mt-audio-avg-bytes-per-second-attribute.md) | Nombre moyen d’octets par seconde.                                                                                                                |
| [**\_alignement de \_ \_ bloc audio MF MT \_**](mf-mt-audio-block-alignment-attribute.md)             | Égal à 1.                                                                                                                                        |
| [**\_canaux de \_ \_ numéros audio MF MT \_**](mf-mt-audio-num-channels-attribute.md)                   | Nombre de canaux audio.                                                                                                                          |
| [**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**](mf-mt-audio-samples-per-second-attribute.md)      | Nombre d’échantillons audio par seconde.                                                                                                                |
| [**\_ \_ données utilisateur MF \_ MT**](mf-mt-user-data-attribute.md)                                      | Contient la partie d’une structure [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) qui apparaît après le membre **wfx** de la structure. |



 

## <a name="interfaces"></a>Interfaces

La source de fichier MP3 expose les interfaces suivantes via [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):

-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

En outre, il expose les interfaces suivantes par le biais de [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):




| GUID du service | Interface | 
|--------------|-----------|
| <strong>MF_METADATA_PROVIDER_SERVICE</strong> | <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a> | 
| <strong>MF_PROPERTY_HANDLER_SERVICE</strong> | <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a><blockquote>[!Note]<br />Consultez <a href="shell-metadata-providers.md">fournisseurs de métadonnées de Shell</a>.</blockquote><br /><br /> | 
| <strong>MF_RATE_CONTROL_SERVICE</strong> | <a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a> | 
| <strong>MF_RATE_CONTROL_SERVICE</strong> | <a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a> | 




 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                           |
| DLL<br/>                      | <dl> <dt>Mf.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Sources et récepteurs multimédias](media-sources-and-sinks.md)
</dt> <dt>

[Sources multimédias](media-sources.md)
</dt> <dt>

[Résolveur source](source-resolver.md)
</dt> <dt>

[Formats multimédias pris en charge dans Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
