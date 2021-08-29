---
description: Crée une paire de clés de type EK 2048 bits sur le module de plateforme sécurisée.
ms.assetid: 393f0264-d1e9-4a08-bdaa-475b32d93e05
title: Méthode CreateEndorsementKeyPair de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.CreateEndorsementKeyPair
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 1df4cb87d88956d9066e8d0d00f56df50b2d18b33ae234f597bb028a2eee5322
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668069"
---
# <a name="createendorsementkeypair-method-of-the-win32_tpm-class"></a>Méthode CreateEndorsementKeyPair de la \_ classe TPM Win32

La méthode **CreateEndorsementKeyPair** de la [**classe \_ TPM Win32**](win32-tpm.md) crée une paire de clés de type EK 2048 bits sur le module de plateforme sécurisée. La paire de clés de type EK doit être disponible pour que la méthode [**TakeOwnership**](takeownership-win32-tpm.md) s’exécute correctement. Vous pouvez utiliser la méthode [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md) pour détecter si la clé de type EK existe déjà sur le module de plateforme sécurisée.

## <a name="syntax"></a>Syntaxe


```mof
uint32 CreateEndorsementKeyPair();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.

Le tableau suivant répertorie certains des codes de retour courants.



| Code/valeur de retour                                                                                                                                                                  | Description                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | La méthode a réussi.<br/>                          |
| <dl> <dt> **TPM \_ E \_ désactivé \_ cmd**</dt> <dt>2150105096 (0x80280008)</dt> </dl> | Une paire de clés de type EK existe déjà sur ce module de plateforme sécurisée.<br/> |



 

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

 

 
