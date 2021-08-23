---
title: Message SB_GETTIPTEXT (commctrl. h)
description: Récupère le texte d’info-bulle pour un composant dans une barre d’État. La barre d’État doit être créée avec le \_ style info-bulles SBT pour activer les info-bulles.
ms.assetid: a3936830-a855-4ef6-b179-3aa3730cd0b8
keywords:
- SB_GETTIPTEXT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- SB_GETTIPTEXT
- SB_GETTIPTEXTA
- SB_GETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89a78fa6650d850cad2b6de8cc77f1d44b49b8325bf6856b989953fc6511f56f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637129"
---
# <a name="sb_gettiptext-message"></a>\_Message SB GETTIPTEXT

Récupère le texte d’info-bulle pour un composant dans une barre d’État. La barre d’État doit être créée avec le style [**\_ info-bulles SBT**](status-bar-styles.md) pour activer les info-bulles.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie l’index de base zéro de la partie qui reçoit le texte info-bulle. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la taille de la mémoire tampon au niveau de *lParam*, en caractères.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une mémoire tampon de caractères qui reçoit le texte d’info-bulle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas utilisée.

## <a name="remarks"></a>Remarques

**Avertissement de sécurité :** L’utilisation incorrecte de ce message peut entraîner des problèmes pour votre application. Par exemple, si le texte est trop grand pour la mémoire tampon *lParam* , cela peut provoquer un dépassement de capacité de la mémoire tampon. vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **SB \_ GETTIPTEXTW** (Unicode) et **SB \_ GETTIPTEXTA** (ANSI)<br/>               |



 

