---
title: Message HDM_GETUNICODEFORMAT (commctrl. h)
description: Obtient l’indicateur de format de caractère Unicode pour le contrôle. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ GetUnicodeFormat.
ms.assetid: 2b36265a-023c-4083-a755-769461f3804b
keywords:
- HDM_GETUNICODEFORMAT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- HDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce625cc9d4c0ede0c4ce9b54dc852025b22d4870
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006281"
---
# <a name="hdm_getunicodeformat-message"></a>\_Message HDM GETUNICODEFORMAT

Obtient l’indicateur de format de caractère Unicode pour le contrôle. Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’indicateur de format Unicode pour le contrôle. Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode. Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.

## <a name="remarks"></a>Notes

Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**HDM \_ SETUNICODEFORMAT**](hdm-setunicodeformat.md)
</dt> </dl>

 

 





