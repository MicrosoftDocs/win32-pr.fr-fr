---
title: Message TVM_SETHOT (commctrl. h)
description: Définit l’élément réactif pour un contrôle d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetHot TreeView.
ms.assetid: 5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8
keywords:
- TVM_SETHOT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETHOT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beccd5429267350682a6721cde66cca9316cf438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942696"
---
# <a name="tvm_sethot-message"></a>TVM \_ SETHOT message

\[Destiné à un usage interne ; non recommandé pour une utilisation dans les applications. Ce message n’est peut-être pas pris en charge dans les versions futures de Windows.\]

Définit l’élément réactif pour un contrôle d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetHot TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers le nouvel élément réactif. Si cette valeur est **null**, le contrôle Tree-View est défini sur ne pas avoir d’élément réactif.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="security-considerations"></a>Considérations relatives à la sécurité

L’utilisation de ce message peut compromettre la sécurité de votre programme.

## <a name="remarks"></a>Notes

L' *élément réactif* est l’élément sur lequel pointe la souris. Ce message se présente comme s’il s’agissait de l’élément réactif, même si la souris n’est pas positionnée dessus.

Ce message n’a aucun effet visible si le style [**TV \_ TRACKSELECT**](tree-view-control-window-styles.md) n’est pas défini.

Si elle est réussie, ce message entraîne le redessin de l’élément réactif.

Ce message est ignoré si *lParam* a la **valeur null** et que le contrôle Tree-View effectue le suivi de la souris.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SetHot TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
</dt> </dl>

 

 





