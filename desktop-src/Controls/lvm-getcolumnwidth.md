---
title: Message LVM_GETCOLUMNWIDTH (commctrl. h)
description: Obtient la largeur d’une colonne en mode rapport ou liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetColumnWidth.
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- LVM_GETCOLUMNWIDTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0577e7cb2a589c432d4b5ca62f640de61d67dc75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102900"
---
# <a name="lvm_getcolumnwidth-message"></a>\_Message GETCOLUMNWIDTH LVM

Obtient la largeur d’une colonne en mode rapport ou liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de la colonne. Ce paramètre est ignoré en mode liste.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la largeur de colonne en cas de réussite, ou zéro dans le cas contraire. Si ce message est envoyé à un contrôle List-View avec le style de [**\_ rapport LVS**](list-view-window-styles.md) et que la colonne spécifiée n’existe pas, la valeur de retour n’est pas définie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





