---
title: Méthode d’élément IWMPStringCollection
description: La méthode Item retourne la chaîne à l’index spécifié.
ms.assetid: 77546cb2-eda5-4bb8-97b9-55270461815f
keywords:
- méthode Item Lecteur Windows Media
- méthode Item Lecteur Windows Media, interface IWMPStringCollection
- Lecteur Windows Media de l’interface IWMPStringCollection, méthode Item
topic_type:
- apiref
api_name:
- IWMPStringCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47928502dce9ed4deb12461763a499de5d962aa1303b4c9cc5eacb02c7619da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568425"
---
# <a name="iwmpstringcollectionitem-method"></a>IWMPStringCollection :: Item, méthode

La méthode **Item** retourne la chaîne à l’index spécifié.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPStringCollection.Item
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*Lindex* \[ dans\]
</dt> <dd>

**System. Int32** qui est l’index.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**System. String** qui est la chaîne à l’index spécifié.

## <a name="remarks"></a>Remarques

L’interface **IWMPStringCollection** est utilisée pour récupérer l’ensemble de valeurs disponibles pour un attribut. Par exemple, la méthode **IWMPMediaCollection. getAttributeStringCollection** peut être utilisée pour récupérer une interface **IWMPStringCollection** représentant toutes les valeurs de l’attribut genre dans le type de média audio. La méthode **Item** peut ensuite être utilisée pour itérer au sein de toutes les valeurs possibles de l’attribut genre.

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWMPMediaCollection. getAttributeStringCollection (VB et C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[**Interface IWMPStringCollection (VB et C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





