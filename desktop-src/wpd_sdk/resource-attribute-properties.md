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
ms.openlocfilehash: 64f4f394fcd91d50f323a8e46a9556daa6a8dbff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522933"
---
# <a name="resource-attribute-properties"></a>Propriétés d’attribut de ressource

Windows Les appareils mobiles prennent en charge les propriétés d’attribut de ressource suivantes.



| Propriété                                    | VarType         | Description                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_clé de \_ ressource d’attribut de ressource wpd \_ \_** | **VT \_ inconnu** | Il s’agit d’un [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) contenant une valeur unique, qui est la clé qui identifie la ressource.                     |
| **\_format d' \_ attribut de ressource wpd \_**        | **\_CLSID VT**   | Valeur GUID qui spécifie le format de la ressource. pour obtenir la liste des formats définis par Windows appareils mobiles, consultez la page [formats d’objet](object-format-guids.md) . |
| **\_ \_ \_ taille totale de l’attribut de ressource wpd \_**   | **\_UI8 VT**     | Taille totale des données de ressource, en octets.                                                                                                                            |



 

## <a name="remarks"></a>Notes

Ces attributs sont retournés par la méthode [**IPortableDeviceResources :: GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[**Propriétés et attributs WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




