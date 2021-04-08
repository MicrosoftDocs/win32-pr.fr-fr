---
title: Méthode InstallBrokerDatabase de la classe Win32_SessionBrokerServiceProperties
description: Installe une base de données du Service Broker pour les connexions Bureau à distance sur un serveur SQL Server central.
ms.assetid: 9cc6fa4a-f1eb-49eb-bec4-acaff73190e8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode InstallBrokerDatabase
- Services Bureau à distance de la méthode InstallBrokerDatabase, classe Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de la classe Services Bureau à distance, méthode InstallBrokerDatabase
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.InstallBrokerDatabase
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da560bd4746c41864b3c56438f841efebe71ecd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740197"
---
# <a name="installbrokerdatabase-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Méthode InstallBrokerDatabase de la \_ classe Win32 SessionBrokerServiceProperties

Installe une base de données du Service Broker pour les connexions Bureau à distance sur un serveur SQL Server central.

## <a name="syntax"></a>Syntaxe


```mof
uint32 InstallBrokerDatabase(
  [in] string newDbFilePath,
  [in] string connStringToCentralDBMaster,
  [in] string centralRdcmsDbName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*newDbFilePath* \[ dans\]
</dt> <dd>

nouveau chemin d’accès au fichier de base de données.

</dd> <dt>

*connStringToCentralDBMaster* \[ dans\]
</dt> <dd>

Chaîne de connexion à la base de données principale centrale.

</dd> <dt>

*centralRdcmsDbName* \[ dans\]
</dt> <dd>

Nom de la base de données centrale.

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

 

 





