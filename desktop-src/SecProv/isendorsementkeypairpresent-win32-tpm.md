---
description: La méthode IsEndorsementKeyPairPresent de la \_ classe TPM Win32 indique si la paire de clés de type EK existe sur l’appareil.
ms.assetid: c36cd0b5-1ac2-4fcf-b140-c5ecb0b3b211
title: Méthode IsEndorsementKeyPairPresent de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEndorsementKeyPairPresent
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: bcbc0c4877aae2db0e94d42838100720ee0ae0dcbdcc33f52cf70d2e23327e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004467"
---
# <a name="isendorsementkeypairpresent-method-of-the-win32_tpm-class"></a>Méthode IsEndorsementKeyPairPresent de la \_ classe TPM Win32

La méthode **IsEndorsementKeyPairPresent** de la [**classe \_ TPM Win32**](win32-tpm.md) indique si la paire de clés de type EK existe sur l’appareil. La paire de clés de type EK est nécessaire pour que l’appareil puisse être détenu. Cette paire de clés peut être créée par la méthode [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) .

L’appareil doit être activé et activé pour que cette méthode aboutisse. Pour activer et activer un appareil sans propriétaire, consultez la méthode [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsEndorsementKeyPairPresent(
  [out] boolean IsEndorsementKeyPairPresent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IsEndorsementKeyPairPresent* \[ à\]
</dt> <dd>

Type : **booléen**

Si la **valeur est true**, la paire de clés de type EK existe sur l’appareil.

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
</dt> <dt>

[**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
