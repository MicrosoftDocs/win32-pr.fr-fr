---
title: Message SB_SETUNICODEFORMAT (commctrl. h)
description: Définit l’indicateur de format de caractère Unicode pour le contrôle. Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.
ms.assetid: 022e7138-c12f-4c59-82da-2ac6d276fa77
keywords:
- SB_SETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c5223f1e707747356c8869ad047a69f6e8d94a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513623"
---
# <a name="sb_setunicodeformat-message"></a>\_Message SB SETUNICODEFORMAT

Définit l’indicateur de format de caractère Unicode pour le contrôle. Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Détermine le jeu de caractères utilisé par le contrôle. Si cette valeur est **true**, le contrôle utilise des caractères Unicode. Si cette valeur est **false**, le contrôle utilise des caractères ANSI.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’indicateur de format Unicode précédent pour le contrôle.

## <a name="remarks"></a>Notes

Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETUNICODEFORMAT SB**](sb-getunicodeformat.md)
</dt> </dl>

 

 





