---
description: Spécifie si le IMFTransform souhaite recevoir des notifications d’achèvement MEPolicySet.
title: MFT_POLICY_SET_AWARE (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2effa9eab2b0b126c2849d39ce7ffe3f62d81e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533624"
---
# <a name="mft_policy_set_aware-attribute"></a>Attribut de reconnaissance de l' \_ ensemble de stratégies MFT \_ \_

Si la valeur est différente de zéro, indique que le **IMFTransform** souhaite recevoir des notifications d’achèvement [MEPolicySet](./mepolicyset.md) .

## <a name="data-type"></a>Type de données

**UInt32** (traité comme **bool**)

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFInputTrustAuthority**](/windows/win32/api/mfidl/nn-mfidl-imfinputtrustauthority)

## <a name="remarks"></a>Notes

Cet attribute peut être utilisé par un Decrypter **IMFInputTrustAuthority** . Une implémentation d’un module de déchiffrement de contenu (CDM) peut inclure une implémentation de **IMFInputTrustAuthority**. L’objet **IMFInputTrustAuthority** est accessible via [IMFContentDecryptionModule :: CreateTrustedInput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).


La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Mise à jour 2020 de Windows 10 avril   <br/>                                        |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 
