---
title: Message TVM_SETIMAGELIST (commctrl. h)
description: Définit la liste d’images normale ou d’État pour un contrôle d’arborescence et redessine le contrôle à l’aide des nouvelles images. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetImageList TreeView.
ms.assetid: 1a7bf2f8-c7db-44a8-b234-0ffc498e9000
keywords:
- TVM_SETIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f308cb8a56b2e74a5703af144bac03c271efc95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741556"
---
# <a name="tvm_setimagelist-message"></a>TVM \_ SETIMAGELIST message

Définit la liste d’images normale ou d’État pour un contrôle d’arborescence et redessine le contrôle à l’aide des nouvelles images. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetImageList TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Type de liste d’images à définir. Ce paramètre peut prendre l’une des valeurs suivantes :



| Valeur                                                                                                                                                      | Signification                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <dt>**TVSIL \_ normal**</dt> </dl> | Indique la liste d’images normale, qui contient les images sélectionnées, non sélectionnées et de superposition pour les éléments d’un contrôle d’arborescence.<br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <dt>**État de TVSIL \_**</dt> </dl>    | Indique la liste d’images d’État. Vous pouvez utiliser des images d’État pour indiquer les États des éléments définis par l’application. Une image d’État s’affiche à gauche de l’image sélectionnée ou non sélectionnée d’un élément.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle de la liste d’images. Si *lParam* a la **valeur null**, le message supprime la liste d’images spécifiée du contrôle Tree-View.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle vers la liste d’images précédente, le cas échéant, ou **null** dans le cas contraire.

## <a name="remarks"></a>Notes

Le contrôle Tree-View ne détruit pas la liste d’images spécifiée avec ce message. Votre application doit détruire la liste d’images lorsqu’elle n’est plus nécessaire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ GETIMAGELIST**](tvm-getimagelist.md)
</dt> </dl>

 

 





