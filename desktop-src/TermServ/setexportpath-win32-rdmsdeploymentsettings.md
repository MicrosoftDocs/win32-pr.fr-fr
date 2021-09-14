---
title: Méthode SetExportPath de la classe Win32_RDMSDeploymentSettings
description: Met à jour le chemin d’accès au répertoire dans lequel les machines virtuelles sont déployées pour une collection de bureaux virtuels.
ms.assetid: e52b79c8-6724-4264-93d5-4a2a14c89b6b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetExportPath
- Services Bureau à distance de la méthode SetExportPath, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode SetExportPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32dbc844aecf86d4c62fada6c5cd68d514a69272
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222057"
---
# <a name="setexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Méthode SetExportPath de la \_ classe Win32 RDMSDeploymentSettings

Met à jour le chemin d’accès au répertoire dans lequel les machines virtuelles sont déployées pour une collection de bureaux virtuels.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetExportPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DirectoryPath* \[ dans\]
</dt> <dd>

Nouveau chemin d’accès au répertoire.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.

## <a name="requirements"></a>Spécifications



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

 

 





