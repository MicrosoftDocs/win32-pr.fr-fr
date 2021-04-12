---
title: Méthode SetBrokerHAMode de la classe Win32_SessionBrokerServiceProperties
description: Migre les données d’une base de données WID locale vers la nouvelle base de données SQL Server. Il configure également le serveur Broker pour utiliser le serveur SQL Server central.
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
ms.openlocfilehash: 4526f8ded96086ccf223b3c8e5aad72d9e0262cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103672"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Méthode SetBrokerHAMode de la \_ classe Win32 SessionBrokerServiceProperties

Migre les données d’une base de données WID locale vers la nouvelle base de données SQL Server. Il configure également le serveur Broker pour utiliser le serveur SQL Server central.

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

**Windows server 2012 R2 et Windows server 2012 :** Ce paramètre n’est pas disponible avant Windows Server 2016.

</dd> <dt>

*brokerDnsRRName* \[ dans\]
</dt> <dd>

Nom DNS du Service Broker.

</dd> <dt>

*activeBrokerName* \[ dans\]
</dt> <dd>

Nom de service Broker actif.

**Windows server 2012 R2 et Windows server 2012 :** Ce paramètre n’est pas disponible avant Windows Server 2016.

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

 

 





