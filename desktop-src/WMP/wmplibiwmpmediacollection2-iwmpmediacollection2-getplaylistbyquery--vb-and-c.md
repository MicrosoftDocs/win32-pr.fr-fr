---
title: Méthode IWMPMediaCollection2 getPlaylistByQuery
description: La méthode getPlaylistByQuery retourne une interface IWMPPlaylist qui fournit l’accès aux éléments multimédias qui correspondent aux conditions de requête.
ms.assetid: ebbb631f-1faa-4c89-8c1d-cc2b128126b8
keywords:
- Lecteur Windows Media de la méthode getPlaylistByQuery
- méthode getPlaylistByQuery Lecteur Windows Media, interface IWMPMediaCollection2
- Lecteur Windows Media de l’interface IWMPMediaCollection2, méthode getPlaylistByQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getPlaylistByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acd80467c78aac832c5ac2784281abcf07975a1956ee304c734b2b45b82901fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053577"
---
# <a name="iwmpmediacollection2getplaylistbyquery-method"></a>IWMPMediaCollection2 :: getPlaylistByQuery, méthode

La `getPlaylistByQuery` méthode retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias qui correspondent aux conditions de requête.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPPlaylist getPlaylistByQuery(
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getPlaylistByQuery( _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getPlaylistByQuery
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*pQuery* \[ dans\]
</dt> <dd>

Interface **wmplib. IWMPQuery** qui représente la requête.

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

Valeur **System. Boolean** qui indique si la sélection doit être triée dans l’ordre croissant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Interface **wmplib. IWMPPlaylist** pour la sélection récupérée.

## <a name="remarks"></a>Remarques

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

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interface IWMPQuery (VB et C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**MediaType (attribut)**](mediatype-attribute.md)
</dt> </dl>

 

 





