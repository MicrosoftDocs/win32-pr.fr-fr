---
title: Message UDM_SETUNICODEFORMAT (commctrl. h)
description: 'UDM_SETUNICODEFORMAT message : définit l’indicateur de format de caractère Unicode pour le contrôle. Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.'
ms.assetid: abe882db-bf32-40b0-a1c0-3e89cdc93fe7
keywords:
- UDM_SETUNICODEFORMAT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- UDM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09eeb63d5c06a5e64c354c950cd84fc451568d36
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115414"
---
# <a name="udm_setunicodeformat-message"></a>\_Message SETUNICODEFORMAT UDM

Définit l’indicateur de format de caractère Unicode pour le contrôle. Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Détermine le jeu de caractères utilisé par le contrôle. Si cette valeur est **true**, le contrôle utilise des caractères Unicode. Si cette valeur est **false**, le contrôle utilise des caractères ANSI.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’indicateur de format Unicode précédent pour le contrôle.

## <a name="remarks"></a>Notes

Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETUNICODEFORMAT UDM**](udm-getunicodeformat.md)
</dt> </dl>

 

 





