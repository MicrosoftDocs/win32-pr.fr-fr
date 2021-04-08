---
title: Message TVM_SHOWINFOTIP (commctrl. h)
description: Affiche l’info-bulle d’un élément spécifié dans un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ShowInfoTip TreeView.
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- TVM_SHOWINFOTIP les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844362"
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

## <a name="return-value"></a>Valeur retournée

Retourne zéro.

## <a name="remarks"></a>Notes

La plupart des applications n’utilisent pas ce message. Les info-bulles sont affichés automatiquement. Pour plus d’informations, consultez Utilisation de l’arborescence info-bulles dans la vue d’ensemble des [contrôles à propos de Tree-View](tree-view-controls.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





