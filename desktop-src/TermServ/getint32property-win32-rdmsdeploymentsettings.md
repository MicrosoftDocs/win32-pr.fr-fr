---
title: Méthode GetInt32Property de la classe Win32_RDMSDeploymentSettings (Microsoft. Diagnostics. appanalysis. h)
description: Récupère une propriété entière pour les paramètres de déploiement d’une collection de bureaux virtuels.
ms.assetid: 6b8174bb-ffb7-4699-a3fb-d32ab0b202fc
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetInt32Property
- Services Bureau à distance de la méthode GetInt32Property, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f96374c610084c8ef7973d4ac4db603d9c28cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510758"
---
# <a name="getint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a>Méthode GetInt32Property de la \_ classe Win32 RDMSDeploymentSettings

Récupère une propriété entière pour les paramètres de déploiement d’une collection de bureaux virtuels.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Clé* \[ dans\]
</dt> <dd>

Alias de la collection de bureaux virtuels.

</dd> <dt>

*Valeur* \[ à\]
</dt> <dd>

Entier qui reçoit la valeur récupérée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                                 |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                                   |
| En-tête<br/>                   | <dl> <dt>Microsoft. Diagnostics. appanalysis. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RDMSDeploymentSettings Win32**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





