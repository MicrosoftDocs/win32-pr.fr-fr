---
description: Crée un volume BitLocker avec le type de système de fichiers spécifié du volume de détection.
ms.assetid: 088e7224-a336-4742-a12f-86755defe16c
title: Méthode PrepareVolume de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PrepareVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 67b36703883825d4144037c54ffb55c00308ed1cfb8ee3e4b074d75d63bf7390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891545"
---
# <a name="preparevolume-method-of-the-win32_encryptablevolume-class"></a>Méthode PrepareVolume de la \_ classe Win32 EncryptableVolume

La méthode **PrepareVolume** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) crée un volume BitLocker avec le type de système de fichiers spécifié du volume de détection. Cette méthode doit être appelée pour que le volume puisse être protégé avec l’une des méthodes **ProtectKeyWith \*** .

## <a name="syntax"></a>Syntaxe

```mof
uint32 PrepareVolume(
  [in] string DiscoveryVolumeType,
  [in] uint32 ForceEncryptionType
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*DiscoveryVolumeType* \[ dans\]
</dt> <dd>

Type : **chaîne**

Chaîne qui spécifie le type de volume de détection.

| Valeur               | Signification                                                            |
|---------------------|--------------------------------------------------------------------|
| **&lt;None&gt;**    | Aucun volume de détection. Cette valeur crée un volume BitLocker natif. |
| **&lt;valeurs&gt;** | Cette valeur est le comportement par défaut.                                |
| **FAT32**           | Cette valeur crée un volume de détection FAT32.                       |

</dd> <dt>

*ForceEncryptionType* \[ dans\]
</dt> <dd>

Type : **UInt32**

Entier qui spécifie le type de chiffrement. Il peut s’agir de l’une des valeurs suivantes.

| Valeur                                                                                                                                                                                                                                       | Signification                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <dt>0</dt> <dt>**non spécifié**</dt> </dl> | Le type de chiffrement n’est pas spécifié.<br/> |
| <span id="Software"></span><span id="software"></span><span id="SOFTWARE"></span><dl> <dt>**Logiciel**</dt> <dt>1</dt> </dl>             | Chiffrement logiciel.<br/>                  |
| <span id="Hardware"></span><span id="hardware"></span><span id="HARDWARE"></span><dl> <dt>**Matériel**</dt> <dt>2</dt> </dl>             | Chiffrement matériel.<br/>                  |

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.

| Code/valeur de retour      | Description                     |
|------------------------|---------------------------------|
| **S_OK** <br/> 0 (0x0) | La méthode a réussi.<br/> |

## <a name="remarks"></a>Remarques

Si vous n’appelez pas cette méthode lors de l’activation d’un volume BitLocker, elle revient à appeler cette méthode avec la valeur par défaut dans le paramètre *DiscoveryVolumeType* .

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7 Entreprise, Windows 7 Édition Intégrale des \[ applications de bureau uniquement\]<br/>                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                 |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
