---
title: Méthode SetDiffVHDPath de la classe Win32_RDMSDeploymentSettings
description: Met à jour le chemin d’accès du répertoire dans lequel les disques de différenciation sont déployés pour une collection de bureaux virtuels.
ms.assetid: 665ffbf9-0250-4956-9bce-f5a6714b47e4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetDiffVHDPath
- Services Bureau à distance de la méthode SetDiffVHDPath, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode SetDiffVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e52d206c9e0cbff19f26e38a2a02f04ea0acc03d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324414"
---
# <a name="setdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Méthode SetDiffVHDPath de la \_ classe Win32 RDMSDeploymentSettings

Met à jour le chemin d’accès du répertoire dans lequel les disques de différenciation sont déployés pour une collection de bureaux virtuels.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetDiffVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DirectoryPath* \[ dans\]
</dt> <dd>

Nouveau chemin d’accès de disque de différenciation.

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

 

 





