---
title: Méthode IsDbReachable de la classe Win32_SessionBrokerServiceProperties
description: Vérifie si la base de données est accessible.
ms.assetid: c9774d6d-1b78-4ec1-bae2-80d41d4c9b06
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsDbReachable
- Services Bureau à distance de la méthode IsDbReachable, classe Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de la classe Services Bureau à distance, méthode IsDbReachable
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.IsDbReachable
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1cd7aaf2035251c503d85683f9aa9e9fe7b7f6285084a97133f0573ba41d79c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118848416"
---
# <a name="isdbreachable-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Méthode IsDbReachable de la \_ classe Win32 SessionBrokerServiceProperties

Vérifie si la base de données est accessible.

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsDbReachable(
  [in] string connStringToDb,
  [in] string connSecondaryStringToDb,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*connStringToDb* \[ dans\]
</dt> <dd>

Chaîne de connexion à la base de données.

</dd> <dt>

*connSecondaryStringToDb* \[ dans\]
</dt> <dd>

Chaîne de connexion secondaire à la base de données centrale.

**Windows Server 2012 R2 et Windows Server 2012 :** Ce paramètre n’est pas disponible avant Windows Server 2016.

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

 

 





