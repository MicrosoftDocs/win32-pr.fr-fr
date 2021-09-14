---
title: Message TVM_GETCOUNT (commctrl. h)
description: Récupère le nombre d’éléments dans un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TreeView GetCount.
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- TVM_GETCOUNT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_GETCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 870ca0d1e4bf04d054d29d78ab60371863648a8f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115714"
---
# <a name="tvm_getcount-message"></a>TVM \_ GETCOUNT (message)

Récupère le nombre d’éléments dans un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne le nombre d’éléments.

## <a name="remarks"></a>Notes

Le nombre de nœuds retourné par [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) est limité aux valeurs entières. Si vous ajoutez un nœud au-delà de 32767, la macro retourne une valeur négative. Après l’ajout de nœuds 65536, le nombre retourne à zéro. Dans ce cas, le contrôle Tree-View apparaît vide sans barre de défilement.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





