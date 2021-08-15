---
description: Contient l’exemple de zone de description pour un fichier MP4 ou 3GP.
ms.assetid: ea157988-bd15-465c-bd6a-6d33cc1a0323
title: Attribut MF_MT_MPEG4_SAMPLE_DESCRIPTION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c59827fa5d2ba6c6621c7e251cf319478fd621d24639e105dcd44863495b364
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741791"
---
# <a name="mf_mt_mpeg4_sample_description-attribute"></a>\_Attribut de \_ Description du MPEG4 MF MT \_ \_

Contient l’exemple de zone de description pour un fichier MP4 ou 3GP.

## <a name="data-type"></a>Type de données

**POIDS\[\]**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Pour définir cet attribut, appelez [**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>S’applique à

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Remarques

La zone Description de l’exemple décrit l’encodage utilisé pour un flux dans le fichier.

La source de fichier MPEG-4 définit cet attribut sur le type de média pour chaque flux. La valeur de l’attribut correspond aux données brutes de la zone de description de l’exemple. Si la source du fichier MPEG-4 peut analyser l’exemple de description, elle ajoute également les détails du format au type de média. Dans le cas contraire, l’application ou le décodeur doit analyser l’exemple de description de l' \_ attribut de description du MPEG4 MF MT \_ \_ \_ .

Lors de la définition de cet attribut sur le récepteur MPEG-4 par le biais de la méthode [**IMFMediaTypeHandler :: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) , les données de l’exemple de description de l’exemple d’attribut \_ MPEG4 MT MT \_ \_ \_ ne doivent pas changer après l’envoi d’un ou de plusieurs échantillons au récepteur de l’interface [**IMFStreamSink ::P rocesssample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) du flux correspondant.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




