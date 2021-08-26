---
description: Demande à une fenêtre IME d’afficher la position de la fenêtre candidate. Pour envoyer cette commande, l’application utilise le \_ message de \_ contrôle de l’IME WM avec les paramètres indiqués ci-dessous.
ms.assetid: e582dbc2-8081-424c-a972-1a182a477293
title: Commande IMC_GETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e155a08c9d95fa2ac9f865d80b18d51120d19b28489bcad418eb4323dda39c3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107319"
---
# <a name="imc_getcandidatepos-command"></a>\_Commande IMC GETCANDIDATEPOS

Demande à une fenêtre IME d’afficher la position de la fenêtre candidate. Pour envoyer cette commande, l’application utilise le message de [**\_ \_ contrôle de l’IME WM**](wm-ime-control.md) avec les paramètres indiqués ci-dessous.


```C++
LRESULT IMC_GETCANDIDATEPOS
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Défini sur IMC \_ GETCANDIDATEPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Pointeur vers une structure [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) qui contient la position de la fenêtre candidate.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne 0 en cas de réussite, ou une valeur différente de zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

Étant donné que l’IME peut ajuster la position d’une fenêtre candidate, une application utilise cette commande pour obtenir la position réelle pour décider s’il faut repositionner la fenêtre. La position Récupérée est dans les coordonnées de la fenêtre par rapport à la fenêtre qui a le focus d’entrée actuel.

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
</dt> </dl>

 

 




