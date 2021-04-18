---
title: Classe Win32_RDMSDeploymentSettings
description: Gère les paramètres de déploiement pour une collection de bureaux virtuels.
ms.assetid: c33563d5-a388-46d3-b23a-797aab9d472a
ms.tgt_platform: multiple
keywords:
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6be75f74a71a82800bc6fdd7ba0c4bae5a85021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508473"
---
# <a name="win32_rdmsdeploymentsettings-class"></a>\_Classe RDMSDeploymentSettings Win32

Gère les paramètres de déploiement pour une collection de bureaux virtuels.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDeploymentSettings
{
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ RDMSDeploymentSettings** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ RDMSDeploymentSettings** possède ces méthodes.



| Méthode                                                                                                  | Description                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**GetBaseVHDPath**](getbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | Récupère le chemin d’accès de base au répertoire dans lequel les disques durs virtuels de la collection de bureaux virtuels sont déployés.<br/>                 |
| [**GetConnectionString**](win32-rdmsdeploymentsettings-getconnectionstring.md)                         | Récupère la chaîne de connexion de base de données au niveau du déploiement.<br/>                                                             |
| [**GetDiffVHDPath**](getdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | Récupère le chemin d’accès du répertoire dans lequel les disques de différenciation sont déployés pour une collection de bureaux virtuels.<br/>            |
| [**GetExportPath**](getexportpath-win32-rdmsdeploymentsettings.md)                                     | Récupère le chemin d’accès du répertoire dans lequel les ordinateurs virtuels sont déployés pour une collection de bureaux virtuels.<br/>                  |
| [**GetInt32Property**](getint32property-win32-rdmsdeploymentsettings.md)                               | Récupère une propriété entière pour les paramètres de déploiement d’une collection de bureaux virtuels.<br/>                             |
| [**GetSecondaryConnectionString**](win32-rdmsdeploymentsettings-getsecondaryconnectionstring.md)       | Récupère la chaîne de connexion secondaire de la base de données au niveau du déploiement, qui peut être utilisée pour prendre en charge l’expiration du mot de passe.<br/> |
| [**GetSMBPath**](getsmbpath-win32-rdmsdeploymentsettings.md)                                           | Récupère le chemin d’accès UNC au partage SMB vers lequel les machines virtuelles de la collection de bureaux virtuels sont déployées.<br/>      |
| [**GetStringArrayDeploymentSetting**](getstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | Récupère les paramètres de déploiement pour une collection de bureaux virtuels.<br/>                                                    |
| [**GetStringProperty**](getstringproperty-win32-rdmsdeploymentsettings.md)                             | Récupère une propriété de type chaîne pour les paramètres de déploiement d’une collection de bureaux virtuels.<br/>                               |
| [**RemoveDeploymentSetting**](removedeploymentsetting-win32-rdmsdeploymentsettings.md)                 | Supprime les paramètres de déploiement pour une collection de bureaux virtuels.<br/>                                                      |
| [**SetBaseVHDPath**](setbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | Récupère le chemin d’accès de base au répertoire dans lequel les disques durs virtuels de la collection de bureaux virtuels sont déployés.<br/>                 |
| [**SetConnectionString**](win32-rdmsdeploymentsettings-setconnectionstring.md)                         | Définit la chaîne de connexion de la base de données au niveau du déploiement.<br/>                                                                  |
| [**SetDiffVHDPath**](setdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | Met à jour le chemin d’accès du répertoire dans lequel les disques de différenciation sont déployés pour une collection de bureaux virtuels.<br/>              |
| [**SetExportPath**](setexportpath-win32-rdmsdeploymentsettings.md)                                     | Met à jour le chemin d’accès au répertoire dans lequel les machines virtuelles sont déployées pour une collection de bureaux virtuels.<br/>                    |
| [**SetInt32Property**](setint32property-win32-rdmsdeploymentsettings.md)                               | Met à jour une propriété entière pour les paramètres de déploiement d’une collection de bureaux virtuels.<br/>                               |
| [**SetSecondaryConnectionString**](win32-rdmsdeploymentsettings-setsecondaryconnectionstring.md)       | Définit la chaîne de connexion secondaire de la base de données au niveau du déploiement.<br/>                                                        |
| [**SetSMBPath**](setsmbpath-win32-rdmsdeploymentsettings.md)                                           | Met à jour le chemin d’accès UNC au partage SMB sur lequel les machines virtuelles de la collection de bureaux virtuels sont déployées.<br/>        |
| [**SetStringArrayDeploymentSetting**](setstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | Met à jour les paramètres de déploiement pour une collection de bureaux virtuels.<br/>                                                      |
| [**SetStringProperty**](setstringproperty-win32-rdmsdeploymentsettings.md)                             | Met à jour une propriété de type chaîne pour les paramètres de déploiement d’une collection de bureaux virtuels.<br/>                                 |



 

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

[Fournisseur de services de gestion Bureau à distance](rdms-api-reference.md)
</dt> </dl>

 

 





