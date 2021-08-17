---
description: Avertit une application lorsqu’un IME est sur le paragraphe d’ouvrir la fenêtre candidate. L’application reçoit cette commande via le \_ message de \_ notification de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: 439ff125-2731-4eb1-8287-4ca8ace7d8ec
title: Événement IMN_OPENCANDIDATE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dbf6db7415a62b6d77925a4fb7106b70f0b42d77f922e0c1b6df76e71d10c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147632"
---
# <a name="imn_opencandidate-event"></a>\_Événement IMN OPENCANDIDATE

Avertit une application lorsqu’un IME est sur le paragraphe d’ouvrir la fenêtre candidate. L’application reçoit cette commande via le message de [**\_ \_ notification de l’IME WM**](wm-ime-notify.md) avec les paramètres de paramètre, comme indiqué ci-dessous.


```C++
IMN_OPENCANDIDATE
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Défini sur IMN \_ OPENCANDIDATE.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Indicateur de liste de candidats. Chaque bit correspond à une liste de candidats : le bit 0 à la première liste, le bit 1 à la seconde, et ainsi de suite. Si un bit spécifié est 1, la fenêtre candidate correspondante est sur le lieu d’être ouverte.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette commande n’a pas de valeur de retour.

## <a name="remarks"></a>Remarques

Une application doit traiter cette commande si elle affiche des candidats. L’application peut récupérer une liste de candidats à afficher à l’aide de la fonction [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) .

Par défaut, la fenêtre IME crée une fenêtre candidate lors du traitement de cette commande.

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

[**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[**notification de l' \_ IME WM \_**](wm-ime-notify.md)
</dt> </dl>

 

 




