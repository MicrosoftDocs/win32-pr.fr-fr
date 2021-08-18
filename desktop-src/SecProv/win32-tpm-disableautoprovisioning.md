---
description: Désactive l’approvisionnement automatique du module de plateforme sécurisée s’il est actuellement activé.
ms.assetid: 30CC2581-9C16-4A11-92F1-625992F2AF20
title: Win32_Tpm ::D méthode isableAutoProvisioning
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.DisableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 910695cc599445e6df027c0eed3ba8aa5575ad0166e06ef167d6c3ccc049c135
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004127"
---
# <a name="win32_tpmdisableautoprovisioning-method"></a>\_TPM Win32 ::D méthode isableautoprovisioning

Désactive l’approvisionnement automatique du module de plateforme sécurisée s’il est actuellement activé. L’opération n’a aucun effet si l’approvisionnement automatique est déjà désactivé. par défaut, l’approvisionnement automatique est activé pour Windows 8 et Windows Server 2012.

Cette méthode est accessible uniquement par les administrateurs locaux.

## <a name="syntax"></a>Syntaxe


```C++
uint32 DisableAutoProvisioning(
  [in, optional] BOOL OnlyForNextBoot
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*OnlyForNextBoot* \[ dans, facultatif\]
</dt> <dd>

Si la valeur est **true**, l’approvisionnement automatique est désactivé uniquement pour le prochain démarrage. Si la valeur est **false** ou n’est pas spécifié, l’approvisionnement automatique est désactivé définitivement.

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

 

 
