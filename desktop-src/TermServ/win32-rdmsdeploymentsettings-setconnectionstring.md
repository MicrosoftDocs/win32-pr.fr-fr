---
title: Méthode SetConnectionString de la classe Win32_RDMSDeploymentSettings
description: Définit la chaîne de connexion de la base de données au niveau du déploiement.
ms.assetid: c8902ab9-72a6-4d69-ab22-f6074205deb4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetConnectionString
- Services Bureau à distance de la méthode SetConnectionString, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode SetConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ccb3f618f6a08dcb95bb7dc04c1494be6a7b5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384447"
---
# <a name="setconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a>Méthode SetConnectionString de la \_ classe Win32 RDMSDeploymentSettings

Définit la chaîne de connexion de la base de données au niveau du déploiement.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetConnectionString(
  [in] string ConnectionString
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ConnectionString* \[ dans\]
</dt> <dd>

Chaîne de connexion à définir

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                              |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RDMSDeploymentSettings Win32**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





