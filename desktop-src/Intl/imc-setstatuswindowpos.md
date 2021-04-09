---
description: Demande à une fenêtre IME de définir la position de la fenêtre d’État. Pour envoyer cette commande, l’application utilise le \_ \_ message de contrôle de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: d77de7ab-1fbc-42f4-829e-e9fb51668d21
title: Commande IMC_SETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99c57eef1a4748bb58018ee47aaee21eb677016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034057"
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
| En-tête<br/>                   | <dl> <dt>IMM. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de méthode d’entrée](input-method-manager.md)
</dt> <dt>

[Commandes du gestionnaire de méthode d’entrée](input-method-manager-commands.md)
</dt> <dt>

[**contrôle de l' \_ IME WM \_**](wm-ime-control.md)
</dt> </dl>

 

 
