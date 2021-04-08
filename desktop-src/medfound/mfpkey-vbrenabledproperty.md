---
description: Spécifie si l’encodeur utilise l’encodage VBR (variable-bit-rate).
ms.assetid: e6826802-99b7-4a38-9b58-8a9cb8b753fb
title: MFPKEY_VBRENABLED, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9061abcc6ac7d7338b63eb5a7cd1a13ad22bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864129"
---
# <a name="mfpkey_vbrenabled-property"></a>MFPKEY \_ propriété VBRENABLED

Spécifie si l’encodeur utilise l’encodage VBR (variable-bit-rate). Lecture-écriture.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

**g \_ wszWMVCVBREnabled**, **g \_ wszWMCPAudioVBRSupported**

## <a name="data-type"></a>Type de données

**VT \_ bool**

## <a name="default-value"></a>Valeur par défaut

**VARIANTE \_ false**

## <a name="remarks"></a>Notes

Cette valeur doit être définie sur **Variant \_ true** pour l’une des autres propriétés VBR à utiliser par le codec.

Une fois que vous avez défini cette valeur sur **Variant \_ true** sur l’encodeur audio, les types de sortie récupérés à l’aide de la méthode [**IMediaObject :: GETOUTPUTTYPE**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) sont des types VBR.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MFPKEY de \_ contrainte \_ énumérée \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[**MFPKEY \_ \_ VBRQUALITY souhaité**](mfpkey-desired-vbrqualityproperty.md)
</dt> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
