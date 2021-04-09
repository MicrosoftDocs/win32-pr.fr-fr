---
title: Message EM_SCROLL (winuser. h)
description: Fait défiler le texte verticalement dans un contrôle d’édition multiligne. Ce message revient à envoyer un message WM \_ VSCROLL au contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 616b5ac2-d92f-4fc5-9a9e-2c7527fb0d97
keywords:
- EM_SCROLL les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09eb185fb14ef866ab0e7ea8c8064445193347d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106267"
---
# <a name="em_scroll-message"></a>\_Message de défilement em

Fait défiler le texte verticalement dans un contrôle d’édition multiligne. Ce message revient à envoyer un message [**WM \_ VSCROLL**](wm-vscroll.md) au contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Action que la barre de défilement doit prendre. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                   | Signification                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> </dl> | Fait défiler d’une ligne vers le bas.<br/> |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**\_gamme SB**</dt> </dl>       | Fait défiler d’une ligne vers le haut.<br/>   |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PG.**</dt> </dl> | Fait défiler d’une page vers le bas.<br/> |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PG PRÉC**</dt> </dl>       | Fait défiler d’une page vers le haut.<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message est réussi, le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de la valeur de retour est **true** et le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est le nombre de lignes que la commande défile. Le nombre retourné peut ne pas être le même que le nombre réel de lignes défilantes si le défilement se déplace au début ou à la fin du texte. Si le paramètre *wParam* spécifie une valeur non valide, la valeur de retour est **false**.

## <a name="remarks"></a>Notes

Pour faire défiler jusqu’à la position d’un caractère ou d’une ligne spécifique, utilisez le message [**em \_ LINESCROLL**](em-linescroll.md) . Pour faire défiler le signe insertion dans la vue, utilisez le message [**em \_ SCROLLCARET**](em-scrollcaret.md) .

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

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

[**\_LINESCROLL em**](em-linescroll.md)
</dt> <dt>

[**\_SCROLLCARET em**](em-scrollcaret.md)
</dt> <dt>

[**\_VSCROLL WM**](wm-vscroll.md)
</dt> </dl>

 

