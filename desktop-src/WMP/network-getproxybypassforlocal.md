---
title: Méthode Network. getProxyBypassForLocal
description: La méthode getProxyBypassForLocal récupère une valeur qui indique si le serveur proxy est contourné si le serveur d’origine se trouve sur un réseau local.
ms.assetid: e5217d56-da22-4424-94b0-400369410b47
keywords:
- Lecteur Windows Media de la méthode getProxyBypassForLocal
- Lecteur Windows Media de la méthode getProxyBypassForLocal, classe de réseau
- Lecteur Windows Media de classe réseau, méthode getProxyBypassForLocal
topic_type:
- apiref
api_name:
- Network.getProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f22eb6187938318d95b9dd7a473b58e216315210d4af41c29b352b2654cbf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054557"
---
# <a name="networkgetproxybypassforlocal-method"></a>Méthode Network. getProxyBypassForLocal

La méthode **getProxyBypassForLocal** récupère une valeur qui indique si le serveur proxy est contourné si le serveur d’origine se trouve sur un réseau local.

## <a name="syntax"></a>Syntaxe


```JScript
bRetVal = Network.getProxyBypassForLocal(
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

Cette méthode retourne une **valeur booléenne** indiquant si le serveur proxy est contourné. La valeur retournée est significative uniquement lorsque **getProxySettings** retourne une valeur de deux (utilisez des paramètres manuels).

## <a name="remarks"></a>Remarques

Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise le *réseau*. **getProxyBypassForLocal** pour afficher si Lecteur Windows Media est défini pour ignorer le serveur proxy pour les adresses locales. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy bypass for local value for HTTP.
   var proxyBypassForLocalHTTP = Player.network.getProxyBypassForLocal("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy bypass for local value for MMS.
   var proxyBypassForLocalMMS = Player.network.getProxyBypassForLocal("MMS");

// Display the proxy bypass for local values in the browser client area.
// Unavailable proxy bypass for local values will display as "undefined".
document.write("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP);
document.write("<BR>");
document.write("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS);

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet réseau**](network-object.md)
</dt> <dt>

[**Network. getProxySettings**](network-getproxysettings.md)
</dt> </dl>

 

 





