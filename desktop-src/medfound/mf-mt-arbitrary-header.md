---
description: Données spécifiques au type d’un flux binaire dans un fichier ASF (Advanced Systems Format).
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: Attribut MF_MT_ARBITRARY_HEADER (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d824aad4f76947786f991807d2f7b301703e3e356d2d1cfb416aa634d49f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826519"
---
# <a name="mf_mt_arbitrary_header-attribute"></a>\_Attribut d' \_ \_ en-tête arbitraire MT

Données spécifiques au type d’un flux binaire dans un fichier ASF (Advanced Systems Format).

## <a name="data-type"></a>Type de données

**[**MT \_ \_En-tête arbitraire**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** stocké en tant qu' **octet \[ \]**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Pour définir cet attribut, appelez [**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Remarques

Les fichiers ASF peuvent contenir des flux de données binaires. L' \_ \_ \_ attribut d’en-tête arbitraire MT arbitraire dans le type de média contient une structure d' [**\_ \_ en-tête MT arbitraire**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) qui décrit le flux.

En plus de l' \_ attribut d' \_ \_ en-tête arbitraire MT, le type de média pour un flux binaire ASF contient les attributs suivants :



| Attribut                                                 | Description                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [**\_type de \_ majeurese MF MT \_**](mf-mt-major-type-attribute.md) | La valeur de l’attribut est **MFMediaType \_ binaire**. |
| [\_ \_ format arbitraire MT \_](mf-mt-arbitrary-format.md)   | Contient des données de format supplémentaires.                       |



 

> [!Note]  
> dans le kit de développement logiciel (SDK) Windows Media Format, les flux binaires sont appelés des flux *arbitraires* ou des *flux de données arbitraires*.

 

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




