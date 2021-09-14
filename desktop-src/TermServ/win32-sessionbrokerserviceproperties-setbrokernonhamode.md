---
title: Méthode SetBrokerNonHAMode de la classe Win32_SessionBrokerServiceProperties
description: migre les données du SQL Server central vers une base de données locale. Il configure également le serveur Broker pour utiliser la base de données locale.
ms.assetid: a73908be-0cc8-4512-842c-439d5cf18ed4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetBrokerNonHAMode
- Services Bureau à distance de la méthode SetBrokerNonHAMode, classe Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de la classe Services Bureau à distance, méthode SetBrokerNonHAMode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerNonHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef811bf8024f8e89f9739461dfa8499891077f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217193"
---
# <a name="setbrokernonhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Méthode SetBrokerNonHAMode de la \_ classe Win32 SessionBrokerServiceProperties

migre les données du SQL Server central vers une base de données locale. Il configure également le serveur Broker pour utiliser la base de données locale.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetBrokerNonHAMode(
  [in] string connStringToCentralDBRdcms
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*connStringToCentralDBRdcms* \[ dans\]
</dt> <dd>

Chaîne de connexion à la base de données centrale.

</dd> </dl>

## <a name="requirements"></a>Spécifications



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

 

 





