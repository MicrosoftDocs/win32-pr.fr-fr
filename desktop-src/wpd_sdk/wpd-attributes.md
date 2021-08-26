---
description: pour Windows 7, Windows appareils mobiles prend en charge les attributs de paramètres suivants pour les méthodes et les événements d’un service d’appareil.
ms.assetid: a7708c60-758a-4fb6-8ef9-074ecdc9cf60
title: Attributs de paramètres (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Parameter
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 8004f4e2f9f7c22d795b6ce4e4cb0affac1b55ecd876c21288c02e226ee14262
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006109"
---
# <a name="parameter-attributes"></a>Attributs de paramètre

pour Windows 7, Windows appareils mobiles prend en charge les attributs de paramètres suivants pour les méthodes et les événements d’un service d’appareil. Ces attributs sont retournés par les méthodes suivantes :

-   [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes)
-   [**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventparameterattributes)




| Attribut                                            | VarType         | Description                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ valeur par défaut de l’attribut du paramètre wpd \_**        | VT \_ *xxxx*      | Valeur par défaut du paramètre.                                                                                                                                                         |
| **\_éléments d' \_ \_ énumération d’attribut de paramètre wpd \_** | **VT \_ inconnu** | Interface [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) qui contient les valeurs d’énumération pour le paramètre.                                   |
| **\_formulaire d' \_ attribut de paramètre wpd \_**                  | **VT \_ UI4**     | Le format des valeurs de paramètre valides est autorisé.                                                                                                                                                 |
| **\_ \_ \_ taille maximale de l’attribut du paramètre wpd \_**             | **\_UI8 VT**     | Taille maximale, en octets, du paramètre.                                                                                                                                               |
| **\_nom d' \_ attribut du paramètre wpd \_**                  | **\_LPWStr VT**  | Chaîne qui spécifie le nom convivial du script d’un paramètre d’événement ou de méthode. Les caractères valides sont alphanumériques \[ a-zA-z0-9 \] et' \_ '.                                                 |
| **\_ordre des \_ attributs du paramètre wpd \_**                 | **VT \_ UI4**     | Index d’ordre de paramètre de base zéro, afin qu’une valeur d’ordre de 0 corresponde au premier paramètre.                                                                                       |
| **\_plage d’attribut de paramètre wpd \_ \_ \_ min.**            | VT \_ *xxxx*      | Valeur maximale d’un paramètre de la plage de formulaire d’attribut de paramètre WPD de formulaire \_ \_ \_ \_ .                                                                                                       |
| **\_plage d’attributs du paramètre wpd \_ \_ \_ Max.**            | VT \_ *xxxx*      | Valeur minimale pour un paramètre de la \_ plage de formulaire d’attribut de paramètre wpd \_ \_ \_ .                                                                                                       |
| **\_étape de \_ plage d’attributs du paramètre wpd \_ \_**           | VT \_ *xxxx*      | Valeur de pas pour un paramètre de la plage de \_ formulaire d’attribut de paramètre wpd \_ \_ \_ .                                                                                                          |
| **\_ \_ expression régulière d’attribut de paramètre wpd \_ \_**   | **\_LPWStr VT**  | Expression régulière qui spécifie des valeurs acceptables pour les paramètres de la forme \_ \_ \_ expression régulière de formulaire d’attribut de paramètre wpd \_ \_ .                                                      |
| **\_type d' \_ utilisation d’attribut de paramètre wpd \_ \_**           | **VT \_ UI4**     | Entier qui spécifie l’utilisation d’un paramètre de méthode, par exemple in/out. Les valeurs valides sont du type d’énumération des [**\_ types d' \_ utilisation \_ de paramètre wpd**](wpd-parameter-usage-types.md) . |
| **\_attribut de paramètre wpd \_ \_ VarType**               | **VT \_ UI4**     | Paramètre VarType.                                                                                                                                                                      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs**](properties-and-attributes.md)
</dt> </dl>

 

 




