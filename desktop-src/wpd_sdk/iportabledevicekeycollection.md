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
ms.openlocfilehash: c246fabe7ced72a5aad6d30101df8035a159a923
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404445"
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
| [**Effacé**](iportabledevicekeycollection-clear.md)       | Supprime tous les éléments de la collection.<br/>                                   |
| [**GetAt**](iportabledevicekeycollection-getat.md)       | Récupère une **PROPERTYKEY** de la collection par index.<br/>                |
| [**GetCount**](iportabledevicekeycollection-getcount.md) | Récupère le nombre de clés de cette collection.<br/>                         |
| [**RemoveAt**](iportabledevicekeycollection-removeat.md) | Supprime l’élément stocké à l’emplacement spécifié par l’index donné.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces de collection**](collection-interfaces.md)
</dt> </dl>

 

