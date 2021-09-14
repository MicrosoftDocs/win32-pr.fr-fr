---
title: Méthode SetStringProperty de la classe Win32_RDMSDeploymentSettings (certenroll. h)
description: Met à jour une propriété de type chaîne pour les paramètres de déploiement d’une collection de bureaux virtuels.
ms.assetid: 500ab1cb-7336-47a8-adee-790976ea30fe
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetStringProperty
- Services Bureau à distance de la méthode SetStringProperty, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode SetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 138f6d91ed428caabf8da69e3d958675f879dd15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324378"
---
# <a name="setstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a>Méthode SetStringProperty de la \_ classe Win32 RDMSDeploymentSettings

Met à jour une propriété de type chaîne pour les paramètres de déploiement d’une collection de bureaux virtuels.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
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
| En-tête<br/>                   | <dl> <dt>Certenroll. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RDMSDeploymentSettings Win32**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





