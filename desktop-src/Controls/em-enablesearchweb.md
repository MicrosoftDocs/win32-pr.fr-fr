---
title: Message EM_ENABLESEARCHWEB (CommCtrl. h)
description: Active ou désactive la fonctionnalité « Rechercher sur le Web » et l’entrée du menu contextuel.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- EM_ENABLESEARCHWEB les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_ENABLESEARCHWEB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdb2638476027f0a7fe2bb1a66a3a00a330e28c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942386"
---
# <a name="em_enablesearchweb-message"></a>\_Message ENABLESEARCHWEB em

Active ou désactive la fonctionnalité « Rechercher sur le Web » et l’entrée du menu contextuel.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

La valeur **true** indique que la fonctionnalité « Rechercher sur le Web » est activée, et la valeur **false** indique qu’elle est désactivée.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si vous désactivez « Rechercher sur le Web » à l’aide de ce message, le message [**em \_ SEARCHWEB**](em-searchweb.md) n’a aucun effet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, 1809 \[ uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2019 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_SEARCHWEB em**](em-searchweb.md)
</dt> </dl>

 

 





