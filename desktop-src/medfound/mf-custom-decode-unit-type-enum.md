---
description: Spécifie le type d’unité contenu dans un IMFSample dans une \_ collection de ForwardedDecodeUnits MFSampleExtension.
ms.assetid: B74890ED-9586-475B-8C77-457ECB893980
title: Énumération MF_CUSTOM_DECODE_UNIT_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_CUSTOM_DECODE_UNIT_TYPE
api_type:
- HeaderDef
api_location:
- mfapi.h
ms.openlocfilehash: 97dd001cfb83f6ffec07035b77558fee591599b087e30dd3b819963db1b70405
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104985"
---
# <a name="mf_custom_decode_unit_type-enumeration"></a>\_ \_ \_ Énumération de type d’unité de décodage personnalisé MF \_

Spécifie le type d’unité contenu dans un [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) dans une collection de [ \_ ForwardedDecodeUnits MFSampleExtension](mfsampleextension-forwardeddecodeunits.md) .

## <a name="members"></a>Membres



| Membre                    | Description                                                             | Valeur |
|---------------------------|-------------------------------------------------------------------------|-------|
| **\_unité de décodage MF \_ \_ nal** | Le type d’unité est l’unité de la couche d’abstraction de réseau (NALU). <br/>     | 0     |
| **\_SEI unité de décodage MF \_ \_** | Le type d’unité est informations supplémentaires sur l’amélioration (SEI).<br/> | 1     |



## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




