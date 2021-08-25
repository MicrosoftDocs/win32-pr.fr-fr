---
title: Message BM_GETIMAGE (winuser. h)
description: Récupère un handle vers l’image (icône ou bitmap) associée au bouton.
ms.assetid: 766ea1b0-418d-41b8-b31d-0fcc58e03893
keywords:
- BM_GETIMAGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- BM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b98ede304499aa97d9129957aa69a0991dee98565ff7827cdad4d0c1a82f19b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921259"
---
# <a name="bm_getimage-message"></a>\_Message GETIMAGE de BM

Récupère un handle vers l’image (icône ou bitmap) associée au bouton.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Type d’image à associer au bouton. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                      | Signification              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**IMAGE \_ bitmap**</dt> </dl> | Bitmap.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**icône d’IMAGE \_**</dt> </dl>       | icône ;<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un handle vers l’image, le cas échéant ; dans le cas contraire, la **valeur est null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_SETIMAGE BM**](bm-setimage.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Boutons](buttons.md)
</dt> </dl>

 

 





