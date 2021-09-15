---
description: Envoyé à toutes les fenêtres de niveau supérieur lorsque le système détecte plus de 12,5% de l’heure système pendant un intervalle de 30 à 60 secondes est consacré au compactage de la mémoire. Cela indique que la mémoire système est insuffisante.
ms.assetid: e8adc655-0252-4a43-8a62-b08e96f5744e
title: Message WM_COMPACTING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb94e77a1c6b27701b26ed4b7e6e01f326aaa40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404216"
---
# <a name="wm_compacting-message"></a>\_Message de compactage WM

Envoyé à toutes les fenêtres de niveau supérieur lorsque le système détecte plus de 12,5% de l’heure système pendant un intervalle de 30 à 60 secondes est consacré au compactage de la mémoire. Cela indique que la mémoire système est insuffisante.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> [!Note]  
> ce message est fourni uniquement à des fins de compatibilité avec les applications à base de Windows 16 bits.

 


```C++
#define WM_COMPACTING                   0x0041
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Taux de temps processeur actuellement passé par le système à compacter la mémoire sur le temps processeur actuellement passé par le système effectuant d’autres opérations. Par exemple, 0x8000 représente 50% du temps processeur passé à compacter la mémoire.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **LRESULT**

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Lorsqu’une application reçoit ce message, elle doit libérer autant de mémoire que possible, en tenant compte du niveau actuel d’activité de l’application et du nombre total d’applications en cours d’exécution sur le système.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Windows Vue](windows.md)
</dt> </dl>

 

 
