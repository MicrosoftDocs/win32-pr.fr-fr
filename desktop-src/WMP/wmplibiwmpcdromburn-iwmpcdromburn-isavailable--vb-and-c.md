---
title: IWMPCdromBurn isAvailable, méthode
description: La méthode isAvailable fournit des informations sur le lecteur de CD et le support.
ms.assetid: 75e81f5f-5839-4012-b0b9-e77b3ca6f35c
keywords:
- isAvailable, méthode Lecteur Windows Media
- isAvailable, méthode Lecteur Windows Media, IWMPCdromBurn, interface
- IWMPCdromBurn interface Lecteur Windows Media, isAvailable, méthode
topic_type:
- apiref
api_name:
- IWMPCdromBurn.isAvailable
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d604cb9d9e170a3837fbd477db4c7ff309e1df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519864"
---
# <a name="iwmpcdromburnisavailable-method"></a>IWMPCdromBurn :: isAvailable, méthode

La méthode **isAvailable** fournit des informations sur le lecteur de CD et le support.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Boolean isAvailable(
  System.String bstrItem
);
```


```VB

Public Function isAvailable( _
  ByVal bstrItem As System.String _
) As System.Boolean
Implements IWMPCdromBurn.isAvailable
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrItem* \[ dans\]
</dt> <dd>

**System. String** qui contient l’une des valeurs suivantes.



| Valeur | Description                 |
|-------|-----------------------------|
| Écrire  | Le lecteur est un graveur de CD.   |
| ROM  | Un CD est présent dans le lecteur. |
| Effacer | Le CD peut être effacé.       |
| Write | Le CD peut être écrit.   |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

**System. Boolean** qui indique le résultat.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11.<br/>                                                                                    |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPCdromBurn (VB et C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





