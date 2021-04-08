---
title: Type de confidentialité (Wininet. h)
description: Spécifie que les paramètres de confidentialité sont pour les cookies internes ou tiers.
ms.assetid: 7d0846d4-fd81-4af9-b7e6-05c4c1438770
topic_type:
- apiref
api_name:
- PRIVACY_TYPE_FIRST_PARTY
- PRIVACY_TYPE_THIRD_PARTY
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38583d5f0c5cee148353f98f5d2be2d4f1a50216
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844374"
---
# <a name="privacy-type"></a>Type de confidentialité

Spécifie que les paramètres de confidentialité sont pour les cookies internes ou tiers.

<dl> <dt>

<span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**TYPE de confidentialité \_ \_ premier \_ tiers**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Fait référence aux paramètres de confidentialité pour les cookies de premier tiers.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**TYPE de confidentialité \_ \_ tiers \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Fait référence aux paramètres de confidentialité pour les cookies tiers.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Les cookies sont catégorisés comme premier tiers et tiers. Un cookie interne est un cookie qui provient du domaine hôte. Si « https://www.blueyonderairlines.com » se trouve dans la barre d’adresses Microsoft Internet Explorer, « www.blueyonderairlines.com » est le domaine hôte. En visitant cette page, si un cookie est défini à partir d’un domaine autre que « www.blueyonderairlines.com », tel que « www.fourthcoffee.com », ce cookie est considéré comme un cookie tiers.

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wininet. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PrivacyGetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[**PrivacySetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

