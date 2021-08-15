---
title: Message LVM_GETGROUPRECT (commctrl. h)
description: Obtient le rectangle pour un groupe spécifié. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetGroupRect.
ms.assetid: 9441a6c5-11d8-4f52-80dd-1b60befd9b9d
keywords:
- LVM_GETGROUPRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETGROUPRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89340015972799b059e4568b5e87be511b7fc3718e7e7494d1bf46296886f030
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540919"
---
# <a name="lvm_getgrouprect-message"></a>\_Message GETGROUPRECT LVM

Obtient le rectangle pour un groupe spécifié. Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetGroupRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Spécifie le groupe par **iGroupId** (voir structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) pour recevoir des informations sur le groupe spécifié par *wParam*. Le récepteur de messages est chargé de définir les membres de structure avec les informations relatives au groupe spécifié par *wParam*.

Le processus appelant est chargé d’allouer de la mémoire pour la structure. Définissez le membre **supérieur** du [**Rect**](/previous-versions//dd162897(v=vs.85)) sur l’un des indicateurs suivants pour spécifier les coordonnées du rectangle à récupérer.



| Valeur                                                                                                                                                                  | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVGGR_GROUP"></span><span id="lvggr_group"></span><dl> <dt>**\_groupe LVGGR**</dt> </dl>                | Coordonnées de l’ensemble du groupe développé.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="LVGGR_HEADER"></span><span id="lvggr_header"></span><dl> <dt>**\_en-tête LVGGR**</dt> </dl>             | Coordonnées de l’en-tête uniquement (groupe réduit).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="LVGGR_LABEL"></span><span id="lvggr_label"></span><dl> <dt>**\_étiquette LVGGR**</dt> </dl>                | Coordonnées de l’étiquette uniquement.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="LVGGR_SUBSETLINK"></span><span id="lvggr_subsetlink"></span><dl> <dt>**LVGGR \_ SUBSETLINK**</dt> </dl> | Coordonnées du lien du sous-ensemble uniquement (sous-ensemble de balises). Un contrôle List-View peut limiter le nombre d’éléments visibles affichés dans chaque groupe. Un lien est présenté à l’utilisateur pour permettre à l’utilisateur de développer le groupe. Cet indicateur retourne le rectangle englobant du lien du sous-ensemble si le groupe est un sous-ensemble (État du groupe de LVGS \_ sous-ensemble, consultez structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), **État** du membre). Cet indicateur est fourni afin que les applications d’accessibilité puissent localiser le lien.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

