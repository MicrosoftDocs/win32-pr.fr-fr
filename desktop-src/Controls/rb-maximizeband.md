---
title: Message RB_MAXIMIZEBAND (commctrl. h)
description: Redimensionne une bande dans un contrôle rebar en sa taille idéale ou la plus grande taille.
ms.assetid: 79fff6d0-01f2-4308-b916-38dc06dad894
keywords:
- RB_MAXIMIZEBAND les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_MAXIMIZEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708a8fae7c0dd8e72eea8e5acefe43ab50054592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843925"
---
# <a name="rb_maximizeband-message"></a>\_Message MAXIMIZEBAND RB

Redimensionne une bande dans un contrôle rebar en sa taille idéale ou la plus grande taille.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la bande à agrandir.

</dd> <dt>

*lParam* 
</dt> <dd>

Indique si la largeur idéale de la bande doit être utilisée lorsque la bande est agrandie. Si cette valeur est différente de zéro, la largeur idéale sera utilisée. Si cette valeur est égale à zéro, la bande sera aussi grande que possible.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_SETBANDINFO RB**](rb-setbandinfo.md)
</dt> </dl>

 

 





