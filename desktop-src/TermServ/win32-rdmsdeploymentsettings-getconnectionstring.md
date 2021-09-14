---
title: Méthode GetConnectionString de la classe Win32_RDMSDeploymentSettings
description: Récupère la chaîne de connexion de base de données au niveau du déploiement.
ms.assetid: 91a90883-9b87-42e5-af52-90226f0344bf
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetConnectionString
- Services Bureau à distance de la méthode GetConnectionString, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode GetConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6476c938f62e0cd0e1f9d034c89fded50994946
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217201"
---
# <a name="getconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a>Méthode GetConnectionString de la \_ classe Win32 RDMSDeploymentSettings

Récupère la chaîne de connexion de base de données au niveau du déploiement.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetConnectionString(
  [out] string ConnectionString
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ConnectionString* \[ à\]
</dt> <dd>

Chaîne de connexion

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.

## <a name="requirements"></a>Spécifications



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

 

 





