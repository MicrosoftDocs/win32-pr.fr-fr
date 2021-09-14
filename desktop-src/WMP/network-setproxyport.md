---
title: Méthode Network. setProxyPort
description: La méthode setProxyPort spécifie le port du proxy à utiliser. | Méthode Network. setProxyPort
ms.assetid: 09cfce4a-191c-4596-b678-15d9328d5c53
keywords:
- Lecteur Windows Media de la méthode setProxyPort
- Lecteur Windows Media de la méthode setProxyPort, classe de réseau
- Lecteur Windows Media de classe réseau, méthode setProxyPort
topic_type:
- apiref
api_name:
- Network.setProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2438688535e4727688ddbd5d67fd65cbed15864d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193244"
---
# <a name="networksetproxyport-method"></a>Méthode Network. setProxyPort

La méthode **setProxyPort** spécifie le port du proxy à utiliser.

## <a name="syntax"></a>Syntaxe


```JScript
Network.setProxyPort(
  protocol,
  port
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*protocole* \[ dans\]
</dt> <dd>

**Chaîne** spécifiant le nom du protocole. Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).

</dd> <dt>

*port* \[ dans\]
</dt> <dd>

**Nombre** (**long**) spécifiant le port du proxy à utiliser.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode n’a aucun effet, à moins que **getProxySettings** retourne la valeur 2 (utiliser des paramètres manuels).

Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise le *réseau*. **setProxyPort** pour spécifier le numéro de port du proxy Lecteur Windows Media pour le protocole MMS. Le numéro de port est récupéré à partir d’un élément INPUT HTML avec ID = "PORT". L’objet **Player** a été créé avec ID = "Player".


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the port number specified by the user.
   var portnumber = PORT.value;

   // Set the port number for the MMS protocol.
   Player.network.setProxyPort("MMS", portnumber);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet réseau**](network-object.md)
</dt> </dl>

 

 





