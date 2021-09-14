---
title: Message STM_GETIMAGE (winuser. h)
description: Une application envoie un \_ message STM GETIMAGE pour récupérer un handle de l’image (icône ou bitmap) associé à un contrôle statique.
ms.assetid: eb5fe67a-09be-4c13-89c6-0e2f23e8c081
keywords:
- STM_GETIMAGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- STM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77fe0c3d00a2a957530160a5ce5a21b8a1cf84e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116953"
---
# <a name="stm_getimage-message"></a>\_Message GETIMAGE STM

Une application envoie un message **STM \_ GETIMAGE** pour récupérer un handle de l’image (icône ou bitmap) associé à un contrôle statique.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie le type d’image à récupérer. Ce paramètre peut prendre l’une des valeurs suivantes :



| Valeur                                                                                                                                                                     | Signification                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**IMAGE \_ bitmap**</dt> </dl>                | Pixels.<br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <dt>**curseur d’IMAGE \_**</dt> </dl>                | Mire.<br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <dt>**IMAGE \_ ENHMETAFILE**</dt> </dl> | Métafichier amélioré.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**icône d’IMAGE \_**</dt> </dl>                      | Située.<br/>              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est un handle vers l’image, le cas échéant ; dans le cas contraire, la **valeur est null**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETIMAGE STM**](stm-setimage.md)
</dt> </dl>

 

 





