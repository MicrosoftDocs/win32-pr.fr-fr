---
title: Message LVM_SETITEMCOUNT (commctrl. h)
description: Force le contrôle List-View à allouer de la mémoire pour le nombre spécifié d’éléments ou définit le nombre virtuel d’éléments dans un contrôle List-View virtuel.
ms.assetid: 5e794c12-ddcb-44fc-b0d2-677352602503
keywords:
- LVM_SETITEMCOUNT les contrôles de message Windows
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
ms.openlocfilehash: 9e390e7ae5913053f91f7f2f8d197af1cf4b7a40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103228"
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

## <a name="remarks"></a>Notes

La façon dont la mémoire est allouée dépend de la façon dont le contrôle List-View a été créé. Vous pouvez envoyer ce message explicitement ou utiliser les macros [**ListView \_ SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) ou [**ListView \_ SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) . Pour plus d’informations, consultez [Virtual List-View style](/windows/desktop/Controls/list-view-controls-overview).

Si le contrôle List-View a été créé sans le style [**LVS \_ OWNERDATA**](list-view-window-styles.md) , l’envoi de ce message amène le contrôle à allouer ses structures de données internes pour le nombre spécifié d’éléments. Cela empêche le contrôle d’avoir à allouer les structures de données chaque fois qu’un élément est ajouté.

Si le contrôle d’affichage de liste a été créé avec le style [**LVS \_ OWNERDATA**](list-view-window-styles.md) (un affichage de liste virtuel), l’envoi de ce message définit le nombre virtuel d’éléments que contient le contrôle.

Le paramètre *lParam* est destiné uniquement aux contrôles List-View qui utilisent les styles [**LVS \_ OWNERDATA**](list-view-window-styles.md) et [**LVS \_**](list-view-window-styles.md) ou de [**\_ liste LVS**](list-view-window-styles.md) .

Lorsque l’affichage de liste de contrôle commun est une vue de liste virtualisée ([**LVS \_ OWNERDATA**](list-view-window-styles.md)), il existe une limite d’éléments de 100 millions dans la liste. Dans ce scénario, **LVM \_ SETITEMCOUNT** retourne false s’il a un *wParam* de 100 000 001.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

