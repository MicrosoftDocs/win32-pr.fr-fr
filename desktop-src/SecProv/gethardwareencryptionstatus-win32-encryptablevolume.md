---
description: Détermine si le volume se trouve sur un lecteur qui prend en charge ou peut prendre en charge le chiffrement matériel.
ms.assetid: C6007BC4-71CD-404A-A0E9-D9662906151F
title: Méthode GetHardwareEncryptionStatus de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareEncryptionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2f48bb7115d19779f437a849078238cee967f2d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516633"
---
# <a name="gethardwareencryptionstatus-method-of-the-win32_encryptablevolume-class"></a>Méthode GetHardwareEncryptionStatus de la \_ classe Win32 EncryptableVolume

La méthode **GetHardwareEncryptionStatus** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) détermine si le volume se trouve sur un lecteur qui prend en charge ou peut prendre en charge le chiffrement matériel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetHardwareEncryptionStatus(
  [out] uint32 HardwareEncryptionStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HardwareEncryptionStatus* \[ à\]
</dt> <dd>

Spécifie si le lecteur peut prendre en charge le chiffrement matériel. Il peut s’agir de l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                               | Signification                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="Not_supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <dt>**Non pris en charge**</dt> <dt>0</dt> </dl> | Le chiffrement matériel n’est pas pris en charge.<br/>    |
| <span id="No_protection"></span><span id="no_protection"></span><span id="NO_PROTECTION"></span><dl> <dt>**Aucune protection**</dt> <dt>1</dt> </dl> | Le chiffrement du lecteur n’est pas pris en charge.<br/>       |
| <span id="Uses_software"></span><span id="uses_software"></span><span id="USES_SOFTWARE"></span><dl> <dt>**Utilise le logiciel**</dt> <dt>2</dt> </dl> | La méthode de chiffrement est basée sur logiciel.<br/> |
| <span id="Uses_hardware"></span><span id="uses_hardware"></span><span id="USES_HARDWARE"></span><dl> <dt>**Utilise le matériel**</dt> <dt>3</dt> </dl> | Le lecteur prend en charge le chiffrement matériel.<br/>  |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne la valeur zéro (0) si le volume est compatible avec le chiffrement matériel BitLocker. Dans le cas contraire, la fonction retourne une erreur.



| Code/valeur de retour                                                                                                                                 | Description                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Le volume est compatible avec le chiffrement matériel BitLocker.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 entreprise, applications de bureau Windows 8 professionnel \[ uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 




