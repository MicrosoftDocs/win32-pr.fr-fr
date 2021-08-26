---
description: Reprend le chiffrement ou le déchiffrement d’un volume.
ms.assetid: e37f3e32-5510-431e-9782-11908e65300d
title: Méthode ResumeConversion de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ResumeConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e1b3908f77b72f7f9a5ca0583193784ba054a50ab59aa63dad1c13b9f03317e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992669"
---
# <a name="resumeconversion-method-of-the-win32_encryptablevolume-class"></a>Méthode ResumeConversion de la \_ classe Win32 EncryptableVolume

La méthode **ResumeConversion** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) reprend le chiffrement ou le déchiffrement d’un volume.

> [!Note]  
> Si le disque prend en charge le chiffrement matériel, cette fonction peut reprendre une opération de nettoyage uniquement. Pour plus d’informations, consultez [**PauseConversion**](pauseconversion-win32-encryptablevolume.md).

 

## <a name="syntax"></a>Syntaxe


```mof
uint32 ResumeConversion();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.

Si cette méthode est utilisée sur un volume entièrement chiffré ou entièrement déchiffré, ou si le chiffrement/déchiffrement est déjà en cours sur le volume, la valeur 0 est retournée en supposant qu’aucune autre erreur ne se produise.



| Code/valeur de retour                                                                                                                                                                  | Description                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | La méthode a réussi.<br/> |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Le volume est verrouillé.<br/>      |



 

## <a name="remarks"></a>Remarques

Si cette méthode est utilisée sur un volume avec chiffrement/déchiffrement suspendu, l’exécution correcte de cette méthode amène [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) à indiquer que le chiffrement ou le déchiffrement est en cours.

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

 

 
