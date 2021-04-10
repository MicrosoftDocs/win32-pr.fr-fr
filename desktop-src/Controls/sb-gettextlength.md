---
title: Message SB_GETTEXTLENGTH (commctrl. h)
description: Récupère la longueur, en caractères, du texte à partir de la partie spécifiée d’une fenêtre d’État.
ms.assetid: 2cd43106-dd43-499e-b595-760e9ededab5
keywords:
- SB_GETTEXTLENGTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_GETTEXTLENGTH
- SB_GETTEXTLENGTHA
- SB_GETTEXTLENGTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b08dd3b870c3c59e5aafbeb9d53baef3816a726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942548"
---
# <a name="sb_gettextlength-message"></a>\_Message SB GETTEXTLENGTH

Récupère la longueur, en caractères, du texte à partir de la partie spécifiée d’une fenêtre d’État.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro du composant à partir duquel récupérer du texte.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur 32 bits qui se compose de valeurs 2 16 bits. Le mot de poids faible spécifie la longueur, en caractères, du texte. Le mot de poids fort spécifie le type d’opération utilisé pour dessiner le texte. Le type peut prendre l’une des valeurs suivantes :



| Code de retour                                                                                    | Description                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>               | Le texte est dessiné avec une bordure qui apparaît plus bas que le plan de la fenêtre.<br/>          |
| <dl> <dt>**SBT \_ NOfrontières**</dt> </dl>  | Le texte est dessiné sans bordures.<br/>                                                     |
| <dl> <dt>**SBT \_ OwnerDraw**</dt> </dl>  | Le texte est dessiné par la fenêtre parente.<br/>                                                |
| <dl> <dt>**SBT \_ fenêtre indépendante**</dt> </dl>     | Le texte est dessiné avec une bordure qui doit apparaître plus haut que le plan de la fenêtre.<br/>         |
| <dl> <dt>**SBT \_ RTLREADING**</dt> </dl> | Le texte s’affiche dans le sens inverse du texte de la fenêtre parente.<br/> |



 

## <a name="remarks"></a>Notes

Les fenêtres normales affichent le texte de gauche à droite (LTR). Les fenêtres peuvent être *mises en miroir* pour afficher des langues telles que l’hébreu ou l’arabe, qui sont lues de droite à gauche (RTL). Si SBT \_ RTLREADING est défini, le texte de la fenêtre d’état spécifié est lu dans le sens inverse à partir du texte de la fenêtre parente.

Ce message retourne une longueur de chaîne maximale de 65 535 caractères. Si la chaîne de texte réelle est plus longue, le message [**SB \_ GETTEXT**](sb-gettext.md) le tronque.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **SB \_ GETTEXTLENGTHW** (Unicode) et **SB \_ GETTEXTLENGTHA** (ANSI)<br/>         |



 

 





