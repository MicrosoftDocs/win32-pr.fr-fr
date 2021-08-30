---
title: Message LB_SETTABSTOPS (winuser. h)
description: Définit les positions des taquets de tabulation dans une zone de liste.
ms.assetid: b96b974e-b1e6-4361-98bb-4dc21c752690
keywords:
- LB_SETTABSTOPS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d842b0c7e2cdcc792227ecb390fa3bc2a4c9d210b7c028b266c867a0c473808
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085319"
---
# <a name="lb_settabstops-message"></a>\_Message SETTABSTOPS lb

Définit les positions des taquets de tabulation dans une zone de liste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie le nombre de taquets de tabulation.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers le premier membre d’un tableau d’entiers contenant les taquets de tabulation. Les entiers représentent le nombre de trimestres de la largeur moyenne des caractères pour la police sélectionnée dans la zone de liste. Par exemple, un taquet de tabulation de 4 est placé à 1,0 unités de caractères et un taquet de tabulation de 6 est placé à 1,5 unités de caractères moyennes. Toutefois, si la zone de liste fait partie d’une boîte de dialogue, les entiers se trouvent dans les unités du modèle de boîte de dialogue. Les taquets de tabulation doivent être triés par ordre croissant ; les onglets en arrière ne sont pas autorisés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si tous les onglets spécifiés sont définis, la valeur de retour est **true**; Sinon, la **valeur est false**.

## <a name="remarks"></a>Remarques

Pour répondre au message **lb \_ SETTABSTOPS** , la zone de liste doit avoir été créée avec le [**style \_ USETABSTOPS**](list-box-styles.md) .

Si *wParam* a pour valeur 0 et *lParam* la **valeur null**, le taquet de tabulation par défaut est deux unités de modèle de boîte de dialogue. Si *wParam* est 1, la zone de liste aura des taquets de tabulation séparés par la distance spécifiée par *lParam*.

Si *lParam* pointe vers plus d’une valeur unique, un taquet de tabulation sera défini pour chaque valeur dans *lParam*, jusqu’au nombre spécifié par *wParam*.

Les valeurs spécifiées par *lParam* se trouvent dans les unités de modèle de boîte de dialogue, qui sont les unités indépendantes du périphérique utilisées dans les modèles de boîte de dialogue. Pour convertir des mesures à partir d’unités de modèle de boîte de dialogue en unités d’écran (pixels), utilisez la fonction [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) .

Windows 95/Windows 98/Windows Millennium edition (Windows) : la mémoire tampon vers laquelle pointe *lParam* doit résider dans la mémoire accessible en écriture, même si le message ne modifie pas le tableau.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

