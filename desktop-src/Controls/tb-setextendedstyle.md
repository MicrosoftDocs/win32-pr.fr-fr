---
title: Message TB_SETEXTENDEDSTYLE (commctrl. h)
description: Définit les styles étendus pour un contrôle de barre d’outils.
ms.assetid: aec64bc7-74b4-4efc-9864-2c8a9fbd35c2
keywords:
- TB_SETEXTENDEDSTYLE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 600e5904637215eeb052c85ec0203c9b86c75ed6b179be643dc9a213156b3afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318879"
---
# <a name="tb_setextendedstyle-message"></a>TO \_ SETEXTENDEDSTYLE message

Définit les styles étendus pour un contrôle de barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Valeur spécifiant les nouveaux styles étendus. Ce paramètre peut être une combinaison de [styles étendus](toolbar-extended-styles.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une **valeur DWORD** qui représente les styles étendus précédents. Cette valeur peut être une combinaison de [styles étendus](toolbar-extended-styles.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TO \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md)
</dt> </dl>

 

 





