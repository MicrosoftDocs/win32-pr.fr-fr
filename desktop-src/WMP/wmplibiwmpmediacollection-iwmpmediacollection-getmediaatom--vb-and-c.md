---
title: Méthode IWMPMediaCollection getMediaAtom
description: La méthode getMediaAtom retourne l’index d’un attribut spécifié dans le jeu d’attributs disponibles.
ms.assetid: 01e3d073-677b-4939-96d3-63ae96eaa25d
keywords:
- Lecteur Windows Media de la méthode getMediaAtom
- méthode getMediaAtom Lecteur Windows Media, interface IWMPMediaCollection
- Lecteur Windows Media de l’interface IWMPMediaCollection, méthode getMediaAtom
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getMediaAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08487cf60c351ff4f8e0741209655cb78c30c3f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292527"
---
# <a name="iwmpmediacollectiongetmediaatom-method"></a>IWMPMediaCollection :: getMediaAtom, méthode

La `getMediaAtom` méthode retourne l’index d’un attribut spécifié dans le jeu d’attributs disponibles.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 getMediaAtom(
  System.String bstrItemName
);
```


```VB

Public Function getMediaAtom( _
  ByVal bstrItemName As System.String _
) As System.Int32
Implements IWMPMediaCollection.getMediaAtom
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrItemName* \[ dans\]
</dt> <dd>

**System. String** qui est le nom de l’élément pour lequel l’index doit être récupéré.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

**System. Int32** qui est l’index.

## <a name="remarks"></a>Notes

Le numéro d’index récupéré avec cette méthode peut être passé à **IWMPMedia. getItemInfoByAtom** pour accéder aux valeurs d’attribut. Cette technique est généralement plus efficace lorsque vous utilisez des sélections volumineuses que l’accès à une valeur d’attribut par nom via **IWMPMedia. getItemInfo**.

Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWMPMedia. getItemInfo (VB et C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getItemInfoByAtom (VB et C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMediaCollection (VB et C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





