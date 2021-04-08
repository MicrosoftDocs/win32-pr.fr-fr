---
title: Message EM_LINEINDEX (winuser. h)
description: Obtient l’index de caractère du premier caractère d’une ligne spécifiée dans un contrôle d’édition multiligne.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- EM_LINEINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_LINEINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611d4ff892f95287c45166ae55ff2389f454512c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941961"
---
# <a name="em_lineindex-message-winuserh"></a>Message EM_LINEINDEX (winuser. h)

Obtient l’index de caractère du premier caractère d’une ligne spécifiée dans un contrôle d’édition multiligne. Un index de caractère est l’index de base zéro du caractère à partir du début du contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Numéro de ligne de base zéro. La valeur-1 spécifie le numéro de la ligne active (la ligne qui contient le signe insertion).

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’index de caractère de la ligne spécifiée dans le paramètre *wParam* , ou a la valeur-1 si le numéro de ligne spécifié est supérieur au nombre de lignes dans le contrôle d’édition.

## <a name="remarks"></a>Notes

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_LINEFROMCHAR em**](em-linefromchar.md)
</dt> </dl>

 

 





