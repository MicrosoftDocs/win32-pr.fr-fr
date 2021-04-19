---
title: Méthode IWMPMedia3 getAttributeCountByType
description: La méthode getAttributeCountByType retourne le nombre d’attributs associés au type d’attribut spécifié.
ms.assetid: d692635f-f9f1-4d8e-a9c5-9d7fa84f41bd
keywords:
- méthode getAttributeCountByType lecteur Windows Media
- méthode getAttributeCountByType lecteur Windows Media, interface IWMPMedia3
- Interface IWMPMedia3 lecteur Windows Media, méthode getAttributeCountByType
topic_type:
- apiref
api_name:
- IWMPMedia3.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49505f9e9df8778cc2c17ba062da6700b9b8aec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539537"
---
# <a name="iwmpmedia3getattributecountbytype-method"></a>IWMPMedia3 :: getAttributeCountByType, méthode

La méthode **getAttributeCountByType** retourne le nombre d’attributs associés au type d’attribut spécifié.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 getAttributeCountByType(
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPMedia3.getAttributeCountByType
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrType* \[ dans\]
</dt> <dd>

**System. String** qui est le type d’attribut.

</dd> <dt>

*bstrLanguage* \[ dans\]
</dt> <dd>

**System. String** qui est le langage. Si la valeur est définie sur null ou sur une chaîne de longueur nulle (""), la chaîne de paramètres régionaux active est utilisée. Dans le cas contraire, la valeur doit être une chaîne valide du langage RFC 1766, par exemple « en-US ».

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**System. Int32** qui est le nombre d’attributs associés au type.

## <a name="remarks"></a>Notes

Cette méthode est utilisée pour découvrir le nombre d’attributs correspondant à un nom d’attribut particulier pour un élément multimédia donné. Les numéros d’index peuvent ensuite être passés à la méthode **getItemInfoByType** . Cela est utile, par exemple, lorsqu’un élément multimédia a été catégorisé sous plusieurs genres.

Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPMedia3 (VB et C#)**](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB et C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





