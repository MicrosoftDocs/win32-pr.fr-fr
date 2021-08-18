---
description: Envoyé à une application lorsque l’IME obtient un caractère du résultat de la conversion. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 1e1353c3-5215-4829-a00a-2fee47a430eb
title: Message WM_IME_CHAR (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337ca982cbd755e01f3dfab465d8b82948dfdbf053a4a7c03417a1d508bc42d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146782"
---
# <a name="wm_ime_char-message"></a>\_Message de \_ type de message IME WM

Envoyé à une application lorsque l’IME obtient un caractère du résultat de la conversion. Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,
 WM_IME_CHAR,
 WPARAM wParam,
 LPARAM lParam   
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de fenêtre.

</dd> <dt>

*wParam* 
</dt> <dd>

**DBCS :** Valeur de caractère codé sur un octet ou sur deux octets. Pour un caractère codé sur deux octets, (BYTE) (wParam >> 8) contient l’octet de tête. Notez que les parenthèses sont nécessaires, car l’opérateur de cast a une priorité plus élevée que l’opérateur de décalage.

**Unicode :** Valeur de caractère Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

L’indicateur de répétition, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de la clé précédente et l’indicateur d’état de transition, avec les valeurs définies ci-dessous.



| bit   | Signification                                                                              |
|-------|--------------------------------------------------------------------------------------|
| 0-15  | Nombre de répétitions. Étant donné que les premier et deuxième octets sont continus, il s’agit toujours de 1. |
| 16-23 | Recherchez dans le code un caractère asiatique complet.                                            |
| 24    | Clé étendue.                                                                        |
| 25-28 | Non utilisé.                                                                            |
| 29    | Code de contexte.                                                                        |
| 30    | État de la clé précédente.                                                                  |
| 31    | État de transition.                                                                    |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Contrairement au message [**WM \_ char**](../inputdev/wm-char.md) pour une fenêtre non Unicode, ce message peut inclure des valeurs de caractères codés sur deux octets et sur un octet. Pour une fenêtre Unicode, ce message est le même que le \_ type WM.

Pour une fenêtre non Unicode, si le message de \_ type IME WM \_ contient un caractère codé sur deux octets et que l’application transmet ce message à [**DEFWINDOWPROC**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), l’IME convertit ce message en deux \_ messages WM char, chacun contenant un octet du caractère codé sur deux octets.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de méthode d’entrée](input-method-manager.md)
</dt> <dt>

[Messages du gestionnaire de méthode d’entrée](input-method-manager-messages.md)
</dt> </dl>

 

 
