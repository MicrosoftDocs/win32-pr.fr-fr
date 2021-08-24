---
title: Message LVM_SETITEMCOUNT (commctrl. h)
description: Force le contrôle List-View à allouer de la mémoire pour le nombre spécifié d’éléments ou définit le nombre virtuel d’éléments dans un contrôle List-View virtuel.
ms.assetid: 5e794c12-ddcb-44fc-b0d2-677352602503
keywords:
- LVM_SETITEMCOUNT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be6b35b38c65663d9811a27341cf10d668a9e045641a8ff0871f6b49fe8bcdbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656279"
---
# <a name="lvm_setitemcount-message"></a>\_Message SETITEMCOUNT LVM

Force le contrôle List-View à allouer de la mémoire pour le nombre spécifié d’éléments ou définit le nombre virtuel d’éléments dans un [contrôle List-View virtuel](list-view-controls-overview.md).

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre d’éléments que le contrôle List-View doit finalement contenir.

</dd> <dt>

*lParam* 
</dt> <dd>

[Version 4,70](common-control-versions.md). Valeurs qui spécifient le comportement du contrôle List View après la réinitialisation du nombre d’éléments. Cette valeur peut être une combinaison des éléments suivants :



| Valeur                                                                                                                                                                                    | Signification                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="LVSICF_NOINVALIDATEALL"></span><span id="lvsicf_noinvalidateall"></span><dl> <dt>**LVSICF \_ NOINVALIDATEALL**</dt> </dl> | Le contrôle de liste n’est pas redessiné à moins que les éléments affectés soient actuellement en vue.<br/>    |
| <span id="LVSICF_NOSCROLL"></span><span id="lvsicf_noscroll"></span><dl> <dt>**LVSICF \_ NOscroll**</dt> </dl>                      | Le contrôle List-View ne modifie pas la position de défilement lorsque le nombre d’éléments change.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

La façon dont la mémoire est allouée dépend de la façon dont le contrôle List-View a été créé. Vous pouvez envoyer ce message explicitement ou utiliser les macros [**ListView \_ SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) ou [**ListView \_ SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) . Pour plus d’informations, consultez [Virtual List-View style](/windows/desktop/Controls/list-view-controls-overview).

Si le contrôle List-View a été créé sans le style [**LVS \_ OWNERDATA**](list-view-window-styles.md) , l’envoi de ce message amène le contrôle à allouer ses structures de données internes pour le nombre spécifié d’éléments. Cela empêche le contrôle d’avoir à allouer les structures de données chaque fois qu’un élément est ajouté.

Si le contrôle d’affichage de liste a été créé avec le style [**LVS \_ OWNERDATA**](list-view-window-styles.md) (un affichage de liste virtuel), l’envoi de ce message définit le nombre virtuel d’éléments que contient le contrôle.

Le paramètre *lParam* est destiné uniquement aux contrôles List-View qui utilisent les styles [**LVS \_ OWNERDATA**](list-view-window-styles.md) et [**LVS \_**](list-view-window-styles.md) ou de [**\_ liste LVS**](list-view-window-styles.md) .

Lorsque l’affichage de liste de contrôle commun est une vue de liste virtualisée ([**LVS \_ OWNERDATA**](list-view-window-styles.md)), il existe une limite d’éléments de 100 millions dans la liste. Dans ce scénario, **LVM \_ SETITEMCOUNT** retourne false s’il a un *wParam* de 100 000 001.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

