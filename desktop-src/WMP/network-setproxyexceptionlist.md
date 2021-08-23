---
title: Méthode Network. setProxyExceptionList
description: La méthode setProxyExceptionList spécifie la liste des exceptions du proxy. | Méthode Network. setProxyExceptionList
ms.assetid: c9eeb058-5ffb-4405-9bf2-776f120e2db4
keywords:
- Lecteur Windows Media de la méthode setProxyExceptionList
- Lecteur Windows Media de la méthode setProxyExceptionList, classe de réseau
- Lecteur Windows Media de classe réseau, méthode setProxyExceptionList
topic_type:
- apiref
api_name:
- Network.setProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf72d9c35778e965021ec31671e4e345ec2d8e281d18f9fcb16c8f2ff04d4722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647299"
---
# <a name="networksetproxyexceptionlist-method"></a>Méthode Network. setProxyExceptionList

La méthode **setProxyExceptionList** spécifie la liste des exceptions du proxy.

## <a name="syntax"></a>Syntaxe


```JScript
Network.setProxyExceptionList(
  protocol,
  list
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*protocole* \[ dans\]
</dt> <dd>

**Chaîne** spécifiant le nom du protocole. Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).

</dd> <dt>

*liste* \[ dans\]
</dt> <dd>

**Chaîne** spécifiant une liste délimitée par des points-virgules des hôtes pour lesquels le serveur proxy est contourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Il s’agit d’une liste d’ordinateurs, de domaines et/ou d’adresses qui contournent le serveur proxy lorsque la partie hôte de l’URL cible correspond à une entrée de la liste.

Le \* caractère peut être utilisé comme caractère générique pour répertorier les entrées. Par exemple, \* . com correspond à tous les ordinateurs hôtes du domaine com, tandis que 67. \* correspond à tous les hôtes de la classe 67 d’un sous-réseau.

Cette méthode n’a aucun effet, à moins que **getProxySettings** retourne la valeur 2 (utiliser des paramètres manuels).

Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise le *réseau*. **setProxyExceptionList** pour spécifier une liste d’hôtes pour lesquels le serveur proxy est contourné lors de l’utilisation du protocole MMS. La nouvelle liste est récupérée à partir d’un élément de texte HTML avec ID = "XLIST". L’objet **Player** a été créé avec ID = "Player".


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the user's new exception list.
   var proxyxlist = XLIST.value;

   // Set the exception list.
   Player.network.setProxyExceptionList("MMS", proxyxlist);
}

else

// Warn that the proxy settings must be set to 2.
alert("Proxy settings must be manual!");

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

 

 





