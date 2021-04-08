---
title: TBN_SAVE le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’une barre d’outils qu’une barre d’outils est en cours d’enregistrement. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 31622f5e-2e33-4a42-8c49-cc3028a6fa62
keywords:
- Contrôles Windows de code de notification TBN_SAVE
topic_type:
- apiref
api_name:
- TBN_SAVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81cd28cb9d5fa1804caa3fe0ca89823305725ddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743804"
---
# <a name="tbn_save-notification-code"></a>TBN le \_ Code de notification d’enregistrement

Avertit la fenêtre parente d’une barre d’outils qu’une barre d’outils est en cours d’enregistrement. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_SAVE 

    lpnmtb = (LPNMTBSAVE) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

L’application recevra ce code de notification une fois au début du processus d’enregistrement et une fois pour chaque bouton. Ce code de notification vous donne la possibilité d’ajouter vos propres informations à celles enregistrées par l’interpréteur de commandes. Si vous ne souhaitez pas ajouter d’informations, ignorez le code de notification. Pour plus d’informations sur la gestion de TBN, consultez Personnalisation de la [barre d’outils](toolbar-controls-overview.md) \_ .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_restauration TBN](tbn-restore.md)
</dt> </dl>

 

 





