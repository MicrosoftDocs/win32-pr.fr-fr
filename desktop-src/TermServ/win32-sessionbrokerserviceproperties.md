---
title: Classe Win32_SessionBrokerServiceProperties
description: Définit la requête pour un service session Broker.
ms.assetid: fe7a0317-8b52-4685-9d0d-2f81058b4561
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerServiceProperties de la classe Services Bureau à distance
- Win32_SessionBrokerServiceProperties de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties.SBNetworkName
- Win32_SessionBrokerServiceProperties.SBDbConnectionString
- Win32_SessionBrokerServiceProperties.SBDbSecondaryConnectionString
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 507c4211b9506e0635966e9541167d24495735ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509377"
---
# <a name="win32_sessionbrokerserviceproperties-class"></a>\_Classe SessionBrokerServiceProperties Win32

Définit la requête pour un service session Broker.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, singleton, provider("Win32_WIN32_SESSIONBROKERSERVICEPROPERTIES_Prov"), AMENDMENT]
class Win32_SessionBrokerServiceProperties
{
  string SBNetworkName;
  string SBDbConnectionString;
  string SBDbSecondaryConnectionString;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SessionBrokerServiceProperties** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](/windows)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ SessionBrokerServiceProperties** possède ces méthodes.



| Méthode                                                                                                | Description                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteSBDbConnectionString**](win32-sessionbrokerserviceproperties-deletesbdbconnectionstring.md) | Supprime du registre les chaînes de connexion à la base de données (primaire et secondaire).<br/> **Windows server 2012 R2, Windows server 2012 et Windows server 2008 R2 :** Cette méthode n’est pas disponible avant Windows Server 2016<br/> |
| [**InstallBrokerDatabase**](win32-sessionbrokerserviceproperties-installbrokerdatabase.md)           | Installe la base de gestion du Service Broker pour les connexions Bureau à distance sur le SQL Server central<br/>                                                                                                                                                                    |
| [**IsDbReachable**](win32-sessionbrokerserviceproperties-isdbreachable.md)                           | Vérifie si la base de l’accès est accessible<br/>                                                                                                                                                                                                 |
| [**SetBrokerHAMode**](win32-sessionbrokerserviceproperties-setbrokerhamode.md)                       | Migre les données de la base de données WID locale vers la nouvelle base de données SQL Server. Il configure également le serveur du Service Broker pour qu’il utilise le SQL Server central<br/>                                                                                        |
| [**SetBrokerNonHAMode**](win32-sessionbrokerserviceproperties-setbrokernonhamode.md)                 | Migre les données du SQL Server central vers la base de données locale. Il configure également le serveur du Service Broker pour qu’il utilise la base de serveurs locale.<br/>                                                                                                              |
| [**SetSBDbConnectionStrings**](win32-sessionbrokerserviceproperties-setsbdbconnectionstrings.md)     | Enregistre les chaînes de connexion de la base de données (primaire et secondaire) dans le registre.<br/> **Windows server 2012 R2, Windows server 2012 et Windows server 2008 R2 :** Cette méthode n’est pas disponible avant Windows Server 2016<br/>     |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SessionBrokerServiceProperties** a ces propriétés.

<dl> <dt>

**SBDbConnectionString**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Chaîne de connexion à la base de données utilisée par le service session Broker.

**Windows Server 2008 R2 :** Cette propriété n’est pas disponible avant Windows Server 2012

</dd> <dt>

**SBDbSecondaryConnectionString**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Optionnel. Chaîne de connexion de base de données secondaire, utilisée par le service session Broker pour prendre en charge l’expiration du mot de passe.

**Windows server 2012 R2, Windows server 2012 et Windows server 2008 R2 :** Cette propriété n’est pas disponible avant Windows Server 2016

</dd> <dt>

**SBNetworkName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de réseau utilisé par le service session Broker.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                      |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

