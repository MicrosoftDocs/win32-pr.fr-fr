---
title: Message STM_GETIMAGE (winuser. h)
description: Une application envoie un \_ message STM GETIMAGE pour récupérer un handle de l’image (icône ou bitmap) associé à un contrôle statique.
ms.assetid: eb5fe67a-09be-4c13-89c6-0e2f23e8c081
keywords:
- STM_GETIMAGE les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032413"
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

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un handle vers l’image, le cas échéant ; dans le cas contraire, la **valeur est null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETIMAGE STM**](stm-setimage.md)
</dt> </dl>

 

 





