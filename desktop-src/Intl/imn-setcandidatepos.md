---
description: Avertit une application lorsque le traitement des candidats est terminé et que l’IME est sur le paragraphe de déplacer la fenêtre candidate. L’application reçoit cette commande via le \_ message de \_ notification de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: 64252d88-130b-44c3-854a-78b01def7a13
title: IMN_SETCANDIDATEPOS le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 689dfe0c38f5508c853af94e271bb1f333bfbad0df18b3fab09450d73497e7fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107059"
---
# <a name="imn_setcandidatepos-notification-code"></a>\_Code de notification SETCANDIDATEPOS IMN

Avertit une application lorsque le traitement des candidats est terminé et que l’IME est sur le paragraphe de déplacer la fenêtre candidate. L’application reçoit cette commande via le message de [**\_ \_ notification de l’IME WM**](wm-ime-notify.md) avec les paramètres de paramètre, comme indiqué ci-dessous.


```C++
IMN_SETCANDIDATEPOS
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Défini sur IMN \_ SETCANDIDATEPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Indicateur de liste de candidats. Chaque bit correspond à une liste de candidats : le bit 0 à la première liste, le bit 1 à la seconde, et ainsi de suite. Si un bit spécifié est 1, la fenêtre candidate correspondante va être déplacée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette commande n’a pas de valeur de retour.

## <a name="remarks"></a>Remarques

Une application doit traiter cette commande si elle affiche la fenêtre candidate elle-même.

La fenêtre IME déplace la fenêtre candidate lors du traitement de cette commande.

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

[**notification de l' \_ IME WM \_**](wm-ime-notify.md)
</dt> </dl>

 

 




