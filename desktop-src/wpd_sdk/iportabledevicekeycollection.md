---
description: L’interface IPortableDeviceKeyCollection contient une collection de valeurs PROPERTYKEY. Cette interface peut être récupérée à partir d’une méthode ou, si un nouvel objet est requis, appeler CoCreate avec CLSID \_ PortableDeviceKeyCollection.
ms.assetid: 2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd
title: Interface IPortableDeviceKeyCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0f648020ddb82db2a619f75bb125e94c7679f8dd3061ac282fcc0f911a498a77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839389"
---
# <a name="iportabledevicekeycollection-interface"></a>Interface IPortableDeviceKeyCollection

L’interface **IPortableDeviceKeyCollection** contient une collection de valeurs **PROPERTYKEY** . Cette interface peut être récupérée à partir d’une méthode ou, si un nouvel objet est requis, appeler **CoCreate** avec **CLSID \_ PortableDeviceKeyCollection**.

## <a name="members"></a>Membres

L’interface **IPortableDeviceKeyCollection** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPortableDeviceKeyCollection** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IPortableDeviceKeyCollection** possède ces méthodes.



| Méthode                                                    | Description                                                                         |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Complémentaires**](iportabledevicekeycollection-add.md)           | Ajoute une clé de propriété à la collection.<br/>                                   |
| [**Effacer**](iportabledevicekeycollection-clear.md)       | Supprime tous les éléments de la collection.<br/>                                   |
| [**GetAt**](iportabledevicekeycollection-getat.md)       | Récupère une **PROPERTYKEY** de la collection par index.<br/>                |
| [**GetCount**](iportabledevicekeycollection-getcount.md) | Récupère le nombre de clés de cette collection.<br/>                         |
| [**RemoveAt**](iportabledevicekeycollection-removeat.md) | Supprime l’élément stocké à l’emplacement spécifié par l’index donné.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces de collection**](collection-interfaces.md)
</dt> </dl>

 

