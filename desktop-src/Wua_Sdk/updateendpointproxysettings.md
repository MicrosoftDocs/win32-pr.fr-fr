---
description: La structure UpdateEndpointProxySettings définit les paramètres de proxy utilisés lors de la demande d’un jeton.
ms.assetid: 24AA8843-D4EE-4F17-8B96-63ED25B365D2
title: UpdateEndpointProxySettings, structure (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointProxySettings
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: aad6ad294baab37b7516152438dbc9fd05f7036a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034033"
---
# <a name="updateendpointproxysettings-structure"></a>UpdateEndpointProxySettings, structure

La structure **UpdateEndpointProxySettings** définit les paramètres de proxy utilisés lors de la demande d’un jeton.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagUpdateEndpointProxySettings {
  BSTR szProxyAddr;
  BSTR szBypassList;
  BSTR szUserName;
  BSTR szPassword;
} UpdateEndpointProxySettings;
```



## <a name="members"></a>Membres

<dl> <dt>

**szProxyAddr**
</dt> <dd>

Le nom DNS ou l’adresse IP du serveur proxy à utiliser (par exemple, « proxy.somecorp.com » ou « 192.168.0.4 »), ou une chaîne vide si aucun proxy ne doit être utilisé.

</dd> <dt>

**szBypassList**
</dt> <dd>

Liste des adresses d’hôtes qui doivent contourner le serveur proxy, ou une chaîne vide si toutes les adresses d’hôte doivent utiliser le serveur proxy

WUA n’utilise pas ces données si **szProxyAddr** est vide.

</dd> <dt>

**szUserName**
</dt> <dd>

Nom d’utilisateur utilisé pour l’authentification auprès du serveur proxy, ou chaîne vide si aucune authentification n’est nécessaire.

WUA n’utilise pas ces données si **szProxyAddr** est vide.

</dd> <dt>

**szPassword**
</dt> <dd>

Mot de passe utilisé pour l’authentification auprès du serveur proxy, ou chaîne vide si aucune authentification n’est nécessaire.

WUA n’utilise pas ces données si **szProxyAddr** est vide.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                              |
| En-tête<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




