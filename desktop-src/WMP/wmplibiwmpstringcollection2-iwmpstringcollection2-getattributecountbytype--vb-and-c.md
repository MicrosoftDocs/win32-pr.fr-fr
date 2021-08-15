---
title: Méthode IWMPStringCollection2 getAttributeCountByType
description: La méthode getAttributeCountByType retourne le nombre d’attributs associés à l’index de collection de chaînes, au nom d’attribut et à la langue spécifiés.
ms.assetid: 30312039-3676-4322-b6f6-fb86098bf578
keywords:
- Lecteur Windows Media de la méthode getAttributeCountByType
- méthode getAttributeCountByType Lecteur Windows Media, interface IWMPStringCollection2
- Lecteur Windows Media de l’interface IWMPStringCollection2, méthode getAttributeCountByType
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c236d03cad0612d8306b8ccde370136cb9b31acca82e0aa52761ed56fb4b9bb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330913"
---
# <a name="iwmpstringcollection2getattributecountbytype-method"></a>IWMPStringCollection2 :: getAttributeCountByType, méthode

La méthode **getAttributeCountByType** retourne le nombre d’attributs associés à l’index de collection de chaînes, au nom d’attribut et à la langue spécifiés.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 getAttributeCountByType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPStringCollection2.getAttributeCountByType
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*lCollectionIndex* \[ dans\]
</dt> <dd>

**System. Int32** spécifiant l’index de base zéro de l’élément de collection de chaînes à partir duquel l’attribut doit être obtenu.

</dd> <dt>

*bstrType* \[ dans\]
</dt> <dd>

**System. String** qui est le nom de l’attribut.

</dd> <dt>

*bstrLanguage* \[ dans\]
</dt> <dd>

**System. String** qui est le nom de la langue. Si la valeur est définie sur null ou sur une chaîne de longueur nulle (""), la chaîne de paramètres régionaux active est utilisée. Dans le cas contraire, la valeur doit être une chaîne valide du langage RFC 1766, par exemple « en-US ».

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**System. Int32** qui est le nombre.

## <a name="remarks"></a>Remarques

Cette méthode est utilisée pour découvrir le nombre d’attributs correspondant à un nom d’attribut particulier pour un élément **StringCollection** donné. Les numéros d’index peuvent ensuite être passés au quatrième paramètre de la méthode **getItemInfoByType** .

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11.<br/>                                                                                    |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPStringCollection2 (VB et C#)**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2. getItemInfoByType (VB et C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





