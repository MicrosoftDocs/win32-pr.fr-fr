---
title: Structure CB_CONNECTION_INFO (Cbclient. h)
description: Contient des informations sur une demande de connexion entrante.
ms.assetid: BA908425-3B68-40AA-B1E3-153D6873EF2C
ms.tgt_platform: multiple
keywords:
- CB_CONNECTION_INFO structure Services Bureau à distance
- Pointeur de structure PCB_CONNECTION_INFO Services Bureau à distance
topic_type:
- apiref
api_name:
- CB_CONNECTION_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36370a4faa823f509d1f3356768add0ece9a6904
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217465"
---
# <a name="cb_connection_info-structure"></a>Structure des informations de \_ connexion CB \_

Contient des informations sur une demande de connexion entrante. Cette structure est utilisée avec la méthode [**IConnectionBrokerClient :: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  WCHAR            UserName[CB_USERNAME_LENGTH];
  WCHAR            Domain[CB_DOMAINNAME_LENGTH];
  WCHAR            InitialProgram[CB_INITAPP_LENGTH];
  CB_RESOURCE_TYPE Resource;
  WCHAR            PluginName[CB_PLUGINNAME_LENGTH];
  WCHAR            FarmName[CB_FARMNAME_LENGTH];
  DWORD            dwVendorInfoLength;
  PBYTE            pVendorSpecificInfo;
} CB_CONNECTION_INFO, *PCB_CONNECTION_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**UserName**
</dt> <dd>

Nom de l’utilisateur qui demande une session.

</dd> <dt>

**Domaine**
</dt> <dd>

Nom du domaine dont le **nom d’utilisateur** est membre.

</dd> <dt>

**InitialProgram**
</dt> <dd>

Chemin d’accès complet et nom de fichier du programme initial qui est démarré lorsque la session est démarrée. Affectez à ce membre une chaîne vide si aucun programme initial ne doit être démarré.

</dd> <dt>

**Ressource**
</dt> <dd>

Valeur de l’énumération de [**\_ \_ type de ressource CB**](cb-resource-type.md) qui spécifie le type de ressource auquel la connexion entrante est connectée. Si le membre **PluginName** a la **valeur null**, ce membre est utilisé par l’connexion Bureau à distance Broker pour déterminer le plug-in à appeler pour déterminer l’ordinateur cible.

</dd> <dt>

**PluginName**
</dt> <dd>

Nom du plug-in à appeler pour déterminer l’ordinateur cible. Si ce paramètre a la **valeur null**, le membre de **ressource** est utilisé pour déterminer le plug-in à appeler.

</dd> <dt>

**FarmName**
</dt> <dd>

Nom de la batterie de serveurs qui contient les ordinateurs, dont l’un sera l’ordinateur cible sur lequel la connexion sera redirigée.

</dd> <dt>

**dwVendorInfoLength**
</dt> <dd>

Ce membre est réservé pour un usage ultérieur.

</dd> <dt>

**pVendorSpecificInfo**
</dt> <dd>

Ce membre est réservé pour un usage ultérieur.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





