---
title: Méthode IWMPMediaCollection2 getStringCollectionByQuery
description: La méthode getStringCollectionByQuery retourne une interface IWMPStringCollection qui fournit l’accès à l’ensemble de toutes les valeurs de chaîne pour un attribut spécifié qui correspondent aux conditions de la requête.
ms.assetid: 2d3b29af-0b6c-4405-8334-9a47a30ff6de
keywords:
- méthode getStringCollectionByQuery lecteur Windows Media
- méthode getStringCollectionByQuery lecteur Windows Media, interface IWMPMediaCollection2
- Interface IWMPMediaCollection2 lecteur Windows Media, méthode getStringCollectionByQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getStringCollectionByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322781bc9ddec3e6f8d74d7229f16ce38e519f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535254"
---
# <a name="iwmpmediacollection2getstringcollectionbyquery-method"></a>IWMPMediaCollection2 :: getStringCollectionByQuery, méthode

La `getStringCollectionByQuery` méthode retourne une interface **IWMPStringCollection** qui fournit l’accès à l’ensemble de toutes les valeurs de chaîne pour un attribut spécifié qui correspondent aux conditions de la requête.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPStringCollection getStringCollectionByQuery(
  System.String bstrAttribute,
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getStringCollectionByQuery( _
  ByVal bstrAttribute As System.String, _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPStringCollection
Implements IWMPMediaCollection2.getStringCollectionByQuery
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrAttribute* \[ dans\]
</dt> <dd>

**System. String** qui est le nom de l’attribut.

</dd> <dt>

*pQuery* \[ dans\]
</dt> <dd>

Interface **wmplib. IWMPQuery** qui correspond à la requête qui définit les conditions utilisées pour récupérer la collection de chaînes.

</dd> <dt>

*bstrMediaType* \[ dans\]
</dt> <dd>

**System. String** qui est le type de média. Doit contenir l’une des valeurs suivantes : « audio », « Video », « photo », « playlist » ou « other ».

</dd> <dt>

*bstrSortAttribute* \[ dans\]
</dt> <dd>

**System. String** qui est le nom d’attribut utilisé pour le tri. Une chaîne de longueur nulle ("") signifie qu’aucun tri n’est appliqué.

</dd> <dt>

*fSortAscending* \[ dans\]
</dt> <dd>

Valeur **System. Boolean** qui indique si l’ensemble de valeurs de chaîne doit être trié par ordre croissant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Interface **wmplib. IWMPStringCollection** pour le jeu récupéré de valeurs de chaîne.

## <a name="remarks"></a>Notes

Les requêtes composées utilisant **IWMPQuery** ne respectent pas la casse.

Lorsque la requête composée spécifiée par le paramètre *pQuery* contient une condition construite sur l’attribut **MediaType** , cette condition est ignorée. La valeur du paramètre *bstrMediaType* est toujours utilisée. Par exemple, si la requête composée contient la condition « MediaType est égal à audio » et que la valeur du paramètre *bstrMediaType* est « Video », la sélection résultante contiendra uniquement les éléments vidéo.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11.<br/>                                                                                    |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPMediaCollection2 (VB et C#)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Interface IWMPQuery (VB et C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**Interface IWMPStringCollection (VB et C#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**MediaType (attribut)**](mediatype-attribute.md)
</dt> </dl>

 

 





