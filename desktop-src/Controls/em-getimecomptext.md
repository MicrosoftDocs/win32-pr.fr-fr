---
title: Message EM_GETIMECOMPTEXT (RichEdit. h)
description: Récupère le texte de la composition de l’éditeur de méthode d’entrée (IME).
ms.assetid: 1516305c-5f87-4ae0-97db-8709c71abacc
keywords:
- EM_GETIMECOMPTEXT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETIMECOMPTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 834c55d6b5e40de7dcacfeb3e2d0c2e0878a0f3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857931"
---
# <a name="em_getimecomptext-message"></a>\_Message GETIMECOMPTEXT em

Récupère le texte de la composition de l’éditeur de méthode d’entrée (IME).

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Structure [**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext) .

</dd> <dt>

*lParam* 
</dt> <dd>

Mémoire tampon qui reçoit le texte de composition. La taille de cette mémoire tampon est contenue dans le membre **CB** de la structure *wParam* .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

En cas de réussite, la valeur de retour est le nombre de caractères Unicode copiés dans la mémoire tampon. Dans le cas contraire, il est égal à zéro.

## <a name="remarks"></a>Notes

Ce message accepte uniquement les chaînes Unicode.

**Avertissement de sécurité :** Veillez à disposer d’une mémoire tampon suffisante pour la taille de l’entrée. Dans le cas contraire, vous risquez de rencontrer des problèmes pour votre application.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP1 uniquement\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
</dt> </dl>

 

 





