---
title: Méthode GetExportPath de la classe Win32_RDMSDeploymentSettings
description: Récupère le chemin d’accès du répertoire dans lequel les ordinateurs virtuels sont déployés pour une collection de bureaux virtuels.
ms.assetid: 8df79e31-b960-46ae-b49c-8052b356e1a8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetExportPath
- Services Bureau à distance de la méthode GetExportPath, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode GetExportPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b77db7a72ff91ee4c161f847f5021cc4dcfe1ad8ee46d08fb8b67be1f341850
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080119"
---
# <a name="getexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Méthode GetExportPath de la \_ classe Win32 RDMSDeploymentSettings

Récupère le chemin d’accès du répertoire dans lequel les ordinateurs virtuels sont déployés pour une collection de bureaux virtuels.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetExportPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DirectoryPath* \[ à\]
</dt> <dd>

Reçoit le chemin d’accès au répertoire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                              |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RDMSDeploymentSettings Win32**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





