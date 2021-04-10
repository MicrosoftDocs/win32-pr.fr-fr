---
description: La source de fichier MP3 analyse les fichiers MP3.
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: Source du fichier MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2241e3b99d5a1918be8ff0182a9eca8939c12ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114382"
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



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID du service</th>
<th>Interface</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MF_METADATA_PROVIDER_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></td>
</tr>
<tr class="even">
<td><strong>MF_PROPERTY_HANDLER_SERVICE</strong></td>
<td><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a>
<blockquote>
[!Note]<br />
Consultez <a href="shell-metadata-providers.md">fournisseurs de métadonnées de Shell</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>MF_RATE_CONTROL_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a></td>
</tr>
<tr class="even">
<td><strong>MF_RATE_CONTROL_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                           |
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

 

 
