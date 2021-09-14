---
title: Message EM_SELECTIONTYPE (RichEdit. h)
description: Détermine le type de sélection d’un contrôle RichEdit.
ms.assetid: a4200e32-1056-47bd-be47-5fabaf99c058
keywords:
- EM_SELECTIONTYPE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SELECTIONTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0deb62ac3bf774c72bb076f6fce9aa8c77b423f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006425"
---
# <a name="em_selectiontype-message"></a>\_Message SELECTIONTYPE em

Détermine le type de sélection d’un contrôle RichEdit.

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

## <a name="return-value"></a>Valeur de retour

Si la sélection est vide, la valeur de retour est SEL \_ vide.

Si la sélection n’est pas vide, la valeur de retour est un jeu d’indicateurs contenant une ou plusieurs des valeurs suivantes.



| Code de retour                                                                                     | Description                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**\_texte sel**</dt> </dl>        | Texte.<br/>                            |
| <dl> <dt>**SEL, \_ objet**</dt> </dl>      | Au moins un objet COM.<br/>         |
| <dl> <dt>**SEL \_ MULTIchar**</dt> </dl>   | Plusieurs caractères de texte.<br/> |
| <dl> <dt>**SEL \_ MULTIobject**</dt> </dl> | Plusieurs objets COM.<br/>        |



 

## <a name="remarks"></a>Notes

Ce message est utile lors du traitement de la [**\_ taille WM**](/windows/desktop/winmsg/wm-size) pour le parent d’un contrôle Rich Edit sans fin.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**taille du WM \_**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

