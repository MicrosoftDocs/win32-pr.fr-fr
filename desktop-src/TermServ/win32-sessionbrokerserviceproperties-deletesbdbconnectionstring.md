---
title: Méthode DeleteSBDbConnectionString de la classe Win32_SessionBrokerServiceProperties
description: Supprime du registre les chaînes de connexion à la base de données (primaire ou secondaire).
ms.assetid: 275dd790-bdc7-46d1-a07d-54ec6fa33e44
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DeleteSBDbConnectionString
- Services Bureau à distance de la méthode DeleteSBDbConnectionString, classe Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de la classe Services Bureau à distance, méthode DeleteSBDbConnectionString
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.DeleteSBDbConnectionString
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a9701afebe150f0c8dc0e4bf437dd23586c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513780"
---
# <a name="deletesbdbconnectionstring-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Méthode DeleteSBDbConnectionString de la \_ classe Win32 SessionBrokerServiceProperties

Supprime du registre les chaînes de connexion à la base de données (primaire ou secondaire).

## <a name="syntax"></a>Syntaxe


```mof
uint32 DeleteSBDbConnectionString(
  [in] boolean IsSecondaryConnString
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IsSecondaryConnString* \[ dans\]
</dt> <dd>

Si la **valeur est true**, la chaîne de connexion secondaire est supprimée. Si la **valeur est false**, la chaîne de connexion principale est supprimée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                         |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SessionBrokerServiceProperties Win32**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





