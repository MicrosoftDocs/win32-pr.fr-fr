---
title: Message PSM_ISDIALOGMESSAGE (Prsht. h)
description: Transmet un message à une boîte de dialogue de feuille de propriétés et indique si la boîte de dialogue a traité le message. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet IsDialogMessage.
ms.assetid: 7629c3f8-0b10-4585-8a95-9309c75b3ebb
keywords:
- PSM_ISDIALOGMESSAGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PSM_ISDIALOGMESSAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b753fc849d76e3ac5071dd85bdd94950460fbb10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117490"
---
# <a name="psm_isdialogmessage-message"></a>\_Message PSM ISDIALOGMESSAGE

Transmet un message à une boîte de dialogue de feuille de propriétés et indique si la boîte de dialogue a traité le message. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) qui contient le message à vérifier.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** si le message a été traité, ou **false** si le message n’a pas été traité.

## <a name="remarks"></a>Notes

Votre boucle de messages doit utiliser le message **\_ ISDIALOGMESSAGE PSM** avec les feuilles de propriétés non modales pour transmettre les messages à la boîte de dialogue de la feuille de propriétés. Sur les systèmes qui prennent en charge Unicode, utilisez les versions Unicode des fonctions [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) et [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) (**GetMessageW** et **PeekMessageW**) pour récupérer les messages.

Si la valeur de retour indique que le message a été traité, il ne doit pas être passé à la fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) ou [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) .

> [!Note]  
> Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

