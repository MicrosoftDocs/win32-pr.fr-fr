---
description: Demande à une fenêtre IME de définir la position de la fenêtre d’État. Pour envoyer cette commande, l’application utilise le \_ \_ message de contrôle de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: d77de7ab-1fbc-42f4-829e-e9fb51668d21
title: Commande IMC_SETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee41deac781f7885185df429c5b5231a36f9d5008b5754b718398e7ab4cd060a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107229"
---
# <a name="imc_setstatuswindowpos-command"></a>\_Commande IMC SETSTATUSWINDOWPOS

Demande à une fenêtre IME de définir la position de la fenêtre d’État. Pour envoyer cette commande, l’application utilise le message de [**\_ \_ contrôle de l’IME WM**](wm-ime-control.md) avec les paramètres de paramètre, comme indiqué ci-dessous.


```C++
LRESULT IMC_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Défini sur IMC \_ SETSTATUSWINDOWPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Pointeur vers une structure de [**points**](/previous-versions//dd162808(v=vs.85)) qui contient la coordonnée x et la coordonnée y de la position de la fenêtre d’État. Les coordonnées sont exprimées en coordonnées d’écran, par rapport à l’angle supérieur gauche de l’affichage.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne 0 en cas de réussite, ou une valeur différente de zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>Imm. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de méthode d’entrée](input-method-manager.md)
</dt> <dt>

[Commandes du gestionnaire de méthode d’entrée](input-method-manager-commands.md)
</dt> <dt>

[**contrôle de l' \_ IME WM \_**](wm-ime-control.md)
</dt> </dl>

 

 
