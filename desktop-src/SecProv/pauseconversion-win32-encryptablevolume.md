---
description: Suspend le chiffrement ou le déchiffrement d’un volume.
ms.assetid: 3c365299-f0e1-480e-ad96-c91bb4108bb2
title: Méthode PauseConversion de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PauseConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1c9756da2339a6a3d8e87466651f61c8ff3f83a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530886"
---
# <a name="pauseconversion-method-of-the-win32_encryptablevolume-class"></a>Méthode PauseConversion de la \_ classe Win32 EncryptableVolume

La méthode **PauseConversion** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) interrompt le chiffrement ou le déchiffrement d’un volume.

> [!Note]  
> Si le disque prend en charge le chiffrement matériel, cette fonction peut suspendre une opération de nettoyage, mais ne peut pas suspendre le chiffrement basé sur le matériel.

 

## <a name="syntax"></a>Syntaxe


```mof
uint32 PauseConversion();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.

Si cette méthode est utilisée sur un volume entièrement chiffré ou entièrement déchiffré, ou si le chiffrement/déchiffrement est déjà suspendu sur le volume, la valeur 0 est retournée en supposant qu’aucune autre erreur ne se produise.



| Code/valeur de retour                                                                                                                                                                  | Description                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | La méthode a réussi.<br/> |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Le volume est verrouillé.<br/>      |



 

## <a name="remarks"></a>Notes

Si cette méthode est utilisée sur un volume avec chiffrement/déchiffrement en cours, l’exécution correcte de cette méthode amène [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) à indiquer que le chiffrement ou le déchiffrement est suspendu.

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
