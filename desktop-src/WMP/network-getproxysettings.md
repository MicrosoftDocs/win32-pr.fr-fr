---
title: Méthode Network. getProxySettings
description: La méthode getProxySettings récupère le paramètre de proxy pour un protocole donné.
ms.assetid: a7b21eab-93e1-458b-aab0-60fd298cce44
keywords:
- méthode getProxySettings lecteur Windows Media
- méthode getProxySettings lecteur Windows Media, classe réseau
- Classe réseau lecteur Windows Media, méthode getProxySettings
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
ms.openlocfilehash: 44a306fca1e671e7e5b3a89c0da952e5c81ba20e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530965"
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



 

## <a name="remarks"></a>Notes

Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise le *réseau*. **getProxySettings** pour afficher un message qui donne des informations sur les paramètres de proxy actuels du lecteur, dans la fenêtre du navigateur. L’objet **Player** a été créé avec ID = "Player".


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

 

 





