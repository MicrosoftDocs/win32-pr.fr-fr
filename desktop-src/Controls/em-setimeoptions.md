---
title: Message EM_SETIMEOPTIONS (RichEdit. h)
description: Définit les options de l’éditeur de méthode d’entrée (IME).
ms.assetid: 8a72ee1c-f6b8-44eb-b8df-57cd834db326
keywords:
- EM_SETIMEOPTIONS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59be3148bd00abd998af200368f2ed77ad3ff911
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006385"
---
# <a name="em_setimeoptions-message"></a>\_Message SETIMEOPTIONS em

Définit les options de l’éditeur de méthode d’entrée (IME).

> [!Note]  
> Ce message est pris en charge uniquement dans les versions asiatiques de Microsoft Rich Edit 1,0. Elle n’est pas prise en charge dans les versions ultérieures.

 

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie l’une des valeurs suivantes.



| Valeur                                                                                                                                             | Signification                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**ensemble de ECOOP \_**</dt> </dl> | Définit les options à celles spécifiées par *lParam*.<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ ou**</dt> </dl>    | Combine les options spécifiées avec les options actuelles.<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ et**</dt> </dl> | Conserve uniquement les options actuelles qui sont également spécifiées par *lParam*.<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**ECOOP \_ Xor**</dt> </dl> | Logiquement exclusive ou les options actuelles avec celles qui sont spécifiées par *lParam.*<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Spécifie une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                 | Signification                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMF_CLOSESTATUSWINDOW"></span><span id="imf_closestatuswindow"></span><dl> <dt>**\_CLOSESTATUSWINDOW IMF**</dt> </dl> | Ferme la fenêtre d’État IME lorsque le contrôle reçoit le focus d’entrée.<br/>                                                                                                               |
| <span id="IMF_FORCEACTIVE"></span><span id="imf_forceactive"></span><dl> <dt>**\_FORCEACTIVE IMF**</dt> </dl>                   | Active l’IME lorsque le contrôle reçoit le focus d’entrée.<br/>                                                                                                                          |
| <span id="IMF_FORCEDISABLE"></span><span id="imf_forcedisable"></span><dl> <dt>**\_FORCEDISABLE IMF**</dt> </dl>                | Désactive l’IME lorsque le contrôle reçoit le focus d’entrée.<br/>                                                                                                                           |
| <span id="IMF_FORCEENABLE"></span><span id="imf_forceenable"></span><dl> <dt>**\_FORCEENABLE IMF**</dt> </dl>                   | Active l’IME lorsque le contrôle reçoit le focus d’entrée.<br/>                                                                                                                            |
| <span id="IMF_FORCEINACTIVE"></span><span id="imf_forceinactive"></span><dl> <dt>**\_FORCEINACTIVE IMF**</dt> </dl>             | Désactive l’IME lorsque le contrôle reçoit le focus d’entrée.<br/>                                                                                                                        |
| <span id="IMF_FORCENONE"></span><span id="imf_forcenone"></span><dl> <dt>**\_FORCENONE IMF**</dt> </dl>                         | Désactive la gestion de l’IME.<br/>                                                                                                                                                                |
| <span id="IMF_FORCEREMEMBER"></span><span id="imf_forceremember"></span><dl> <dt>**\_FORCEREMEMBER IMF**</dt> </dl>             | Restaure l’État IME précédent lorsque le contrôle reçoit le focus d’entrée.<br/>                                                                                                           |
| <span id="IMF_MULTIPLEEDIT"></span><span id="imf_multipleedit"></span><dl> <dt>**\_MULTIPLEEDIT IMF**</dt> </dl>                | Spécifie que la chaîne de composition ne sera pas annulée ou déterminée par les modifications de focus. Cela permet à une application d’avoir des chaînes de composition distinctes sur chaque contrôle RichEdit.<br/> |
| <span id="IMF_VERTICAL"></span><span id="imf_vertical"></span><dl> <dt>**VERTICAL de IMF \_**</dt> </dl>                            | Remarque utilisée dans Rich Edit 2,0 et versions ultérieures. <br/>                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si l’opération a échoué, la valeur de retour est une valeur différente de zéro.

Si l’opération échoue, la valeur de retour est zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETIMEOPTIONS em**](em-getimeoptions.md)
</dt> </dl>

 

 





