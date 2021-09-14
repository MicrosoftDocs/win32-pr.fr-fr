---
title: Méthode IWMPMediaCollection2 getByAttributeAndMediaType
description: La méthode getByAttributeAndMediaType retourne une interface IWMPPlaylist qui fournit l’accès aux éléments multimédias qui ont un attribut et un type de média spécifiés.
ms.assetid: dce9cef4-1d12-4bee-a75d-42274556c5bc
keywords:
- Lecteur Windows Media de la méthode getByAttributeAndMediaType
- méthode getByAttributeAndMediaType Lecteur Windows Media, interface IWMPMediaCollection2
- Lecteur Windows Media de l’interface IWMPMediaCollection2, méthode getByAttributeAndMediaType
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getByAttributeAndMediaType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1ee4e9421b4546cdc8ace6173dacab5034b905
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292519"
---
# <a name="iwmpmediacollection2getbyattributeandmediatype-method"></a>IWMPMediaCollection2 :: getByAttributeAndMediaType, méthode

La `getByAttributeAndMediaType` méthode retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias qui ont un attribut et un type de média spécifiés.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPPlaylist getByAttributeAndMediaType(
  System.String bstrAttribute,
  System.String bstrValue,
  System.String bstrMediaType
);
```


```VB

Public Function getByAttributeAndMediaType( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getByAttributeAndMediaType
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrAttribute* \[ dans\]
</dt> <dd>

**System. String** qui est l’attribut spécifié.

</dd> <dt>

*bstrValue* \[ dans\]
</dt> <dd>

**System. String** qui est la valeur spécifiée pour l’attribut spécifié dans *bstrAttribute*.

</dd> <dt>

*bstrMediaType* \[ dans\]
</dt> <dd>

**System. String** qui est le type de média spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Interface **wmplib. IWMPPlaylist** pour la sélection récupérée.

## <a name="requirements"></a>Spécifications



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
</dt> </dl>

 

 





