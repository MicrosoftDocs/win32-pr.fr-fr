---
title: Méthode SetInt32Property de la classe Win32_RDMSDeploymentSettings
description: Met à jour une propriété entière pour les paramètres de déploiement d’une collection de bureaux virtuels.
ms.assetid: c5e6dbd5-7db7-4409-bf53-c2680e4a5319
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetInt32Property
- Services Bureau à distance de la méthode SetInt32Property, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fecdc42031514d5219fc03172b951602ad021ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228582"
---
# <a name="setint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a>Méthode SetInt32Property de la \_ classe Win32 RDMSDeploymentSettings

Met à jour une propriété entière pour les paramètres de déploiement d’une collection de bureaux virtuels.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Clé* \[ dans\]
</dt> <dd>

Alias de la collection de bureaux virtuels.

</dd> <dt>

*Valeur* \[ dans\]
</dt> <dd>

Nouvelle valeur de la propriété.

</dd> </dl>

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

 

 





