---
description: La méthode IsSrkAuthCompatible de la \_ classe TPM Win32 indique si l’autorisation de clé de racine de stockage (SRK) est compatible avec la valeur attendue par Windows Vista.
ms.assetid: ce6d05b8-673a-40ab-a1d7-3fedfd099306
title: Méthode IsSrkAuthCompatible de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsSrkAuthCompatible
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: f5250f8d3f9ad38f9d4c46350e06e0fe32f756dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866957"
---
# <a name="issrkauthcompatible-method-of-the-win32_tpm-class"></a>Méthode IsSrkAuthCompatible de la \_ classe TPM Win32

La méthode **IsSrkAuthCompatible** de la [**classe \_ TPM Win32**](win32-tpm.md) indique si l’autorisation de clé de racine de stockage (SRK) est compatible avec la valeur attendue par Windows Vista.

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsSrkAuthCompatible(
  [out] boolean IsSrkAuthCompatible
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IsSrkAuthCompatible* \[ à\]
</dt> <dd>

Type : **booléen**

Si la valeur est **true**, la valeur d’autorisation SRK a une valeur égale à zéro.

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

 

 
