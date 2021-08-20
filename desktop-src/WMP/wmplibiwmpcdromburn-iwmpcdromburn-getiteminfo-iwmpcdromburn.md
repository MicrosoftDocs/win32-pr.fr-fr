---
title: Méthode IWMPCdromBurn getItemInfo
description: La méthode getItemInfo récupère la valeur de l’attribut spécifié pour le CD.
ms.assetid: 9ca54ec4-42be-40c1-931e-c3bfcbc2b370
keywords:
- Lecteur Windows Media de la méthode getItemInfo
- méthode getItemInfo Lecteur Windows Media, interface IWMPCdromBurn
- Lecteur Windows Media de l’interface IWMPCdromBurn, méthode getItemInfo
topic_type:
- apiref
api_name:
- IWMPCdromBurn.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2cf1a91ad60826e19051a59617157110fbcd8d75eff325f94f9b3f84d759aa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116227"
---
# <a name="iwmpcdromburngetiteminfo-method"></a>IWMPCdromBurn :: getItemInfo, méthode

La méthode **getItemInfo** récupère la valeur de l’attribut spécifié pour le CD.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String getItemInfo(
  System.String bstrItem
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItem As System.String _
) As System.String
Implements IWMPCdromBurn.getItemInfo
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrItem* \[ dans\]
</dt> <dd>

**System. String** qui contient l’une des valeurs suivantes.



| Valeur         | Description                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| AvailableTime | Récupère le temps disponible sur le CD, en secondes.                                          |
| Vide         | Récupère un **System. Boolean** (représenté sous la forme d’une chaîne) indiquant si le CD est vide. |
| FreeSpace     | Récupère l’espace libre sur le CD, en octets.                                                |
| TotalSpace    | Récupère l’espace total, en octets, sur le CD.                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**System. String** qui est la valeur de l’attribut spécifié.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11<br/>                                                                                     |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPCdromBurn (VB et C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





