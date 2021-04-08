---
description: Données spécifiques au type d’un flux binaire dans un fichier ASF (Advanced Systems Format).
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: Attribut MF_MT_ARBITRARY_HEADER (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd559ede3506335378ae1d56bf5b886e1407946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034207"
---
# <a name="mf_mt_arbitrary_header-attribute"></a>\_Attribut d' \_ \_ en-tête arbitraire MT

Données spécifiques au type d’un flux binaire dans un fichier ASF (Advanced Systems Format).

## <a name="data-type"></a>Type de données

**[**MT \_ \_En-tête arbitraire**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** stocké en tant qu' **octet \[ \]**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Pour définir cet attribut, appelez [**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Notes

Les fichiers ASF peuvent contenir des flux de données binaires. L' \_ \_ \_ attribut d’en-tête arbitraire MT arbitraire dans le type de média contient une structure d' [**\_ \_ en-tête MT arbitraire**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) qui décrit le flux.

En plus de l' \_ attribut d' \_ \_ en-tête arbitraire MT, le type de média pour un flux binaire ASF contient les attributs suivants :



| Attribut                                                 | Description                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [**\_type de \_ majeurese MF MT \_**](mf-mt-major-type-attribute.md) | La valeur de l’attribut est **MFMediaType \_ binaire**. |
| [\_ \_ format arbitraire MT \_](mf-mt-arbitrary-format.md)   | Contient des données de format supplémentaires.                       |



 

> [!Note]  
> Dans le kit de développement logiciel (SDK) Windows Media format, les flux binaires sont appelés des *flux arbitraires* ou des *flux de données arbitraires*.

 

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




