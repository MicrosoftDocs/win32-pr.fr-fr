---
title: Message EM_SETOPTIONS (RichEdit. h)
description: Définit les options pour un contrôle RichEdit.
ms.assetid: 98ef2de9-4c34-45ba-8e8a-eaf505f97f56
keywords:
- EM_SETOPTIONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c43dda8268b42dc264a86600826d2a6b550e35c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103492"
---
# <a name="em_setoptions-message"></a>\_Message SETOPTIONS em

Définit les options pour un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie l’opération, qui peut prendre l’une des valeurs suivantes.



| Valeur                                                                                                                                             | Signification                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**ensemble de ECOOP \_**</dt> </dl> | Définit les options à celles spécifiées par *lParam*.<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ ou**</dt> </dl>    | Combine les options spécifiées avec les options actuelles.<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ et**</dt> </dl> | Conserve uniquement les options actuelles qui sont également spécifiées par *lParam*.<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**ECOOP \_ Xor**</dt> </dl> | Logiquement exclusive ou les options actuelles avec celles qui sont spécifiées par *lParam*.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Spécifie une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                 | Signification                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="ECO_AUTOWORDSELECTION"></span><span id="eco_autowordselection"></span><dl> <dt>**ECO \_ AUTOWORDSELECTION**</dt> </dl> | Sélection automatique du mot sur le double-clic.<br/>                                                                           |
| <span id="ECO_AUTOVSCROLL"></span><span id="eco_autovscroll"></span><dl> <dt>**ECO \_ AUTOVSCROLL**</dt> </dl>                   | Identique au style [**es \_ AUTOVSCROLL**](rich-edit-control-styles.md) .<br/>                                      |
| <span id="ECO_AUTOHSCROLL"></span><span id="eco_autohscroll"></span><dl> <dt>**ECO \_ AUTOHSCROLL**</dt> </dl>                   | Identique au style [**es \_ AUTOHSCROLL**](rich-edit-control-styles.md) .<br/>                                      |
| <span id="ECO_NOHIDESEL"></span><span id="eco_nohidesel"></span><dl> <dt>**ECO \_ NOHIDESEL**</dt> </dl>                         | Identique au style [**es \_ NOHIDESEL**](rich-edit-control-styles.md) .<br/>                                          |
| <span id="ECO_READONLY"></span><span id="eco_readonly"></span><dl> <dt>**ECO en \_ lecture seule**</dt> </dl>                            | Identique au style [**es \_ ReadOnly**](rich-edit-control-styles.md) .<br/>                                            |
| <span id="ECO_WANTRETURN"></span><span id="eco_wantreturn"></span><dl> <dt>**ECO \_ WANTRETURN**</dt> </dl>                      | Identique au style [**es \_ WANTRETURN**](rich-edit-control-styles.md) .<br/>                                        |
| <span id="ECO_SELECTIONBAR"></span><span id="eco_selectionbar"></span><dl> <dt>**ECO \_ SELECTIONBAR**</dt> </dl>                | Identique au style [**es \_ SELECTIONBAR**](rich-edit-control-styles.md) .<br/>                                    |
| <span id="ECO_VERTICAL"></span><span id="eco_vertical"></span><dl> <dt>**ECO \_ vertical**</dt> </dl>                            | Identique au [**style \_ vertical es**](rich-edit-control-styles.md) . Disponible uniquement dans les versions asiatiques.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message retourne les options actuelles du contrôle d’édition.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Styles de contrôle RichEdit**](rich-edit-control-styles.md)
</dt> </dl>

 

 





