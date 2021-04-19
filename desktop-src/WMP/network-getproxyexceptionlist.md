---
title: Méthode Network. getProxyExceptionList
description: La méthode getProxyExceptionList récupère la liste des exceptions du proxy.
ms.assetid: f81d8c0f-cc75-470c-9c24-ceaf8a4b6f97
keywords:
- méthode getProxyExceptionList lecteur Windows Media
- méthode getProxyExceptionList lecteur Windows Media, classe réseau
- Classe réseau lecteur Windows Media, méthode getProxyExceptionList
topic_type:
- apiref
api_name:
- Network.getProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ace9bd569c1cc53a8f3d522703aee6154e68a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533194"
---
# <a name="networkgetproxyexceptionlist-method"></a>Méthode Network. getProxyExceptionList

La méthode **getProxyExceptionList** récupère la liste des exceptions du proxy.

## <a name="syntax"></a>Syntaxe


```JScript
strRetVal = Network.getProxyExceptionList(
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

Cette méthode retourne une **chaîne** spécifiant une liste délimitée par des points-virgules des hôtes pour lesquels le serveur proxy est contourné. La valeur retournée est significative uniquement lorsque **getProxySettings** retourne une valeur de deux (utilisez des paramètres manuels).

## <a name="remarks"></a>Notes

Il s’agit d’une liste d’ordinateurs, de domaines et/ou d’adresses qui contournent le serveur proxy lorsque la partie hôte de l’URL cible correspond à une entrée de la liste.

Le \* caractère peut être utilisé comme caractère générique pour répertorier les entrées. Par exemple, \* . com correspond à tous les ordinateurs hôtes du domaine com alors que 67. \* correspond à tous les hôtes de la classe 67 d’un sous-réseau.

Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise le *réseau*. **getProxyExceptionList** pour afficher les listes de proxys ignorés pour les protocoles MMS et http. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy exception list for HTTP.
   var proxyExceptionListHTTP = Player.network.getProxyExceptionList("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy exception list for MMS.
   var proxyExceptionListMMS = Player.network.getProxyExceptionList("MMS");

// Display the proxy exception lists in the browser client area.
// Unavailable proxy exception lists will display as "undefined".
document.write("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
document.write("<BR>");
document.write("The current MMS proxy exception list: " + proxyExceptionListMMS);

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

 

 





