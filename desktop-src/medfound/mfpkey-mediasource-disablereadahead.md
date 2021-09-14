---
description: Active ou désactive la lecture anticipée dans une source de média.
ms.assetid: b2b8711f-ba63-4fba-bb88-8d254135eb21
title: MFPKEY_MediaSource_DisableReadAhead, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d06fe354431a24e15152268ba0ea6352e535c5e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236010"
---
# <a name="mfpkey_mediasource_disablereadahead-property"></a>MFPKEY \_ MediaSource \_ DisableReadAhead, propriété

Active ou désactive la lecture anticipée dans une source de média.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**VARIANT \_ booléen**

VT \_ bool

**boolVal**



## <a name="remarks"></a>Notes

Les applications peuvent utiliser cette propriété pour configurer des sources multimédias. Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

Si la valeur est **\_ true**, la source du média n’est pas lue dans le flux de données d’octets. Ce paramètre peut optimiser les performances si vous envisagez de lire une quantité limitée de données à partir de la source du média, par exemple pour obtenir une image miniature d’un fichier vidéo.

Pour une lecture audio/vidéo classique, cette propriété doit avoir la valeur **Variant \_ false**. La valeur par défaut **est \_ false**.

Toutes les sources de média ne prennent pas en charge cette propriété.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| Client<br/> | Windows 7<br/>                                                               |
| En-tête<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




