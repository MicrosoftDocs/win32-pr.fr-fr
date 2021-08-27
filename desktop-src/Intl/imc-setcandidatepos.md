---
description: Demande à une fenêtre IME de définir la position de la fenêtre candidats. Pour envoyer cette commande, l’application utilise le \_ message de \_ contrôle de l’IME WM avec les paramètres indiqués ci-dessous.
ms.assetid: 7a2f9958-4a4e-462a-9737-e7796fd90216
title: Commande IMC_SETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fbce21cac53eecf3ad5b99cc7dbe5cf5b52304ed25869a5c3f6ae729ac9d016
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107269"
---
# <a name="imc_setcandidatepos-command"></a>\_Commande IMC SETCANDIDATEPOS

Demande à une fenêtre IME de définir la position de la fenêtre candidats. Pour envoyer cette commande, l’application utilise le message de [**\_ \_ contrôle de l’IME WM**](wm-ime-control.md) avec les paramètres indiqués ci-dessous.


```C++
LRESULT IMC_SETCANDIDATEPOS
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Défini sur IMC \_ SETCANDIDATEPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Pointeur vers une structure [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) qui contient la coordonnée x et la coordonnée y de la fenêtre candidats. L’application doit définir le membre **dwIndex** de cette structure.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne 0 en cas de réussite, ou une valeur différente de zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

Cette commande est destinée aux applications qui affichent des caractères de composition seuls, mais qui utilisent la fenêtre IME pour afficher les candidats.

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

[**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[**contrôle de l' \_ IME WM \_**](wm-ime-control.md)
</dt> </dl>

 

 




