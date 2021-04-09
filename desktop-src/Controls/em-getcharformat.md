---
title: Message EM_GETCHARFORMAT (RichEdit. h)
description: Détermine la mise en forme des caractères dans un contrôle RichEdit.
ms.assetid: 210b8719-5ed7-49f2-bd93-8a4e1efab1e8
keywords:
- EM_GETCHARFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd71db4d3a13f2acfe33c2843b0d9aad46c6f9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032944"
---
# <a name="em_getcharformat-message"></a>\_Message GETCHARFORMAT em

Détermine la mise en forme des caractères dans un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie la plage de texte à partir de laquelle la mise en forme doit être récupérée. Il peut avoir l’une des valeurs suivantes.



| Valeur                                                                                                                                                         | Signification                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <dt>**CSAH \_ par défaut**</dt> </dl>       | Mise en forme de caractères par défaut.<br/>             |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <dt>**\_sélection SCF**</dt> </dl> | Mise en forme des caractères de la sélection actuelle.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Structure [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) qui reçoit les attributs du premier caractère. Le membre **dwMask** spécifie les attributs qui sont cohérents dans toute la sélection. Par exemple, si l’ensemble de la sélection est en italique ou non en italique, CFM \_ Italic est défini ; si la sélection est en partie en italique et partiellement non, cfm \_ Italic n’est pas défini.

Microsoft Rich Edit 2,0 et versions ultérieures : ce paramètre peut être un pointeur vers une structure [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , qui est une extension de la structure [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) . Avant d’envoyer le message **\_ GETCHARFORMAT em** , définissez le membre **cbSize** de la structure pour indiquer la version de la structure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message retourne la valeur du membre **dwMask** de la structure [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





