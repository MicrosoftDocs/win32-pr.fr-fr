---
title: Message TVM_SETAUTOSCROLLINFO (commctrl. h)
description: Définit les informations utilisées pour déterminer les caractéristiques de défilement automatique. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetAutoScrollInfo TreeView.
ms.assetid: de55933f-1caa-4193-84de-0486c41e8f1f
keywords:
- TVM_SETAUTOSCROLLINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETAUTOSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa1f7920d2ec8c443b2ec5f1ff9189c22c5f21e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511139"
---
# <a name="tvm_setautoscrollinfo-message"></a>TVM \_ SETAUTOSCROLLINFO message

Définit les informations utilisées pour déterminer les caractéristiques de défilement automatique. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetAutoScrollInfo TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Spécifie les pixels par seconde. Le décalage à faire défiler est divisé par le *wParam* pour déterminer la durée totale du défilement automatique.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Spécifie l’intervalle de redessination. Redessinez à chaque intervalle de elasped jusqu’à ce que l’élément fasse l’objet d’un défilement. Avec *wParam* donné, l’emplacement de l’élément est calculé et un redessin se produit. Définissez cette valeur pour créer un défilement fluide.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true**.

## <a name="remarks"></a>Notes

Les informations de défilement automatique sont utilisées pour faire défiler un élément non visible dans l’affichage. Le contrôle doit avoir le style étendu [**TV \_ ex \_ AUTOHSCROLL**](tree-view-control-window-extended-styles.md) . Pour plus d’informations sur les styles étendus, consultez Tree-View les styles étendus de contrôle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





