---
title: Méthode IWMPSettings setMode
description: La méthode setMode définit le mode de boucle ou le mode de lecture aléatoire sur actif ou inactif.
ms.assetid: e9d3765e-6edb-47a5-ac97-5e00b62498c2
keywords:
- Lecteur Windows Media de la méthode setMode
- méthode setMode Lecteur Windows Media, interface IWMPSettings
- Lecteur Windows Media de l’interface IWMPSettings, méthode setMode
topic_type:
- apiref
api_name:
- IWMPSettings.setMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529aadf412cdae869ae3c308d82dcd08a7dfd581aeb7ecc711052f6acd54b962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568406"
---
# <a name="iwmpsettingssetmode-method"></a>IWMPSettings :: setMode, méthode

La méthode **setMode** définit le mode de boucle ou le mode de lecture aléatoire sur actif ou inactif.

## <a name="syntax"></a>Syntaxe


```CSharp
public void setMode(
  System.String bstrMode,
  System.Boolean varfMode
);
```


```VB

Public Sub setMode( _
  ByVal bstrMode As System.String, _
  ByVal varfMode As System.Boolean _
)
Implements IWMPSettings.setMode
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrMode* \[ dans\]
</dt> <dd>

**System. String** qui est le nom du mode en cours de modification, contenant l’une des valeurs suivantes.



| Valeur      | Description                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| autoRewind | Les suivis sont redémarrés à partir du début après avoir été lus jusqu’à la fin.                                |
| loop       | La séquence de suivi se répète lui-même.                                                           |
| showFrame  | L’image clé la plus proche s’affiche lorsque l’image n’est pas lue. Ce mode n’est pas pertinent pour les pistes audio. |
| lecture aléatoire    | Les pistes sont lues dans un ordre aléatoire.                                                               |



 

</dd> <dt>

*varfMode* \[ dans\]
</dt> <dd>

Valeur **System. Boolean** spécifiant si le nouveau mode spécifié est actif.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

lorsque le mode showFrame est actif, Lecteur Windows Media devez accéder au contenu track pour récupérer l’image vidéo. Utilisez ce mode avec précaution lors de la diffusion de contenu qui n’est pas local.

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

[**IWMPSettings. getMode (VB et C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> </dl>

 

 





