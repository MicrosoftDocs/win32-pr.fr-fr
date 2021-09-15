---
title: Méthode IWMPLibraryServices getCountByType
description: La méthode getCountByType retourne le nombre de bibliothèques disponibles d’un type spécifié.
ms.assetid: 75f22e21-fbaf-45dc-b64f-1f687a3cf241
keywords:
- Lecteur Windows Media de la méthode getCountByType
- méthode getCountByType Lecteur Windows Media, interface IWMPLibraryServices
- Lecteur Windows Media de l’interface IWMPLibraryServices, méthode getCountByType
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbd874c06c2557102011c63ee1abb895d092656
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413306"
---
# <a name="iwmplibraryservicesgetcountbytype-method"></a>IWMPLibraryServices :: getCountByType, méthode

La méthode **getCountByType** retourne le nombre de bibliothèques disponibles d’un type spécifié.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 getCountByType(
  WMPLibraryType wmplt
);
```


```VB

Public Function getCountByType( _
  ByVal wmplt As WMPLibraryType _
) As System.Int32
Implements IWMPLibraryServices.getCountByType
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*wmplt* \[ dans\]
</dt> <dd>

Valeur de l’énumération **wmplib. WMPLibraryType** qui spécifie le type de bibliothèque à compter.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

**System. Int32** qui est le nombre de bibliothèques.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11.<br/>                                                                                    |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPLibraryServices (VB et C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**WMPLibraryType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





