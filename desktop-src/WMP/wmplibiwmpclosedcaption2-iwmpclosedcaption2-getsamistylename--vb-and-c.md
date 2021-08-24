---
title: Méthode IWMPClosedCaption2 getSAMIStyleName
description: La méthode getSAMIStyleName retourne le nom d’un style pris en charge par le fichier SAMI actuel.
ms.assetid: e7678ca6-f52f-45f4-bd1c-7fbcdf1cc47c
keywords:
- Lecteur Windows Media de la méthode getSAMIStyleName
- méthode getSAMIStyleName Lecteur Windows Media, interface IWMPClosedCaption2
- Lecteur Windows Media de l’interface IWMPClosedCaption2, méthode getSAMIStyleName
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMIStyleName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd599370afb9029a481fbae33264796232e4f129c1a5da0d2658452b785a870c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031349"
---
# <a name="iwmpclosedcaption2getsamistylename-method"></a>IWMPClosedCaption2 :: getSAMIStyleName, méthode

La méthode **getSAMIStyleName** retourne le nom d’un style pris en charge par le fichier sami actuel.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String getSAMIStyleName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMIStyleName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMIStyleName
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*nIndex* \[ dans\]
</dt> <dd>

**System. Int32** qui est l’index de base zéro du nom de style à récupérer

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**System. String** qui est le nom du style tel que spécifié dans le fichier sami.

## <a name="remarks"></a>Remarques

Les styles d’un fichier SAMI sont indexés dans l’ordre indiqué dans le fichier, à partir de zéro.

Cette méthode retourne une chaîne de longueur nulle (""), à moins qu’un fichier multimédia numérique soit ouvert (AxWindowsMediaPlayer. openState est égal à 13).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Ajout de sous-titres à des médias numériques**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interface IWMPClosedCaption (VB et C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption. SAMIStyle (VB et C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption2 (VB et C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





