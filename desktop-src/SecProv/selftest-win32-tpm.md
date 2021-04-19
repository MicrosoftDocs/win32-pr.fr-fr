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
ms.openlocfilehash: 8681ee8ca49b8b2f7de550ffc5baa0ff8c0c9470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515626"
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

 

 
