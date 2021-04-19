---
description: Représente le type de la source du frame.
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: Attribut MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8823a828a81290fe3b039c8959d694c62331622f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524115"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a>\_Attribut de \_ \_ types FRAMESOURCE \_ de l’attribut DEVICESTREAM MF

Représente le type de la source du frame.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Cette valeur de cet attribut doit être un masque de masque d’une ou de plusieurs valeurs de l’énumération [**MFFrameSourceTypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) . Pour prendre en charge la compatibilité descendante, lorsque cet attribut n’est pas défini pour un type de média, il est supposé avoir la valeur **MFFrameSourceTypes :: Color**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1607 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




