---
description: Données de format supplémentaires pour un flux binaire dans un fichier ASF (Advanced Systems Format).
ms.assetid: fc5b9890-1508-498e-b2ce-ed4fa2052f9c
title: Attribut MF_MT_ARBITRARY_FORMAT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf98da23fbc4631ca67462dfc58f870abe73885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529185"
---
# <a name="mf_mt_arbitrary_format-attribute"></a>\_Attribut de \_ format arbitraire MT \_ MF

Données de format supplémentaires pour un flux binaire dans un fichier ASF (Advanced Systems Format).

## <a name="data-type"></a>Type de données

**POIDS\[\]**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Pour définir cet attribut, appelez [**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Notes

Les applications peuvent utiliser des flux binaires pour contenir des types de données personnalisés. La source de média ASF traite la valeur de cet attribut comme un objet blob opaque. Le membre **formatType** de la structure d' [**\_ \_ en-tête arbitraire MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) définit la disposition des données de format.

Cette structure correspond au champ de données de format des données spécifiques au type dans l’objet de propriétés de flux, dans les fichiers où le type de flux est un **\_ \_ média binaire ASF**. Pour plus d’informations, consultez la spécification ASF.

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
</dt> <dt>

[\_ \_ \_ en-tête arbitraire MT](mf-mt-arbitrary-header.md)
</dt> </dl>

 

 




