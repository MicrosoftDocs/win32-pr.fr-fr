---
title: Message EM_REQUESTRESIZE (RichEdit. h)
description: Force un contrôle RichEdit à envoyer un code de \_ notification en REQUESTRESIZE à sa fenêtre parente.
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- EM_REQUESTRESIZE les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200581"
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

## <a name="return-value"></a>Valeur retournée

Ce message ne retourne pas de valeur.

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

**Référence**
</dt> <dt>

[**en \_ REQUESTRESIZE**](en-requestresize.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**taille du WM \_**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

