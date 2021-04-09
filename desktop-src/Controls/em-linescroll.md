---
title: Message EM_LINESCROLL (winuser. h)
description: Fait défiler le texte dans un contrôle d’édition multiligne.
ms.assetid: 5398082d-f1ef-4a3a-9e5a-83cf286adbf1
keywords:
- EM_LINESCROLL les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_LINESCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 646e225ef269ccddca2cdc29caf635d94c1671e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033055"
---
# <a name="em_linescroll-message"></a>\_Message LINESCROLL em

Fait défiler le texte dans un contrôle d’édition multiligne.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

**Contrôles d’édition :** Nombre de caractères à faire défiler horizontalement.

**Contrôles RichEdit :** Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Nombre de lignes à faire défiler verticalement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message est envoyé à un contrôle d’édition multiligne, la valeur de retour est **true**.

Si le message est envoyé à un contrôle d’édition sur une seule ligne, la valeur de retour est **false**.

## <a name="remarks"></a>Notes

Le contrôle ne défile pas verticalement après la dernière ligne de texte dans le contrôle d’édition. Si la ligne actuelle plus le nombre de lignes spécifié par le paramètre *lParam* dépasse le nombre total de lignes dans le contrôle d’édition, la valeur est ajustée de sorte que la dernière ligne du contrôle d’édition soit défilante en haut de la fenêtre Modifier-contrôle.

**Contrôles d’édition :** Le **message \_ LINESCROLL em** fait défiler le texte verticalement ou horizontalement dans un contrôle d’édition multiligne. Le **message \_ LINESCROLL em** peut être utilisé pour faire défiler horizontalement le dernier caractère d’une ligne.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Le **message \_ LINESCROLL em** fait défiler le texte verticalement dans un contrôle d’édition multiligne. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

 





