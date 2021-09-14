---
title: Méthode GetSecondaryConnectionString de la classe Win32_RDMSDeploymentSettings
description: Récupère la chaîne de connexion secondaire de la base de données au niveau du déploiement, qui peut être utilisée pour prendre en charge l’expiration du mot de passe.
ms.assetid: 0de02752-6cbf-4c21-b752-a57ed58aeef1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetSecondaryConnectionString
- Services Bureau à distance de la méthode GetSecondaryConnectionString, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode GetSecondaryConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2c09f4fcacabbe928fcda00447e252077bd8a51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217196"
---
# <a name="getsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a>Méthode GetSecondaryConnectionString de la \_ classe Win32 RDMSDeploymentSettings

Récupère la chaîne de connexion secondaire de la base de données au niveau du déploiement, qui peut être utilisée pour prendre en charge l’expiration du mot de passe.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetSecondaryConnectionString(
  [out] string SecondaryConnectionString
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SecondaryConnectionString* \[ à\]
</dt> <dd>

Chaîne de connexion à récupérer

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

 

 





