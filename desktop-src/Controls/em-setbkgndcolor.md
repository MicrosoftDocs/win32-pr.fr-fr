---
title: Message EM_SETBKGNDCOLOR (RichEdit. h)
description: Le \_ message SETBKGNDCOLOR em définit la couleur d’arrière-plan d’un contrôle RichEdit.
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- EM_SETBKGNDCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETBKGNDCOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091f04909e2660498f1380628439c067b5438b6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006421"
---
# <a name="em_setbkgndcolor-message"></a>\_Message SETBKGNDCOLOR em

Le **message \_ SETBKGNDCOLOR em** définit la couleur d’arrière-plan d’un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie s’il faut utiliser la couleur système. Si ce paramètre est une valeur différente de zéro, l’arrière-plan est défini sur la couleur système d’arrière-plan de la fenêtre. Dans le cas contraire, l’arrière-plan est défini sur la couleur spécifiée.

</dd> <dt>

*lParam* 
</dt> <dd>

Structure [**COLORREF**](/windows/desktop/gdi/colorref) spécifiant la couleur si *wParam* est égal à zéro. Pour générer **COLORREF**, utilisez la macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Ce message retourne la couleur d’arrière-plan d’origine.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Autres ressources**
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

