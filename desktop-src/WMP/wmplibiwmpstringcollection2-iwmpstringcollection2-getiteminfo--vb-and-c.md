---
title: Méthode IWMPStringCollection2 getItemInfo
description: La méthode getItemInfo retourne la chaîne correspondant à l’index et au nom d’élément de collection de chaînes spécifiés.
ms.assetid: 4a107e85-9eb7-42be-b1f9-8e9e92e6e509
keywords:
- méthode getItemInfo lecteur Windows Media
- méthode getItemInfo lecteur Windows Media, interface IWMPStringCollection2
- Interface IWMPStringCollection2 lecteur Windows Media, méthode getItemInfo
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4741c4a3ba74b03038974d8b66bc42c23830ebb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540637"
---
# <a name="iwmpstringcollection2getiteminfo-method"></a>IWMPStringCollection2 :: getItemInfo, méthode

La méthode **getItemInfo** retourne la chaîne correspondant à l’index et au nom d’élément de collection de chaînes spécifiés.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String getItemInfo(
  System.Int32 lCollectionIndex,
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPStringCollection2.getItemInfo
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*lCollectionIndex* \[ dans\]
</dt> <dd>

**System. Int32** spécifiant l’index de base zéro de l’élément de collection de chaînes à partir duquel l’attribut doit être obtenu.

</dd> <dt>

*bstrItemName* \[ dans\]
</dt> <dd>

**System. String** qui est le nom de l’attribut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**System. String** qui est le nom de l’élément de collection de chaînes. Pour les attributs dont la valeur sous-jacente est **System. Boolean**, la chaîne « true » ou « false » est retournée.

## <a name="remarks"></a>Notes

Pour récupérer des attributs avec plusieurs valeurs et attributs avec des valeurs complexes, utilisez la méthode **getItemInfoByType** .

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11.<br/>                                                                                    |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPStringCollection2**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2. getItemInfoByType (VB et C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





