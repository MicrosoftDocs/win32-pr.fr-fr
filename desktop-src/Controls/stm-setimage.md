---
title: Message STM_SETIMAGE (winuser. h)
description: Une application envoie un \_ message STM SETIMAGE pour associer une nouvelle image à un contrôle statique.
ms.assetid: d3e7c5d4-f621-40f6-9558-7fb699e8b489
keywords:
- STM_SETIMAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- STM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27c4f9c216d2e987727a1e2fa9bc6de12a823d52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941797"
---
# <a name="stm_setimage-message"></a>\_Message SETIMAGE STM

Une application envoie un message **STM \_ SETIMAGE** pour associer une nouvelle image à un contrôle statique.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie le type d’image à associer au contrôle statique. Ce paramètre peut prendre l’une des valeurs suivantes :



| Valeur                                                                                                                                                                     | Signification                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**IMAGE \_ bitmap**</dt> </dl>                | Pixels.<br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <dt>**curseur d’IMAGE \_**</dt> </dl>                | Mire.<br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <dt>**IMAGE \_ ENHMETAFILE**</dt> </dl> | Métafichier amélioré.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**icône d’IMAGE \_**</dt> </dl>                      | Située.<br/>              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle de l’image à associer au contrôle statique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un handle vers l’image précédemment associée au contrôle statique, le cas échéant ; dans le cas contraire, la **valeur est null**.

## <a name="remarks"></a>Notes

Pour associer une image à un contrôle statique, le contrôle doit avoir le style approprié. Le tableau suivant indique le style requis pour chaque type d’image.



| Type d’image         | Style de contrôle statique |
|--------------------|----------------------|
| IMAGE \_ bitmap      | \_bitmap SS           |
| curseur d’IMAGE \_      | \_icône SS             |
| IMAGE \_ ENHMETAFILE | \_ENHMETAFILE SS      |
| icône d’IMAGE \_        | \_icône SS             |



 

> [!IMPORTANT]
>
> Dans la version 6 des contrôles Microsoft Win32, une image bitmap transmise à un contrôle statique à l’aide du message **\_ SETIMAGE STM** était la même bitmap que celle retournée par un message **\_ SETIMAGE STM** suivant. Le client est chargé de supprimer toute bitmap envoyée à un contrôle statique.
>
> Avec Windows XP, si la bitmap transmise dans le message **STM \_ SETIMAGE** contient des pixels avec une valeur alpha différente de zéro, le contrôle statique prend une copie de l’image bitmap. Cette bitmap copiée est retournée par le prochain message **\_ SETIMAGE STM** . Le code client peut suivre indépendamment les bitmaps transmises au contrôle statique, mais s’il ne vérifie pas et ne libère pas les bitmaps retournées par les messages **STM \_ SETIMAGE** , les bitmaps sont divulguées.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**STM \_ GETIMAGE**](stm-getimage.md)
</dt> </dl>

 

 





