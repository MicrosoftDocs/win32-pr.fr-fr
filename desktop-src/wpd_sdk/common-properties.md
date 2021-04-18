---
description: Les appareils mobiles Windows (WPD) prennent en charge les propriétés suivantes des paramètres de commande.
ms.assetid: 03eff101-5c36-48ea-9dcd-2c4ee29a2ac6
title: Paramètres de commande (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Command
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7687488c38f95fd6d7e7b69d64ad6ae32631700d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526773"
---
# <a name="command-parameters"></a>Paramètres de commande

Les appareils mobiles Windows (WPD) prennent en charge les propriétés suivantes des paramètres de commande.




| **Propriété**                                            | **VarType**     | **Description**                                                                                                                                                              |
|---------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ informations sur le client \_ commun de la propriété wpd**          | **VT \_ inconnu** | Interface [**IPortableDeviceValues**](iportabledevicevalues.md) que le pilote utilise pour identifier le client.                                                             |
| **\_contexte des \_ \_ informations du client commun \_ \_ de la propriété wpd** | **\_LPWStr VT**  | Contexte spécifié par le pilote qui identifie un client pour toutes les opérations suivantes.                                                                                          |
| **\_catégorie de \_ \_ commande commune \_ de la propriété wpd**            | **\_CLSID VT**   | La partie **GUID** de la valeur **PROPERTYKEY** de la commande.                                                                                                            |
| **\_ID de \_ \_ commande commune \_ de la propriété wpd**                  | **VT \_ UI4**     | Portion d’ID unique persistante (PID) de la valeur **PROPERTYKEY** de la commande.                                                                                          |
| **\_cible de \_ la \_ commande \_ commune de la propriété wpd**              | **\_LPWStr VT**  | Identificateur de l’objet cible.                                                                                                                                                |
| **\_code d' \_ \_ Erreur du pilote commun \_ \_ de la propriété wpd**          | **VT \_ UI4**     | Code d’erreur spécifique au pilote retourné par un pilote WPD.                                                                                                                       |
| **\_valeur courante de la propriété wpd \_ \_ HRESULT**                      | **\_erreur VT**   | Valeur **HRESULT** retournée par un pilote wpd pour une opération particulière.                                                                                                   |
| **\_ID d' \_ \_ objet commun \_ de la propriété wpd**                  | **VT \_ inconnu** | Interface [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de type Variant **VT \_ LPWStr** qui contient une liste d’identificateurs d’objets. |
| **\_ \_ ID communs des propriétés \_ persistantes communes \_ \_ de la propriété wpd**      | **VT \_ inconnu** | Interface [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de type Variant **VT \_ LPWStr** qui contient une liste de PID.               |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs**](properties-and-attributes.md)
</dt> </dl>

 

 




