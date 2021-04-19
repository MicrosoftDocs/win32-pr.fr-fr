---
description: L’interface IPortableDevicePropVariantCollection contient une collection de valeurs PROPVARIANT indexées du même VARTYPE.
ms.assetid: 41224958-a5a0-4e09-8733-d0ae036f68b9
title: Interface IPortableDevicePropVariantCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 14ba07894c74567487704bb1f63e7242542af313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528068"
---
# <a name="iportabledevicepropvariantcollection-interface"></a>Interface IPortableDevicePropVariantCollection

L’interface **IPortableDevicePropVariantCollection** contient une collection de valeurs **PROPVARIANT** indexées du même VarType. Le VARTYPE du premier élément ajouté à la collection détermine le VARTYPE de la collection. Une tentative d’ajout d’un élément d’un autre VARTYPE peut échouer si la valeur **PROPVARIANT** ne peut pas être modifiée en VarType actuel de la collection. Pour modifier le VARTYPE de la collection, appelez **ChangeType**.

Cette interface peut être récupérée à partir d’une méthode ou, si un nouvel objet est requis, appeler **CoCreate** avec **CLSID \_ PortableDevicePropVariantCollection**.

## <a name="members"></a>Membres

L’interface **IPortableDevicePropVariantCollection** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPortableDevicePropVariantCollection** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IPortableDevicePropVariantCollection** possède ces méthodes.



| Méthode                                                                | Description                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Complémentaires**](iportabledevicepropvariantcollection-add.md)               | Ajoute un élément à la collection.<br/>                                          |
| [**ChangeType**](iportabledevicepropvariantcollection-changetype.md) | Convertit tous les éléments de la collection au VARTYPE spécifié.<br/>           |
| [**Effacé**](iportabledevicepropvariantcollection-clear.md)           | Libère, puis supprime tous les éléments de la collection.<br/>                  |
| [**GetAt**](iportabledevicepropvariantcollection-getat.md)           | Récupère un élément de la collection par un index de base zéro.<br/>             |
| [**GetCount**](iportabledevicepropvariantcollection-getcount.md)     | Récupère le nombre d’éléments de cette collection.<br/>                        |
| [**GetType**](iportabledevicepropvariantcollection-gettype.md)       | Récupère le type de données des éléments de la collection.<br/>                  |
| [**RemoveAt**](iportabledevicepropvariantcollection-removeat.md)     | Supprime l’élément stocké à l’emplacement spécifié par l’index donné.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces de collection**](collection-interfaces.md)
</dt> </dl>

 

