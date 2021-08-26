---
description: Représente le type de la source du frame.
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: Attribut MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce2e7f90f4e5f23e99bac8e532455fac1309cc0e20177c5800d85f4580e20a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013189"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a>\_Attribut de \_ \_ types FRAMESOURCE \_ de l’attribut DEVICESTREAM MF

Représente le type de la source du frame.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Cette valeur de cet attribut doit être un masque de masque d’une ou de plusieurs valeurs de l’énumération [**MFFrameSourceTypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) . Pour prendre en charge la compatibilité descendante, lorsque cet attribut n’est pas défini pour un type de média, il est supposé avoir la valeur **MFFrameSourceTypes :: Color**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1607 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




