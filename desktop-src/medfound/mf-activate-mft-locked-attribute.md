---
description: Spécifie si le chargeur de topologie doit modifier les types de médias sur une Media Foundation transformation (MFT). En général, les applications n’utilisent pas cet attribut.
ms.assetid: 96a99f35-f9db-407e-a4e3-7adc3caccb19
title: Attribut MF_ACTIVATE_MFT_LOCKED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445447af46e1ce1da25aaa075dd4490d1210c1d01b2e7717829d2672dc74701f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060909"
---
# <a name="mf_activate_mft_locked-attribute"></a>\_Attribut de \_ verrouillage MFT d’activation MF \_

Spécifie si le chargeur de topologie doit modifier les types de médias sur une Media Foundation transformation (MFT). En général, les applications n’utilisent pas cet attribut.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Remarques

Si la valeur de cet attribut est différente de zéro, le chargeur de topologie ne modifiera pas les types de média sur la MFT. Le chargeur de topologie définit cet attribut après le chargement de la topologie.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
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

 

 




