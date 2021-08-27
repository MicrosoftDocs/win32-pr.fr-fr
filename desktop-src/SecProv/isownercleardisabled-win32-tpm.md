---
description: La méthode IsOwnerClearDisabled de la \_ classe TPM Win32 indique si le propriétaire de l’appareil est limité à l’effacement de l’appareil.
ms.assetid: 04f98e9b-c1a0-4828-b7cb-67b32d7470ea
title: Méthode IsOwnerClearDisabled de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnerClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 639804b21c97a6e445c0eddc9253c46774a4ccd895d58bfe32289432702cbe03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080629"
---
# <a name="isownercleardisabled-method-of-the-win32_tpm-class"></a>Méthode IsOwnerClearDisabled de la \_ classe TPM Win32

La méthode **IsOwnerClearDisabled** de la [**classe \_ TPM Win32**](win32-tpm.md) indique si le propriétaire de l’appareil est limité à l’effacement de l’appareil.

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsOwnerClearDisabled(
  [out] boolean IsOwnerClearDisabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IsOwnerClearDisabled* \[ à\]
</dt> <dd>

Type : **booléen**

Si la **valeur est true**, le propriétaire de l’appareil ne peut pas effacer l’appareil. Seul un utilisateur physiquement présent peut être en mesure de supprimer l’appareil. Si la **valeur est false**, le propriétaire de l’appareil peut effacer l’appareil.

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
</dt> </dl>

 

 
