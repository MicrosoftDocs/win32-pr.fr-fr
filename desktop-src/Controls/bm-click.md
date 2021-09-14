---
title: Message BM_CLICK (winuser. h)
description: Simule l’utilisateur qui clique sur un bouton. Ce message force le bouton à recevoir les \_ messages WM LBUTTONDOWN et WM \_ LBUTTONUP, ainsi que la fenêtre parente du bouton pour recevoir un code de notification sur lequel un clic a été \_ effectué.
ms.assetid: f76ca5eb-170c-43fc-a239-67af15497f08
keywords:
- BM_CLICK les contrôles de Windows de message
topic_type:
- apiref
api_name:
- BM_CLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b86c4809ac1ded3a9b7c57d1b73b70ab1cebc3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920384"
---
# <a name="bm_click-message"></a>\_Message de clic sur BM

Simule l’utilisateur qui clique sur un bouton. Ce message force le bouton à recevoir les messages [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) et [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) , ainsi que la fenêtre parente du bouton pour recevoir un code de notification sur lequel un clic a été [ \_ effectué](bn-clicked.md) .

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

Si le bouton se trouve dans une boîte de dialogue et que la boîte de dialogue n’est pas active, le message de **\_ clic** peut échouer. Pour garantir la réussite de cette situation, appelez la fonction [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) pour activer la boîte de dialogue avant d’envoyer le message de **\_ clic de BM** au bouton.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

