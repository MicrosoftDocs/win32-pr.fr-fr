---
title: Message EM_FINDWORDBREAK (RichEdit. h)
description: Recherche la prochaine césure de mot avant ou après la position de caractère spécifiée ou récupère des informations sur le caractère à cette position.
ms.assetid: b5df1365-4672-4c82-8ae4-ebf8b60bf871
keywords:
- EM_FINDWORDBREAK les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_FINDWORDBREAK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6533358c0f4f521bc7021e290dfe11d66d4499e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006505"
---
# <a name="em_findwordbreak-message"></a>\_Message FINDWORDBREAK em

Recherche la prochaine césure de mot avant ou après la position de caractère spécifiée ou récupère des informations sur le caractère à cette position.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie l’opération de recherche. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                  | Signification                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WB_CLASSIFY"></span><span id="wb_classify"></span><dl> <dt>**WB \_ classifier**</dt> </dl>                | Retourne la classe de caractères et les indicateurs de saut de mot du caractère à la position spécifiée.<br/>                                                                                                                          |
| <span id="WB_ISDELIMITER"></span><span id="wb_isdelimiter"></span><dl> <dt>**WB \_ ISDELIMITER**</dt> </dl>       | Retourne la **valeur true** si le caractère situé à la position spécifiée est un délimiteur, ou **false** dans le cas contraire.<br/>                                                                                                                   |
| <span id="WB_LEFT"></span><span id="wb_left"></span><dl> <dt>**WB \_ gauche**</dt> </dl>                            | Recherche le caractère le plus proche avant la position spécifiée qui commence un mot.<br/>                                                                                                                                         |
| <span id="WB_LEFTBREAK"></span><span id="wb_leftbreak"></span><dl> <dt>**WB \_ LEFTBREAK**</dt> </dl>             | Recherche le mot suivant à la fin de la position spécifiée. Cette valeur est identique à celle de WB \_ PREVBREAK.<br/>                                                                                                                       |
| <span id="WB_MOVEWORDLEFT"></span><span id="wb_movewordleft"></span><dl> <dt>**WB \_ MOVEWORDLEFT**</dt> </dl>    | Recherche le caractère suivant qui commence un mot avant la position spécifiée. Cette valeur est utilisée pendant le traitement des touches CTRL + Flèche gauche. Cette valeur est similaire à celle de WB \_ MOVEWORDPREV. Pour plus d'informations, consultez la section Notes.<br/> |
| <span id="WB_MOVEWORDRIGHT"></span><span id="wb_movewordright"></span><dl> <dt>**WB \_ MOVEWORDRIGHT**</dt> </dl> | Recherche le caractère suivant qui commence un mot après la position spécifiée. Cette valeur est utilisée pendant le traitement de la touche CTRL + droite. Cette valeur est similaire à celle de WB \_ MOVEWORDNEXT. Pour plus d'informations, consultez la section Notes.<br/>           |
| <span id="WB_RIGHT"></span><span id="wb_right"></span><dl> <dt>**WB à \_ droite**</dt> </dl>                         | Recherche le caractère suivant qui commence un mot après la position spécifiée.<br/>                                                                                                                                             |
| <span id="WB_RIGHTBREAK"></span><span id="wb_rightbreak"></span><dl> <dt>**WB \_ RIGHTBREAK**</dt> </dl>          | Recherche le délimiteur de fin de mot suivant après la position spécifiée. Cette valeur est identique à celle de WB \_ NEXTBREAK.<br/>                                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Position de départ d’un caractère de base zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Le message retourne une valeur basée sur le paramètre *wParam* .



| Code de retour                                                                                    | Description                                                                                                            |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**wParam**</dt> </dl>          | Valeur renvoyée<br/>                                                                                                |
| <dl> <dt>**WB \_ classifier**</dt> </dl>    | Retourne la classe de caractères et les indicateurs de saut de mot du caractère à la position spécifiée.<br/>                |
| <dl> <dt>**WB \_ ISDELIMITER**</dt> </dl> | Retourne la **valeur true** si le caractère situé à la position spécifiée est un délimiteur. Sinon, elle retourne **false**.<br/> |
| <dl> <dt>**Personnes**</dt> </dl>          | Retourne l’index de caractère de l’arrêt de mot.<br/>                                                              |



 

## <a name="remarks"></a>Notes

Si *wParam* est WB \_ Left et WB \_ Right, la procédure de saut de mot recherche les césures de mots uniquement après les délimiteurs. Cela correspond à la fonctionnalité d’un contrôle d’édition. Si *wParam* est WB \_ MOVEWORDLEFT ou WB \_ MOVEWORDRIGHT, la procédure de césure de mots compare également les classes de caractères et les indicateurs de césure lexicale.

Pour plus d’informations sur les classes de caractères et les indicateurs de césure lexicale, consultez [mots et sauts de ligne](using-rich-edit-controls.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





