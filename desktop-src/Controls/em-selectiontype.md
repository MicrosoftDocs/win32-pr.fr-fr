---
title: Message EM_SELECTIONTYPE (RichEdit. h)
description: Détermine le type de sélection d’un contrôle RichEdit.
ms.assetid: a4200e32-1056-47bd-be47-5fabaf99c058
keywords:
- EM_SELECTIONTYPE les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509178"
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

## <a name="return-value"></a>Valeur retournée

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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**taille du WM \_**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

