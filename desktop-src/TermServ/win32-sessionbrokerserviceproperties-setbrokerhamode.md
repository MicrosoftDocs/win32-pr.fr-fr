---
title: Méthode SetBrokerHAMode de la classe Win32_SessionBrokerServiceProperties
description: migre les données d’une base de données WID locale vers la nouvelle base de données SQL server. il configure également le serveur du service broker pour qu’il utilise le serveur de SQL central.
ms.assetid: 8f14590d-3042-403c-a1cb-a3b257866284
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetBrokerHAMode
- Services Bureau à distance de la méthode SetBrokerHAMode, classe Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de la classe Services Bureau à distance, méthode SetBrokerHAMode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17b72233b51686911e4b1d0a661f4e46fa9bcaa813bb6ccc973b2f8a5b12da24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604548"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Méthode SetBrokerHAMode de la \_ classe Win32 SessionBrokerServiceProperties

migre les données d’une base de données WID locale vers la nouvelle base de données SQL server. il configure également le serveur du service broker pour qu’il utilise le serveur de SQL central.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetBrokerHAMode(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms,
  [in] string brokerDnsRRName,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*connStringToCentralDBRdcms* \[ dans\]
</dt> <dd>

Chaîne de connexion à la base de données centrale.

</dd> <dt>

*secondaryConnStringToCentralDBRdcms* \[ dans\]
</dt> <dd>

Chaîne de connexion secondaire à la base de données centrale.

**Windows Server 2012 R2 et Windows Server 2012 :** Ce paramètre n’est pas disponible avant Windows Server 2016.

</dd> <dt>

*brokerDnsRRName* \[ dans\]
</dt> <dd>

Nom DNS du Service Broker.

</dd> <dt>

*activeBrokerName* \[ dans\]
</dt> <dd>

Nom de service Broker actif.

**Windows Server 2012 R2 et Windows Server 2012 :** Ce paramètre n’est pas disponible avant Windows Server 2016.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                         |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SessionBrokerServiceProperties Win32**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





