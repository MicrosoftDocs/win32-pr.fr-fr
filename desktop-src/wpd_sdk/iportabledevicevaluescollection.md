---
description: L’interface IPortableDeviceValuesCollection contient une collection d’interfaces IPortableDeviceValues indexées de base zéro.
ms.assetid: 8bce9d27-f240-41ec-acf4-fefccdd95e9f
title: Interface IPortableDeviceValuesCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cebe15dc9a4f4347eb58563e9b43240464565a4c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522964"
---
# <a name="iportabledevicevaluescollection-interface"></a>Interface IPortableDeviceValuesCollection

L’interface **IPortableDeviceValuesCollection** contient une collection d’interfaces **IPortableDeviceValues** indexées de base zéro. Cette interface peut être récupérée à partir d’une méthode ou, si un nouvel objet est requis, appeler **CoCreate** avec **CLSID \_ PortableDeviceValuesCollection**.

## <a name="members"></a>Membres

L’interface **IPortableDeviceValuesCollection** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPortableDeviceValuesCollection** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IPortableDeviceValuesCollection** possède ces méthodes.



| Méthode                                                       | Description                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Complémentaires**](iportabledevicevaluescollection-add.md)           | Ajoute un élément à la collection<br/>                                           |
| [**Effacé**](iportabledevicevaluescollection-clear.md)       | Libère tous les éléments de la collection.<br/>                                  |
| [**GetAt**](iportabledevicevaluescollection-getat.md)       | Récupère un élément de la collection par un index de base zéro.<br/>             |
| [**GetCount**](iportabledevicevaluescollection-getcount.md) | Récupère le nombre d’éléments dans la collection.<br/>                         |
| [**RemoveAt**](iportabledevicevaluescollection-removeat.md) | Supprime l’élément stocké à l’emplacement spécifié par l’index donné.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces de collection**](collection-interfaces.md)
</dt> </dl>

 

