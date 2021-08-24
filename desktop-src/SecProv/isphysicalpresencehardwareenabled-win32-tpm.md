---
description: La méthode IsPhysicalPresenceHardwareEnabled de la \_ classe TPM Win32 indique si la présence physique sur la plateforme peut être définie à l’aide d’un signal matériel.
ms.assetid: 65dabfa9-bfbe-4b9b-8e80-02269895c7ad
title: Méthode IsPhysicalPresenceHardwareEnabled de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalPresenceHardwareEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 499ec39741b23583b599407ef43696ab82164f365626c8042586b6b6e4b56deb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797039"
---
# <a name="isphysicalpresencehardwareenabled-method-of-the-win32_tpm-class"></a>Méthode IsPhysicalPresenceHardwareEnabled de la \_ classe TPM Win32

La méthode **IsPhysicalPresenceHardwareEnabled** de la [**classe \_ TPM Win32**](win32-tpm.md) indique si la présence physique sur la plateforme peut être définie à l’aide d’un signal matériel. Cette valeur est configurée par le fabricant de la plateforme en fonction de la conception de la plateforme. La documentation du fabricant de la plateforme peut fournir des informations supplémentaires.

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsPhysicalPresenceHardwareEnabled(
  [out] boolean IsPhysicalPresenceHardwareEnabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IsPhysicalPresenceHardwareEnabled* \[ à\]
</dt> <dd>

Type : **booléen**

Si la **valeur est true**, la présence physique sur la plateforme peut être définie à l’aide d’un signal matériel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.

Les codes de retour courants sont répertoriés ci-dessous.



| Code/valeur de retour                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Remarques

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                      |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM. mof Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> </dl>

 

 
