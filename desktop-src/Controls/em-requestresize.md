---
title: Message EM_REQUESTRESIZE (RichEdit. h)
description: Force un contrôle RichEdit à envoyer un code de \_ notification en REQUESTRESIZE à sa fenêtre parente.
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- EM_REQUESTRESIZE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41e7be8e0f30d5c1ec011247f3964292c2218e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006429"
---
# <a name="em_requestresize-message"></a>\_Message REQUESTRESIZE em

Force un contrôle RichEdit à envoyer un code de notification en [**\_ REQUESTRESIZE**](en-requestresize.md) à sa fenêtre parente.

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

Ce message ne retourne pas de valeur.

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

**Référence**
</dt> <dt>

[**en \_ REQUESTRESIZE**](en-requestresize.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**taille du WM \_**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

