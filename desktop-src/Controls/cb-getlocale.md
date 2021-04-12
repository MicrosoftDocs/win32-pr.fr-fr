---
title: Message CB_GETLOCALE (winuser. h)
description: Obtient les paramètres régionaux actuels de la zone de liste déroulante. Les paramètres régionaux sont utilisés pour déterminer l’ordre de tri correct du texte affiché pour les zones de liste déroulante avec le \_ style de tri CBS et le texte ajouté à l’aide du \_ message CB ADDSTRING.
ms.assetid: 57c77ce2-bad0-43f3-8325-f2a7227994ec
keywords:
- CB_GETLOCALE les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847d9f73e8bf0b1d533d0b79ba86d939bee0e9b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032851"
---
# <a name="cb_getlocale-message"></a>\_Message GETLOCALE CB

Obtient les paramètres régionaux actuels de la zone de liste déroulante. Les paramètres régionaux sont utilisés pour déterminer l’ordre de tri correct du texte affiché pour les zones de liste déroulante avec le style de [**\_ Tri CBS**](combo-box-styles.md) et le texte ajouté à l’aide du message [**CB \_ ADDSTRING**](cb-addstring.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour spécifie les paramètres régionaux actuels de la zone de liste déroulante. Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contient le code de pays/région et le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de langue.

## <a name="remarks"></a>Notes

L’identificateur de langue est constitué d’un identificateur de sous-langue et d’un identificateur de langue primaire. La macro [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) obtient l’identificateur de langue principal et la macro [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) obtient l’identificateur de sous-langue.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**$ \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ SETLOCALE**](cb-setlocale.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

