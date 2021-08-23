---
description: Supprime toutes les clés externes et les informations associées enregistrées sur le volume du système d’exploitation en cours d’exécution et utilisées pour déverrouiller automatiquement les volumes de données.
ms.assetid: a5fef793-0634-493d-b62d-cb842844b1e8
title: Méthode ClearAllAutoUnlockKeys de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ClearAllAutoUnlockKeys
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 46ee3791425afafe63b0d566c3f4204fecc9195f4341b90caee4c95306afdeab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668169"
---
# <a name="clearallautounlockkeys-method-of-the-win32_encryptablevolume-class"></a>Méthode ClearAllAutoUnlockKeys de la \_ classe Win32 EncryptableVolume

La méthode **ClearAllAutoUnlockKeys** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) supprime toutes les clés externes et les informations associées enregistrées sur le volume du système d’exploitation en cours d’exécution et utilisées pour déverrouiller automatiquement les volumes de données.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ClearAllAutoUnlockKeys();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                   | Description                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | La méthode a réussi.<br/>                                                        |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/> |
| <dl> <dt>**FVE \_ E \_ non \_ OS \_ volume**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | La méthode ne peut être exécutée que pour le volume du système d’exploitation en cours d’exécution.<br/>     |



 

## <a name="remarks"></a>Remarques

**ClearAllAutoUnlockKeys** atteint la même fonctionnalité que l’exécution de [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) pour chaque volume de données qui a été associé au système d’exploitation en cours d’exécution, même les volumes de données qui ne sont pas actuellement connectés à l’ordinateur. Elle supprime également toutes les informations de déverrouillage obsolètes associées aux volumes de données qui n’existent plus.

Avant d’appeler le [**déchiffrement**](decrypt-win32-encryptablevolume.md) sur le volume du système d’exploitation en cours d’exécution, utilisez **ClearAllAutoUnlockKeys** pour vous assurer que les informations placées dans le Registre du système d’exploitation pour déverrouiller automatiquement les volumes de données ne sont pas accessibles en clair sur le disque.

Une fois l’exécution de **ClearAllAutoUnlockKeys** réussie, les méthodes [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) ou [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) peuvent être utilisées pour déverrouiller tous les volumes de données de cet ordinateur. Utilisez [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) pour réactiver le déverrouillage automatique d’un volume de données.

Si aucune autre erreur n’est retournée, **ClearAllAutoUnlockKeys** supprime du Registre tous les ID de protecteur de volume et les clés externes utilisés pour déverrouiller automatiquement tout volume de données qui a déjà été associé au volume du système d’exploitation en cours d’exécution.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows vista Enterprise, Windows les applications de bureau vista Ultimate \[ uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
