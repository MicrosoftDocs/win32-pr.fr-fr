---
title: Méthode IWMPMedia getItemInfoByAtom
description: La méthode getItemInfoByAtom retourne la valeur de l’attribut avec le numéro d’index spécifié.
ms.assetid: d9a4b737-add1-4bbd-8e03-e58f45d65a62
keywords:
- Lecteur Windows Media de la méthode getItemInfoByAtom
- méthode getItemInfoByAtom Lecteur Windows Media, interface IWMPMedia
- Lecteur Windows Media de l’interface IWMPMedia, méthode getItemInfoByAtom
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfoByAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72a8820618b39418aa7be82faeef15a372e0e0f90c0db025e99c55be49d8c13e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115692"
---
# <a name="iwmpmediagetiteminfobyatom-method"></a>IWMPMedia :: getItemInfoByAtom, méthode

La méthode **getItemInfoByAtom** retourne la valeur de l’attribut avec le numéro d’index spécifié.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String getItemInfoByAtom(
  System.Int32 lAtom
);
```


```VB

Public Function getItemInfoByAtom( _
  ByVal lAtom As System.Int32 _
) As System.String
Implements IWMPMedia.getItemInfoByAtom
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*lAtom* \[ dans\]
</dt> <dd>

**System. Int32** qui spécifie l’index auquel l’attribut demandé réside dans le jeu d’attributs disponibles.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**System. String** qui est la valeur de l’attribut.

## <a name="remarks"></a>Remarques

Cette méthode peut être utilisée pour récupérer des métadonnées pour un élément multimédia spécifique à l’aide d’un numéro d’index d’attribut. La propriété **attributeCount** peut être utilisée pour déterminer le nombre d’attributs disponibles pour l’élément multimédia.

La méthode **getMediaAtom** de l’interface **IWMPMediaCollection** peut également être utilisée pour récupérer l’index d’un attribut particulier. Cette technique est généralement plus efficace que les méthodes **getItemInfo** ou **getItemInfoByType** lorsque vous utilisez des sélections volumineuses.

Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. attributeCount (VB et C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getItemInfo (VB et C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. setItemInfo (VB et C#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB et C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection. getMediaAtom (VB et C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)
</dt> </dl>

 

 





