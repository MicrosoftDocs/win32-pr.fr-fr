---
title: Méthode Network. Setproxysettings n'
description: La méthode Setproxysettings n’spécifie le paramètre de proxy pour un protocole donné.
ms.assetid: 473501c9-27ea-47ec-bc82-691804fbfb89
keywords:
- Lecteur Windows Media de la méthode setproxysettings n'
- Lecteur Windows Media de la méthode setproxysettings n', classe de réseau
- Lecteur Windows Media de classe réseau, méthode setproxysettings n'
topic_type:
- apiref
api_name:
- Network.setProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f3da665b07f717449721c9fb43a8733cdb6c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193243"
---
# <a name="networksetproxysettings-method"></a>Méthode Network. Setproxysettings n'

La méthode **setproxysettings n'** spécifie le paramètre de proxy pour un protocole donné.

## <a name="syntax"></a>Syntaxe


```JScript
Network.setProxySettings(
  protocol,
  setting
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*protocole* \[ dans\]
</dt> <dd>

**Chaîne** spécifiant le nom du protocole. Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).

</dd> <dt>

*paramètre* \[ dans\]
</dt> <dd>

**Nombre** (**long**) contenant l’une des valeurs suivantes.



| Valeur | Description                                                          |
|-------|----------------------------------------------------------------------|
| 0     | N’utilisez pas de serveur proxy.                                           |
| 1     | Utilisez les paramètres de proxy du navigateur actuel (valide uniquement pour HTTP). |
| 2     | Utilisez les paramètres de proxy spécifiés manuellement.                           |
| 3     | Détectez automatiquement les paramètres du proxy.                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="examples"></a>Exemples

l’exemple suivant utilise JScript avec un élément SELECT HTML **pour permettre à l’utilisateur de spécifier le paramètre de proxy Lecteur Windows Media pour le protocole HTTP. L’objet Player** a été créé avec ID = "Player".


```JScript
<SELECT ID = HTTPsetproxy  NAME = "HTTPsetproxy"  LANGUAGE="JScript"
        onChange = "
                      /* Store the current selection.*/
                      var setting = this.value;

                      /* Change the proxy setting. */
                      Player.network.setProxySettings('HTTP', setting);
">

<OPTION VALUE=0>Do not use a proxy server
<OPTION VALUE=1>Use the browser settings
<OPTION VALUE=2>Use manual settings
<OPTION VALUE=3>Auto-detect settings

</SELECT>

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

 

 





