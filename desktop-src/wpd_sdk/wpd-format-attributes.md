---
description: 'pour Windows 7, Windows appareils mobiles prend en charge les attributs suivants pour les formats sur un service d’appareil. Ces attributs sont retournés par la méthode IPortableDeviceServiceCapabilities :: GetFormatAttributes.'
ms.assetid: 53282e01-54da-4adf-8a09-2086d6398275
title: Attributs de format (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Format
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 559f731ec7d61007b05e4625ff67488b5ef482fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195795"
---
# <a name="format-attributes"></a>Attributs de format

pour Windows 7, Windows appareils mobiles prend en charge les attributs suivants pour les formats sur un service d’appareil. Ces attributs sont retournés par la méthode [**IPortableDeviceServiceCapabilities :: GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) .




| **Attribut**                        | **VarType**    | **Description**                                                                                                           |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------|
| **\_attribut de format wpd \_ \_ MimeType** | **\_LPWStr VT** | Type MIME de format.                                                                                                     |
| **nom de l' \_ attribut de format wpd \_ \_**     | **\_LPWStr VT** | Chaîne qui spécifie le nom convivial du format du script. Les caractères valides sont alphanumériques \[ a-zA-z0-9 \] et' \_ '. |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs**](properties-and-attributes.md)
</dt> </dl>

 

 




