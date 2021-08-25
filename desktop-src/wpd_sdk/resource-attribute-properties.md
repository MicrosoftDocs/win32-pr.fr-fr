---
description: Windows Les appareils mobiles prennent en charge les propriétés d’attribut de ressource suivantes.
ms.assetid: 9b90db8a-e833-48cf-b484-70ac5ac32a76
title: Propriétés d’attribut de ressource (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 956cd349089afb00a1350bf32e8f06acd5747599f6d5a731e4bf5d8dd1c96295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928069"
---
# <a name="resource-attribute-properties"></a>Propriétés d’attribut de ressource

Windows Les appareils mobiles prennent en charge les propriétés d’attribut de ressource suivantes.



| Propriété                                    | VarType         | Description                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_clé de \_ ressource d’attribut de ressource wpd \_ \_** | **VT \_ inconnu** | Il s’agit d’un [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) contenant une valeur unique, qui est la clé qui identifie la ressource.                     |
| **\_format d' \_ attribut de ressource wpd \_**        | **\_CLSID VT**   | Valeur GUID qui spécifie le format de la ressource. pour obtenir la liste des formats définis par Windows appareils mobiles, consultez la page [formats d’objet](object-format-guids.md) . |
| **\_ \_ \_ taille totale de l’attribut de ressource wpd \_**   | **\_UI8 VT**     | Taille totale des données de ressource, en octets.                                                                                                                            |



 

## <a name="remarks"></a>Remarques

Ces attributs sont retournés par la méthode [**IPortableDeviceResources :: GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[**Propriétés et attributs WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




