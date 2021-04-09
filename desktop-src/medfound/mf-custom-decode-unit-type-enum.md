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
ms.openlocfilehash: 406f6b3f6b93ced212ccf06910b69761ac0dfd9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201991"
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
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




