---
description: Retourne la version des métadonnées FVE du volume.
ms.assetid: 21d5bf6d-c613-4200-b35c-1bad1ee72ec7
title: Méthode GetVersion de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetVersion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 25952c29b6db6db045fe839951d76994cc907b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544640"
---
# <a name="getversion-method-of-the-win32_encryptablevolume-class"></a>Méthode GetVersion de la \_ classe EncryptableVolume Win32

La méthode **GetVersion** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) retourne la version de métadonnées FVE du volume.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetVersion(
  [out] uint32 Version
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Version* \[ de à\]
</dt> <dd>

Type : **UInt32**

Entier non signé qui indique la version des métadonnées du volume.



| Valeur                                                                                                                                                                                                                       | Signification                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Inconnu**</dt> <dt>0</dt> </dl> | Le système d’exploitation est inconnu.<br/>                                                                                                                                                                                               |
| <span id="Vista"></span><span id="vista"></span><span id="VISTA"></span><dl> <dt>**Vista**</dt> <dt>1</dt> </dl>         | Format Windows Vista, ce qui signifie que le volume a été protégé avec BitLocker sur un ordinateur exécutant Windows Vista.<br/>                                                                                                                |
| <span id="Win7"></span><span id="win7"></span><span id="WIN7"></span><dl> <dt>**Win7**</dt> <dt>2</dt> </dl>             | Format Windows 7, ce qui signifie que le volume a été protégé avec BitLocker sur un ordinateur exécutant Windows 7 ou que le format des métadonnées a été mis à niveau à l’aide de la méthode [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md) .<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.

Si le volume est déjà déverrouillé et qu’aucune autre erreur ne se produit, cette méthode retourne zéro.



| Code/valeur de retour                                                                                                                                                       | Description                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                       | S_OK<br/>                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt> </dl> | La valeur du paramètre de *version* n’est pas valide.<br/> |
| <dl> <dt>**Erreur \_ \_Données non valides**</dt> <dt>13 (0xD)</dt> </dl>       | Le pilote a renvoyé un format de données non pris en charge.<br/>     |



 

## <a name="remarks"></a>Notes

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]<br/>                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                 |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
