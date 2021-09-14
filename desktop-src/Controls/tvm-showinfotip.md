---
title: Message TVM_SHOWINFOTIP (commctrl. h)
description: Affiche l’info-bulle d’un élément spécifié dans un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ShowInfoTip TreeView.
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- TVM_SHOWINFOTIP les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_SHOWINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76f147253800469a800677a242ff0ab0ccdbdfa4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115557"
---
# <a name="tvm_showinfotip-message"></a>TVM \_ SHOWINFOTIP message

Affiche l’info-bulle d’un élément spécifié dans un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ ShowInfoTip TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Handle de l’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne zéro.

## <a name="remarks"></a>Notes

La plupart des applications n’utilisent pas ce message. Les info-bulles sont affichés automatiquement. Pour plus d’informations, consultez Utilisation de l’arborescence info-bulles dans la vue d’ensemble des [contrôles à propos de Tree-View](tree-view-controls.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





