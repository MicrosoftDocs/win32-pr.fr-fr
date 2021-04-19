---
description: Indique si un flash a été déclenché pour le frame capturé.
ms.assetid: CF900CB4-8967-40F3-B60C-867192A641E9
title: Attribut MF_CAPTURE_METADATA_PHOTO_FRAME_FLASH (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff5e9a47c07c8d7a2cec4e7dbf7b34669301122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544759"
---
# <a name="mf_capture_metadata_photo_frame_flash-attribute"></a>\_Attribut Flash de l' \_ \_ \_ image de MÉTADONNÉEs de capture MF \_

Indique si un flash a été déclenché pour le frame capturé.

## <a name="data-type"></a>Type de données

**UINT32**



| Valeur                                                                               | Signification                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>        | Un flash n’a pas été déclenché sur ce frame.<br/>                                                                                                   |
| <dl> <dt>Différent de zéro</dt> </dl> | Un flash a été déclenché sur ce frame.<br/>                                                                                                       |
| <dl> <dt>1</dt> </dl>        | Réservé<br/> Ne vérifiez pas explicitement la valeur 1. Les applications doivent uniquement vérifier les ! = 0 pour indiquer si un flash a été déclenché.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




