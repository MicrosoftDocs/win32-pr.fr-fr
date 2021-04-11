---
title: Message LVM_GETNEXTITEMINDEX (commctrl. h)
description: Récupère l’index d’un élément d’un contrôle List View spécifié qui correspond aux propriétés et à la relation spécifiées avec un autre élément. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetNextItemIndex.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getnextitemindex.htm
keywords:
- LVM_GETNEXTITEMINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETNEXTITEMINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cfc393aee4f275e941a04bb3f23ee4c2c3ac529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105499"
---
# <a name="lvm_getnextitemindex-message"></a>\_Message GETNEXTITEMINDEX LVM

Récupère l’index d’un élément d’un contrôle List View spécifié qui correspond aux propriétés et à la relation spécifiées avec un autre élément. Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetNextItemIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnextitemindex) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ in, out\]
</dt> <dd>

Pointeur vers la structure [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) pour l’élément sur lequel commencer la recherche, ou-1 pour rechercher le premier élément qui correspond aux indicateurs spécifiés. Le processus appelant est responsable de l’allocation de cette structure et de la définition de ses membres.

</dd> <dt>

*lParam* 
</dt> <dd>

Spécifie la relation à l’élément listé dans le paramètre *wParam*. Il peut s’agir d’une des valeurs suivantes ou d’une combinaison des valeurs suivantes :



| Valeur                                                                                                                                                                                                                                                             | Signification                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>Effectue une recherche par index.</dt> </dl>                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_ALL"></span><span id="_______________lvni_all"></span><dl> <dt> **LVNI \_ tout**</dt><dt></dt> </dl>                               | Recherche un élément suivant par index, la valeur par défaut.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt></dt><dt>Effectue une recherche par relation physique avec l’index de l’élément où la recherche doit commencer.</dt> </dl>                                         |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_ABOVE"></span><span id="_______________lvni_above"></span><dl> <dt> **LVNI \_ ci-dessus**</dt><dt></dt> </dl>                         | Recherche un élément qui se trouve au-dessus de l’élément spécifié.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_BELOW"></span><span id="_______________lvni_below"></span><dl> <dt> **LVNI \_ ci-dessous**</dt><dt></dt> </dl>                         | Recherche un élément qui se trouve sous l’élément spécifié.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_TOLEFT"></span><span id="_______________lvni_toleft"></span><dl> <dt> **LVNI \_ VersGauche**</dt><dt></dt> </dl>                      | Recherche un élément à gauche de l’élément spécifié.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="_______________LVNI_PREVIOUS"></span><span id="_______________lvni_previous"></span><dl> <dt> **LVNI \_ précédent**</dt><dt></dt> </dl>                | **Windows Vista et versions ultérieures :** Recherche un élément qui est trié avant l’élément spécifié dans *wParam*. L' \_ indicateur précédent LVNI n’est pas directionnel (LVNI \_ ci-dessus trouvera l’élément positionné ci-dessus, tandis que LVNI \_ précédent trouvera l’élément commandé avant.) L' \_ indicateur précédent LVNI inverse fondamentalement la logique de la recherche effectuée par les messages LVM \_ GETNEXTITEM ou LVM \_ GETNEXTITEMINDEX.<br/> |
| <span id="_______________LVNI_TORIGHT"></span><span id="_______________lvni_toright"></span><dl> <dt> **LVNI \_ VersDroite**</dt><dt></dt> </dl>                   | Recherche un élément à droite de l’élément spécifié.<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="_______________LVNI_DIRECTIONMASK"></span><span id="_______________lvni_directionmask"></span><dl> <dt> **LVNI \_ DIRECTIONMASK**</dt><dt></dt> </dl> | **Windows Vista et versions ultérieures :** Un masque d’indicateur directionnel avec la valeur comme suit : LVNI \_ ci-dessus \| LVNI \_ sous \| LVNI \_ VersGauche \| LVNI \_ TORIGHT.<br/>                                                                                                                                                                                                                                                               |
| <dl> <dt></dt><dt>L’état de l’élément à rechercher peut être spécifié avec une ou plusieurs des valeurs suivantes :</dt> </dl>                                |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_CUT"></span><span id="_______________lvni_cut"></span><dl> <dt> **LVNI \_ couper**</dt><dt></dt> </dl>                               | L’indicateur d’état [**de \_ coupure Lvis**](list-view-item-states.md) est défini pour l’élément.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_DROPHILITED"></span><span id="_______________lvni_drophilited"></span><dl> <dt> **LVNI \_ DROPHILITED**</dt><dt></dt> </dl>       | L’indicateur d’état [**Lvis \_ DROPHILITED**](list-view-item-states.md) est défini pour l’élément<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="_______________LVNI_FOCUSED"></span><span id="_______________lvni_focused"></span><dl> <dt> **LVNI \_ concentré**</dt><dt></dt> </dl>                   | L’indicateur d’état [**\_ focus Lvis**](list-view-item-states.md) est défini pour l’élément.<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="_______________LVNI_SELECTED"></span><span id="_______________lvni_selected"></span><dl> <dt> **LVNI \_ sélectionné**</dt><dt></dt> </dl>                | L’indicateur d’état [**\_ sélectionné Lvis**](list-view-item-states.md) est défini pour l’élément.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="_______________LVNI_STATEMASK"></span><span id="_______________lvni_statemask"></span><dl> <dt> **LVNI \_ STATEMASK**</dt><dt></dt> </dl>             | **Windows Vista et versions ultérieures :** Un masque d’indicateur d’État avec la valeur comme suit : LVNI \_ Focused \| LVNI \_ \| LVNI \_ Cut \| LVNI \_ DROPHILITED.<br/>                                                                                                                                                                                                                                                               |
| <dl> <dt></dt><dt>Recherche par apparence d’éléments ou par groupe.</dt> </dl>                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_VISIBLEORDER"></span><span id="_______________lvni_visibleorder"></span><dl> <dt> **LVNI \_ VISIBLEORDER**</dt><dt></dt> </dl>    | **Windows Vista et versions ultérieures :** Rechercher dans l’ordre visible.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_VISIBLEONLY"></span><span id="_______________lvni_visibleonly"></span><dl> <dt> **LVNI \_ VISIBLEONLY**</dt><dt></dt> </dl>       | **Windows Vista et versions ultérieures :** Recherchez les éléments visibles.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_SAMEGROUPONLY"></span><span id="_______________lvni_samegrouponly"></span><dl> <dt> **LVNI \_ SAMEGROUPONLY**</dt><dt></dt> </dl> | **Windows Vista et versions ultérieures :** Rechercher dans le groupe actuel.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt></dt><dt>Si tous les indicateurs d’état spécifiés ne sont pas définis pour un élément, la recherche se poursuit avec l’élément suivant.</dt> </dl>                          |                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Notez que les indicateurs suivants, à utiliser uniquement avec Windows Vista, s’excluent mutuellement de tous les autres indicateurs en cours d’utilisation : LVNI \_ Previous, LVNI \_ VISIBLEONLY, LVNI \_ SAMEGROUPONLY, LVNI \_ VISIBLEORDER, LVNI \_ DIRECTIONMASK et LVNI \_ STATEMASK.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETNEXTITEM LVM**](lvm-getnextitem.md)
</dt> </dl>

 

 





