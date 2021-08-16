---
description: Windows Les appareils mobiles prennent en charge les attributs de propriété suivants.
ms.assetid: 129ee2b8-075c-457a-85ef-658a56eed541
title: Attributs de propriété (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Property
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 85bf37b716349aae164594eeb8085e8c6df9dc5445728bbf7d9222705a9cb8c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843562"
---
# <a name="property-attributes-portabledeviceh"></a>Attributs de propriété (PortableDevice. h)

Windows Les appareils mobiles prennent en charge les attributs de propriété suivants. Ces attributs sont retournés par les méthodes suivantes :

-   [**IPortableDeviceCapabilities::GetFixedPropertyAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)
-   [**IPortableDeviceProperties::GetPropertyAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getpropertyattributes)
-   [**IPortableDeviceServiceCapabilities::GetFormatPropertyAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatpropertyattributes)



| Attribut                                           | VarType         | Description                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **l' \_ attribut de propriété wpd \_ \_ peut \_ Supprimer**           | **VT \_ bool**    | Valeur booléenne qui spécifie si le client peut supprimer la propriété. Pour supprimer une propriété, définissez sa valeur sur VT \_ vide.                                                                                                                                                                                                                                                                   |
| **l' \_ attribut de propriété wpd \_ \_ peut \_ lire**             | **VT \_ bool**    | Valeur booléenne qui spécifie si le client peut lire la propriété.                                                                                                                                                                                                                                                                                                                       |
| **l' \_ attribut de propriété wpd \_ \_ peut \_ écrire**            | **VT \_ bool**    | Valeur booléenne qui spécifie si le client peut modifier la propriété.                                                                                                                                                                                                                                                                                                                     |
| **\_ \_ \_ valeur par défaut de l’attribut de propriété wpd \_**        | VT \_ *xxxx*      | Valeur définie par l’appareil qui spécifie la valeur par défaut d’une propriété. Cela s’applique uniquement aux propriétés accessibles en écriture.                                                                                                                                                                                                                                                               |
| **\_éléments de \_ l' \_ énumération des attributs de propriété wpd \_** | **VT \_ inconnu** | Interface [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) qui contient une collection de valeurs pour une propriété dont l’attribut de **\_ formulaire d' \_ attribut \_ de propriété wpd** est l' **\_ \_ \_ \_ énumération de formulaire d’attribut de propriété wpd**. Le type de données dépend de la propriété en cours d’interrogation.                                                                              |
| **\_attribut de propriété WPD \_ \_ FAST \_ propriété**        | **VT \_ bool**    | Si la valeur est true, cette propriété appartient au groupe de *Propriétés Fast* . Il s’agit des propriétés qui peuvent être récupérées rapidement à partir de l’appareil.                                                                                                                                                                                                                                                        |
| **\_formulaire d' \_ attribut de propriété wpd \_**                  | **VT \_ UI4**     | Valeur énumérée de [**WpdAttributeForm**](wpdattributeform.md) qui spécifie la forme des valeurs valides autorisées pour cette propriété.                                                                                                                                                                                                                                                         |
| **nom de l' \_ attribut de propriété wpd \_ \_**                  | **\_LPWStr VT**  | Chaîne qui spécifie le nom convivial du script de la propriété. Les caractères valides sont alphanumériques \[ a-zA-z0-9 \] et' \_ '.                                                                                                                                                                                                                                                                    |
| **plage d’attributs de la \_ propriété wpd \_ \_ \_ Max**            | VT \_ *xxxx*      | Valeur maximale d’une propriété dont l’attribut de **\_ formulaire d' \_ attribut \_ de propriété wpd** est une plage de formulaire d' **attribut de \_ propriété \_ \_ \_ wpd**. Le type de données peut être n’importe quel type numérique.                                                                                                                                                                                                               |
| **\_plage d’attribut de propriété wpd \_ \_ \_ min**            | VT \_ *xxxx*      | La valeur minimale d’une propriété dont l’attribut de **\_ formulaire d' \_ attribut \_ de propriété wpd** est la plage de formulaire d' **attribut de \_ propriété \_ \_ \_ wpd**. Le type de données peut être n’importe quel type numérique.                                                                                                                                                                                                               |
| **\_étape de \_ plage des attributs \_ \_ de la propriété wpd**           | VT \_ *xxxx*      | La valeur d’étape d’une propriété dont l’attribut de **\_ formulaire d' \_ attribut \_ de propriété wpd** est la plage de formulaire d' **attribut de \_ propriété \_ \_ \_ wpd**. L’étape spécifie le degré de modification d’une propriété de plage. Par exemple, une propriété avec une valeur minimale de 10, une valeur maximale de 20 et une étape de 5 peut avoir les valeurs suivantes : **10**, **15**, **20**. Le type de données peut être n’importe quel type numérique. |
| **\_ \_ \_ expression régulière de l’attribut de propriété wpd \_**   | **\_LPWStr VT**  | Chaîne d’expression régulière qui spécifie des valeurs acceptables pour les propriétés dont le formulaire est une **\_ \_ \_ \_ \_ expression régulière de formulaire d’attribut de propriété wpd**.                                                                                                                                                                                                                                             |
| **\_attribut de propriété wpd \_ \_ VarType**               | **VT \_ UI4**     | Entier qui spécifie le VARTYPE de la propriété, par exemple **VT \_ bool**.                                                                                                                                                                                                                                                                                                              |
| **\_ \_ \_ taille maximale de l’attribut de propriété wpd \_**             | **\_UI8 VT**     | Valeur qui spécifie la taille maximale, en octets, de la valeur de cette propriété.                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés**](properties-and-attributes.md)
</dt> </dl>

 

 




