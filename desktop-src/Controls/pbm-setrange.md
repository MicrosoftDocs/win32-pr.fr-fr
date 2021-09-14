---
title: Message PBM_SETRANGE (commctrl. h)
description: Définit les valeurs minimale et maximale d’une barre de progression et redessine la barre pour refléter la nouvelle plage.
ms.assetid: 251eb8c5-bedc-4e2c-90c2-e1626cb00420
keywords:
- PBM_SETRANGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e588170c80378082eab7e419e9425e716b8caf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117694"
---
# <a name="pbm_setrange-message"></a>\_Message PBM

Définit les valeurs minimale et maximale d’une barre de progression et redessine la barre pour refléter la nouvelle plage.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la valeur de plage minimale et [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la valeur de plage maximale. La valeur de plage minimale ne doit pas être négative. Par défaut, la valeur minimale est zéro. La valeur de plage maximale doit être supérieure à la valeur de plage minimale. Par défaut, la valeur de plage maximale est 100.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne les valeurs de la plage précédente en cas de réussite, ou zéro dans le cas contraire. [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la valeur minimale précédente et [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la valeur maximale précédente.

## <a name="remarks"></a>Notes

Si vous ne définissez pas les valeurs de plage, le système définit la valeur minimale sur 0 et la valeur maximale sur 100. Étant donné que ce message exprime la plage en tant qu’entier non signé 16 bits, il peut s’étendre de 0 à 65 535. La valeur minimale de la plage peut être comprise entre 0 et 65 535. De même, la valeur maximale peut être comprise entre 0 et 65 535.

Pour définir une plage plus grande, appelez [**PBM \_ SETRANGE32**](pbm-setrange32.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETRANGE PBM**](pbm-getrange.md)
</dt> <dt>

[**\_SETRANGE32 PBM**](pbm-setrange32.md)
</dt> </dl>

 

