---
description: Demande à une fenêtre IME d’afficher la position de la fenêtre d’État. Pour envoyer cette commande, l’application utilise le \_ message de \_ contrôle de l’IME WM avec les paramètres indiqués ci-dessous.
ms.assetid: 59c7baae-1b8a-4761-9814-31afd8d39691
title: Commande IMC_GETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfb542ef95a7825e4809e0fa2ce9175493bffeffbbaa36926a91299746026d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068079"
---
# <a name="imc_getstatuswindowpos-command"></a>\_Commande IMC GETSTATUSWINDOWPOS

Demande à une fenêtre IME d’afficher la position de la fenêtre d’État. Pour envoyer cette commande, l’application utilise le message de [**\_ \_ contrôle de l’IME WM**](wm-ime-control.md) avec les paramètres indiqués ci-dessous.


```C++
LRESULT IMC_GETSTATUSWINDOWPOS
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Défini sur IMC \_ GETSTATUSWINDOWPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une structure de [**points**](/previous-versions//dd162808(v=vs.85)) qui contient la coordonnée x et la coordonnée y de la position de la fenêtre d’État en coordonnées d’écran, par rapport à l’angle supérieur gauche de l’écran.

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

 

 
