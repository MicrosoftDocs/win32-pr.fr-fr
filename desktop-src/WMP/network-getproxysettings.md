---
title: Méthode Network. getProxySettings
description: La méthode getProxySettings récupère le paramètre de proxy pour un protocole donné.
ms.assetid: a7b21eab-93e1-458b-aab0-60fd298cce44
keywords:
- Lecteur Windows Media de la méthode getProxySettings
- Lecteur Windows Media de la méthode getProxySettings, classe de réseau
- Lecteur Windows Media de classe réseau, méthode getProxySettings
topic_type:
- apiref
api_name:
- Network.getProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e142e7366c9e2b03e55dbd3768ee9c4fb41f30266d221a2ac5ac80019d5a7b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647439"
---
# <a name="networkgetproxysettings-method"></a>Méthode Network. getProxySettings

La méthode **getProxySettings** récupère le paramètre de proxy pour un protocole donné.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Network.getProxySettings(
  protocol
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*protocole* \[ dans\]
</dt> <dd>

**Chaîne** spécifiant le nom du protocole. Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un **nombre** (**long**) contenant l’une des valeurs suivantes.



| Valeur | Description                                                                      |
|-------|----------------------------------------------------------------------------------|
| 0     | Aucun serveur proxy n’est utilisé.                                                |
| 1     | Les paramètres de proxy du navigateur actuel sont utilisés (valides uniquement pour HTTP). |
| 2     | Les paramètres de proxy spécifiés manuellement sont utilisés.                            |
| 3     | Les paramètres de proxy sont détectés automatiquement.                                      |



 

## <a name="remarks"></a>Remarques

Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise le *réseau*. **getProxySettings** pour afficher un message qui donne des informations sur les paramètres de proxy actuels du lecteur, dans la fenêtre du navigateur. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Retrieve a number representing the current proxy settings.
var proxySetting = Player.network.getProxySettings("MMS");

// Display the message the corresponds to the current settings.
switch(proxySetting){

   case 0:
     document.write("A proxy server is not being used");
     break;

   case 1: 
     document.write("The proxy settings for the current browser are being used.");
     break;

   case 2:
     document.write("The manually specified proxy settings are being used.");
     break;

case 3:
     document.write("The proxy settings are being auto-detected.");
     break;

   default:
     document.write("Unable to determine proxy setting, try again.");
}

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet réseau**](network-object.md)
</dt> </dl>

 

 





