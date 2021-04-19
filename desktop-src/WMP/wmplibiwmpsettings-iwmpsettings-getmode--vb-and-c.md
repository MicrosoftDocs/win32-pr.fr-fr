---
title: Méthode IWMPSettings getMode
description: La méthode getMode retourne une valeur indiquant si le mode de boucle ou le mode de lecture aléatoire est actif.
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- méthode getMode lecteur Windows Media
- méthode getMode lecteur Windows Media, interface IWMPSettings
- Interface IWMPSettings lecteur Windows Media, méthode getMode
topic_type:
- apiref
api_name:
- IWMPSettings.getMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229cacf629410f958a062615cd5feb22be2ab0d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542337"
---
# <a name="iwmpsettingsgetmode-method"></a>IWMPSettings :: getMode, méthode

La méthode **getMode** retourne une valeur indiquant si le mode de boucle ou le mode de lecture aléatoire est actif.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Boolean getMode(
  System.String bstrMode
);
```


```VB

Public Function getMode( _
  ByVal bstrMode As System.String _
) As System.Boolean
Implements IWMPSettings.getMode
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrMode* \[ dans\]
</dt> <dd>

**System. String** qui est l’une des valeurs suivantes.



| Valeur      | Description                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| autoRewind | Les suivis sont redémarrés à partir du début après avoir été lus jusqu’à la fin.                                |
| loop       | La séquence de suivi se répète lui-même.                                                           |
| showFrame  | L’image clé la plus proche s’affiche lorsque l’image n’est pas lue. Ce mode n’est pas pertinent pour les pistes audio. |
| lecture aléatoire    | Les pistes sont lues dans un ordre aléatoire.                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Valeur **System. Boolean** indiquant si le mode spécifié est actif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPSettings (VB et C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. setMode (VB et C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





