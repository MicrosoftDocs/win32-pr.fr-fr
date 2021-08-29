---
title: Méthode Network. getProxyPort
description: La méthode getProxyPort récupère le port proxy utilisé.
ms.assetid: 76771750-3763-4029-b194-d8567b5f365e
keywords:
- Lecteur Windows Media de la méthode getProxyPort
- Lecteur Windows Media de la méthode getProxyPort, classe de réseau
- Lecteur Windows Media de classe réseau, méthode getProxyPort
topic_type:
- apiref
api_name:
- Network.getProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83937bcb5d8180085ab97bfd71a0cb1653a65e8bca8cead952e4bf24e10ee690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054587"
---
# <a name="networkgetproxyport-method"></a>Méthode Network. getProxyPort

La méthode **getProxyPort** récupère le port proxy utilisé.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Network.getProxyPort(
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

Cette méthode retourne un **nombre** (**long**) contenant le port proxy utilisé. La valeur retournée est significative uniquement lorsque **getProxySettings** retourne une valeur de deux (utilisez des paramètres manuels).

## <a name="remarks"></a>Remarques

Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise le *réseau*. **getProxyPort** pour afficher les numéros de port du proxy Lecteur Windows Media actuel pour les protocoles MMS et HTTP. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy port number for HTTP.
   var proxyPortHTTP = Player.network.getProxyPort("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy port number for MMS.
   var proxyPortMMS = Player.network.getProxyPort("MMS");

// Display the port numbers in the browser client area.
// Unavailable port numbers will display as "undefined".
document.write("The current HTTP proxy port is: " + proxyPortHTTP);
document.write("<BR>");
document.write("The current MMS proxy port is: " + proxyPortMMS);

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

 

 





