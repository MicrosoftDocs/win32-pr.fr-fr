---
description: 'Contient l’URL du fichier IFO (informations sur le DVD) spécifié par le serveur HTTP dans l’en-tête HTTP, &\# 0034 ; Pragma : ifoFileURI.dlna.org&\# 0034 ;.'
ms.assetid: 007e0f4d-fb37-4dec-96a7-311df567eb04
title: Attribut MF_BYTESTREAM_IFO_FILE_URI (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c80e015b68272b073c442b4064c80a6787b811
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127314081"
---
# <a name="mf_bytestream_ifo_file_uri-attribute"></a>\_Attribut d' \_ \_ URI de fichier IFO BYTESTREAM MF \_

Contient l’URL du fichier IFO (informations sur le DVD) spécifié par le serveur HTTP dans l’en-tête HTTP, « Pragma : ifoFileURI.dlna.org ».

## <a name="data-type"></a>Type de données

**LPWSTR**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="applies-to"></a>S’applique à

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a>Notes

Le flux d’octets HTTP recherche la chaîne « ifoFileURI.dlna.org » dans l’en-tête HTTP. Si la chaîne est trouvée, elle est copiée dans cet attribut sur le flux d’octets.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                                        |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                                           |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de flux d’octets](byte-stream-attributes.md)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




