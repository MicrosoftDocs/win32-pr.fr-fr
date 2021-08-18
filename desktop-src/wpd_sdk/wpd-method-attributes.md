---
description: 'pour Windows 7, Windows appareils mobiles prend en charge les attributs suivants pour les méthodes d’un service d’appareil. Ces attributs sont retournés par la méthode IPortableDeviceServiceCapabilities :: GetMethodAttributes.'
ms.assetid: b920e037-7737-4a18-b4f1-5c59e0a857dd
title: Attributs de méthode (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Method
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ac41b4e9c7273c953a9689ce8c3d9f44d32925aded5b36291c45895b872fa9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026336"
---
# <a name="method-attributes"></a>Attributs de méthode

pour Windows 7, Windows appareils mobiles prend en charge les attributs suivants pour les méthodes d’un service d’appareil. Ces attributs sont retournés par la méthode [**IPortableDeviceServiceCapabilities :: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) .




| Attribut                                      | VarType         | Description                                                                                                               |
|------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ accès aux attributs de la méthode wpd \_**             | **\_CLSID VT**   | Accès à la méthode requis.                                                                                               |
| **\_ \_ \_ format associé à l’attribut de méthode wpd \_** | **\_CLSID VT**   | Format associé à la méthode, ou **GUID \_ null** s’il n’existe aucun format associé.                                |
| **nom de l' \_ attribut de méthode wpd \_ \_**               | **\_LPWStr VT**  | Chaîne qui spécifie le nom convivial du script de la méthode. Les caractères valides sont alphanumériques \[ a-zA-z0-9 \] et' \_ '. |
| **\_paramètres d' \_ attribut de méthode wpd \_**         | **VT \_ inconnu** | Interface [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) qui contient les paramètres de la méthode.    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs**](properties-and-attributes.md)
</dt> </dl>

 

 




