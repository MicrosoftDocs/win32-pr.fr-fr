---
description: Contient le lien symbolique pour une transformation de Media Foundation matérielle (MFT).
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: Attribut MFT_ENUM_HARDWARE_URL_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7119ea4bde7900087f706cb6fbc77c845721debab54dfa05b48f5c0094b1e29e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722583"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a>\_Attribut d' \_ \_ attribut d’URL matériel de l’énumération MFT \_

Contient le lien symbolique pour une transformation de Media Foundation matérielle (MFT).

## <a name="data-type"></a>Type de données

**WCHAR\***

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Remarques

Cet attribut est pris en charge par les MFTs basés sur le matériel. La valeur de l’attribut est le lien symbolique pour le pilote de périphérique. Cet attribut est également défini sur les pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) alloués par la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , lorsque ces pointeurs représentent des MFTS basées sur le matériel.

Le lien symbolique doit être considéré comme une chaîne opaque. Pour obtenir le nom complet d’un appareil, interrogez l’attribut [ \_ \_ nom convivial](mft-friendly-name-attribute.md) de la MFT.

Cet attribut n’est pas défini pour le MFTs logiciel.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Matériel MFTs](hardware-mfts.md)
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 




