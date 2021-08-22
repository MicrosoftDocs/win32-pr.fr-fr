---
description: Indique à une fenêtre IME de spécifier la police logique à utiliser pour afficher les caractères intermédiaires dans la fenêtre de composition. Pour envoyer cette commande, l’application utilise le \_ message de \_ contrôle de l’IME WM avec les paramètres indiqués ci-dessous.
ms.assetid: 17b222e7-bf57-4cdd-8475-d9a8be03ab7f
title: Commande IMC_SETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ebc9f435371d4ae08b12191419c95fd53c69256064f0e90bb654e75fab922f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949270"
---
# <a name="imc_setcompositionfont-command"></a>\_Commande IMC SETCOMPOSITIONFONT

Indique à une fenêtre IME de spécifier la police logique à utiliser pour afficher les caractères intermédiaires dans la fenêtre de composition. Pour envoyer cette commande, l’application utilise le message de [**\_ \_ contrôle de l’IME WM**](wm-ime-control.md) avec les paramètres indiqués ci-dessous.


```C++
LRESULT IMC_SETCOMPOSITIONFONT
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Défini sur IMC \_ SETCOMPOSITIONFONT.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Pointeur vers une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) qui contient des informations sur la police logique.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne 0 en cas de réussite, ou une valeur différente de zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

Lors du traitement de cette commande, la fenêtre IME modifie la police actuellement sélectionnée dans le contexte d’entrée.

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

 

 
