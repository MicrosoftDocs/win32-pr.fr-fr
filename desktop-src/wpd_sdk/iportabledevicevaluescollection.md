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
ms.openlocfilehash: cd6547a96013b2b83ce9962a62f0837dd01cacac6f3e64adc3b964754c148c5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928379"
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
| [**Effacer**](iportabledevicevaluescollection-clear.md)       | Libère tous les éléments de la collection.<br/>                                  |
| [**GetAt**](iportabledevicevaluescollection-getat.md)       | Récupère un élément de la collection par un index de base zéro.<br/>             |
| [**GetCount**](iportabledevicevaluescollection-getcount.md) | Récupère le nombre d’éléments dans la collection.<br/>                         |
| [**RemoveAt**](iportabledevicevaluescollection-removeat.md) | Supprime l’élément stocké à l’emplacement spécifié par l’index donné.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces de collection**](collection-interfaces.md)
</dt> </dl>

 

