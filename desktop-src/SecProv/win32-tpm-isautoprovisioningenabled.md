---
description: Indique si l’approvisionnement automatique du module de plateforme sécurisée est activé.
ms.assetid: C908673C-8BDB-4541-85C6-65FED1EBB535
title: 'Win32_Tpm :: IsAutoProvisioningEnabled, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsAutoProvisioningEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 53541922b803a7898b66ce363a5718114b6c5f6d3913a6cde86650200ae76770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890854"
---
# <a name="win32_tpmisautoprovisioningenabled-method"></a>Win32 \_ TPM :: IsAutoProvisioningEnabled, méthode

Indique si l’approvisionnement automatique du module de plateforme sécurisée est activé. par défaut, l’approvisionnement automatique est activé pour Windows 8 et Windows Server 2012.

Cette méthode est accessible uniquement par les administrateurs locaux.

## <a name="syntax"></a>Syntaxe


```C++
uint32 IsAutoProvisioningEnabled(
  [out] BOOL IsAutoProvisioningEnabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IsAutoProvisioningEnabled* \[ à\]
</dt> <dd>

Affectez la valeur **true** si l’approvisionnement automatique du module de plateforme sécurisée est activé.

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

 

 
