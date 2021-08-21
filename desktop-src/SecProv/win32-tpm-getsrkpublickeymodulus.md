---
description: obtient le modulo de la partie publique de la clé racine du module de plateforme sécurisée Stockage.
ms.assetid: 266AE378-8BF2-4F6E-A055-E15D95E218DC
title: 'Win32_Tpm :: GetSrkPublicKeyModulus, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkPublicKeyModulus
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 40a0cc63d00b0219ad5a86600db4ff3ebc420874e890dfec5233b33d1ba380dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890843"
---
# <a name="win32_tpmgetsrkpublickeymodulus-method"></a>Win32 \_ TPM :: GetSrkPublicKeyModulus, méthode

obtient le modulo de la partie publique de la clé racine du module de plateforme sécurisée Stockage.

Cette méthode est accessible uniquement par les administrateurs locaux.

## <a name="syntax"></a>Syntaxe


```C++
uint32 GetSrkPublicKeyModulus(
  [out] uint8 SrkPublicKeyModulus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SrkPublicKeyModulus* \[ à\]
</dt> <dd>

retourne un tableau de 256 octets contenant le modulo de la partie publique de la clé racine du module de plateforme sécurisée Stockage

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

 

 
