---
description: Effectue un test automatique du module de plateforme sécurisée et retourne le résultat.
ms.assetid: 0f8fdb68-80b1-4fc4-beb9-e87f51b85031
title: Méthode SelfTest de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.SelfTest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 42e0cf4e458be4ff95c05086d603f64d17fb7ff3c3da5a6781529d4632627f75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891374"
---
# <a name="selftest-method-of-the-win32_tpm-class"></a>Méthode SelfTest de la \_ classe TPM Win32

La méthode **SelfTest** de la [**classe \_ TPM Win32**](win32-tpm.md) effectue un test automatique du module de plateforme sécurisée et retourne le résultat.

Un auto-test TPM s’exécute automatiquement au démarrage de l’ordinateur.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SelfTest(
  [out] uint8 SelfTestResult[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SelfTestResult* \[ à\]
</dt> <dd>

Type : **UInt8 \[ \]**

Tableau d’octets qui contient le résultat de l’auto-test. Le format de ce paramètre est spécifique au fabricant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.

Le tableau suivant répertorie certains des codes de retour courants.



| Code/valeur de retour                                                                                                                                 | Description                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | La méthode a été exécutée avec succès.<br/> |



 

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

 

 
