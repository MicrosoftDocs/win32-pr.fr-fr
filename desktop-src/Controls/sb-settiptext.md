---
title: Message SB_SETTIPTEXT (commctrl. h)
description: Définit le texte d’info-bulle pour un composant dans une barre d’État. La barre d’État doit avoir été créée avec le \_ style info-bulles SBT pour activer les info-bulles.
ms.assetid: 8fc3cc00-9742-4861-b2c2-b8aa30f75aaa
keywords:
- SB_SETTIPTEXT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- SB_SETTIPTEXT
- SB_SETTIPTEXTA
- SB_SETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d5ddb3f4fdfe18525e2b444438295f8a926180
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117050"
---
# <a name="sb_settiptext-message"></a>\_Message SB SETTIPTEXT

Définit le texte d’info-bulle pour un composant dans une barre d’État. La barre d’État doit avoir été créée avec le style [**\_ info-bulles SBT**](status-bar-styles.md) pour activer les info-bulles.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro du composant qui recevra le texte d’info-bulle.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une mémoire tampon de caractères qui contient le nouveau texte d’info-bulle.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour n’est pas utilisée.

## <a name="remarks"></a>Notes

Ce texte d’info-bulle s’affiche dans deux situations :

-   Lorsque le volet correspondant dans la barre d’état contient uniquement une icône.
-   Lorsque le volet correspondant dans la barre d’état contient du texte tronqué en raison de la taille du volet.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **SB \_ SETTIPTEXTW** (Unicode) et **SB \_ SETTIPTEXTA** (ANSI)<br/>               |



 

 





