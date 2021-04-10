---
description: Spécifie si le chargeur de topologie doit modifier les types de médias sur une Media Foundation transformation (MFT). En général, les applications n’utilisent pas cet attribut.
ms.assetid: 96a99f35-f9db-407e-a4e3-7adc3caccb19
title: Attribut MF_ACTIVATE_MFT_LOCKED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4d6dcb6cb60f760d87761a18b2b83545937878c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114610"
---
# <a name="mf_activate_mft_locked-attribute"></a>\_Attribut de \_ verrouillage MFT d’activation MF \_

Spécifie si le chargeur de topologie doit modifier les types de médias sur une Media Foundation transformation (MFT). En général, les applications n’utilisent pas cet attribut.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Notes

Si la valeur de cet attribut est différente de zéro, le chargeur de topologie ne modifiera pas les types de média sur la MFT. Le chargeur de topologie définit cet attribut après le chargement de la topologie.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 




