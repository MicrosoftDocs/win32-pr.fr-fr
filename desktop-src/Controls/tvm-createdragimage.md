---
title: Message TVM_CREATEDRAGIMAGE (commctrl. h)
description: Crée une image bitmap de glissement pour l’élément spécifié dans un contrôle Tree-View.
ms.assetid: fbe97921-c9d3-473c-933c-d6bc0599e24d
keywords:
- TVM_CREATEDRAGIMAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 189b37affc6a4382541faea13199cacfcb9b7df5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103903"
---
# <a name="tvm_createdragimage-message"></a>TVM \_ CREATEDRAGIMAGE message

Crée une image bitmap de glissement pour l’élément spécifié dans un contrôle Tree-View. Le message crée également une liste d’images pour l’image bitmap et ajoute l’image bitmap à la liste d’images. Une application peut afficher l’image lors du déplacement de l’élément à l’aide des fonctions de la liste d’images. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ CreateDragImage TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Handle de l’élément qui reçoit la nouvelle bitmap de glissement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle de la liste d’images à laquelle la bitmap glissante a été ajoutée en cas de réussite, ou **null** dans le cas contraire.

## <a name="remarks"></a>Notes

Si vous créez un contrôle Tree-View sans liste d’images associée, vous ne pouvez pas utiliser le message **TVM \_ CREATEDRAGIMAGE** pour créer l’image à afficher pendant une opération glisser. Vous devez implémenter votre propre méthode de création d’un curseur de glissement.

Votre application est responsable de la destruction de la liste d’images lorsqu’elle n’est plus nécessaire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





