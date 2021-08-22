---
title: Méthode IWMPLibrary isIdentical
description: La méthode isIdentical retourne une valeur qui indique si l’objet fourni est le même que celui en cours.
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- Lecteur Windows Media de la méthode isIdentical
- méthode isIdentical Lecteur Windows Media, interface IWMPLibrary
- Lecteur Windows Media de l’interface IWMPLibrary, méthode isIdentical
topic_type:
- apiref
api_name:
- IWMPLibrary.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ed37725bbda5b170ece8ce71c12499b42f0b361cbac3bbe65f1b875af06fc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506049"
---
# <a name="iwmplibraryisidentical-method"></a>IWMPLibrary :: isIdentical, méthode

La méthode **isIdentical** retourne une valeur qui indique si l’objet fourni est le même que celui en cours.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Boolean isIdentical(
  IWMPLibrary pIWMPLibrary
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPLibrary As IWMPLibrary _
) As System.Boolean
Implements IWMPLibrary.isIdentical
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*pIWMPLibrary* \[ dans\]
</dt> <dd>

Interface **wmplib. IWMPLibrary** qui représente l’objet à comparer avec l’objet actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**System. Boolean** qui est le résultat de la comparaison. La valeur **true** indique que les objets sont identiques.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11.<br/>                                                                                    |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPLibrary (VB et C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





