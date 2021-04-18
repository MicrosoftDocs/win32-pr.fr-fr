---
description: Spécifie que l’encodeur MFT prend en charge la réception des événements MEEncodingParameter lors de la diffusion en continu.
ms.assetid: 8DE04537-641C-4154-9C7F-A7D025CA4C39
title: Attribut MFT_ENCODER_SUPPORTS_CONFIG_EVENT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49c688abc4d372a463115c369e4616babe3bcaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519833"
---
# <a name="mft_encoder_supports_config_event-attribute"></a>L' \_ encodeur MFT \_ prend en charge l' \_ attribut d’événement de configuration \_

Spécifie que l’encodeur MFT prend en charge la réception des événements [MEEncodingParameter](meencodingparameters.md) lors de la diffusion en continu.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Notes

Envoyé par l’encodeur MFT via [**IMFTransform ::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[Applications Windows 8.1 Desktop Apps \| UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Mftransform. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFTransform ::P rocessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
</dt> </dl>

 

 




