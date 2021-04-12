---
description: La méthode IsOwnershipAllowed de la \_ classe TPM Win32 indique si la possibilité d’installer un propriétaire pour l’appareil est autorisée.
ms.assetid: dfeb5afe-4169-470b-b5e4-cf1e5781271e
title: Méthode IsOwnershipAllowed de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnershipAllowed
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c818d5a4e4eb16ac637372f0c7ed0f2e9211ef88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201349"
---
# <a name="isownershipallowed-method-of-the-win32_tpm-class"></a>Méthode IsOwnershipAllowed de la \_ classe TPM Win32

La méthode **IsOwnershipAllowed** de la [**classe \_ TPM Win32**](win32-tpm.md) indique si la possibilité d’installer un propriétaire pour l’appareil est autorisée.

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsOwnershipAllowed(
  [out] boolean IsOwnershipAllowed
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IsOwnershipAllowed* \[ à\]
</dt> <dd>

Type : **booléen**

Si la **valeur est true**, la possibilité d’installer un propriétaire pour l’appareil est autorisée. Si la **valeur est false**, la méthode [**TakeOwnership**](takeownership-win32-tpm.md) ne parvient pas à installer un propriétaire pour l’appareil.

Cette valeur peut être modifiée à l’aide de la méthode [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) . La valeur est réinitialisée à **true** après l’exécution de la méthode [**Clear**](clear-win32-tpm.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.

Les codes de retour courants sont répertoriés ci-dessous.



| Code/valeur de retour                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Notes

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                      |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM. mof Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> </dl>

 

 
