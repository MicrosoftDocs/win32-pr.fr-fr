---
description: Obtient les informations d’autorisation du propriétaire d’un module de plateforme sécurisée, le cas échéant dans le registre.
ms.assetid: 3E2C28C8-4154-4B1B-9C47-AEDFD5622979
title: 'Win32_Tpm :: GetOwnerAuth, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 3c68624def56ff00dbc714f070d5f3532a257f2de0ef818221552e716c7ff571
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004097"
---
# <a name="win32_tpmgetownerauth-method"></a>Win32 \_ TPM :: GetOwnerAuth, méthode

Obtient les informations d’autorisation du propriétaire d’un module de plateforme sécurisée, le cas échéant dans le registre. si un module de plateforme sécurisée est détenu ou approvisionné dans Windows 8 avec les paramètres par défaut, les informations d’autorisation du propriétaire du module de plateforme sécurisée sont stockées dans le registre et peuvent être utilisées par cette méthode.

Cette méthode est accessible uniquement par les administrateurs locaux.

## <a name="syntax"></a>Syntaxe


```C++
uint32 GetOwnerAuth(
  [out] STRING OwnerAuth
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Origine* \[ à\]
</dt> <dd>

Informations d’autorisation du propriétaire pour un module de plateforme sécurisée (TPM), le cas échéant dans le registre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux [services de base TPM](../tbs/tbs-return-codes.md) , peuvent être retournées.

Les codes de retour courants sont répertoriés ci-dessous.



| Code/valeur de retour                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Remarques

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                      |
| Espace de noms<br/>                | \\\\.\\ racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>\_TPM. mof Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> </dl>

 

 
