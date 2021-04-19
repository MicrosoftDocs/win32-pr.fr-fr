---
description: Utilise le fourni Active Directory chaîne d’identificateur de sécurité (SID) pour obtenir la clé dérivée et déverrouiller le volume chiffré.
ms.assetid: 89FBC815-859D-415A-8F26-170FB2DB7387
title: Méthode UnlockWithAdSid de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: cbd2a327a2ede322c01009fe32aa0492a7e65610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518896"
---
# <a name="unlockwithadsid-method-of-the-win32_encryptablevolume-class"></a>Méthode UnlockWithAdSid de la \_ classe Win32 EncryptableVolume

La méthode **UnlockWithAdSid** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) utilise le fourni Active Directory chaîne d’identificateur de sécurité (SID) pour obtenir la clé dérivée et déverrouiller le volume chiffré.

> [!Note]  
> Si le disque prend en charge le chiffrement matériel, cette fonction définit l’état de la bande sur « déverrouillé ».

 

## <a name="syntax"></a>Syntaxe


```mof
uint32 UnlockWithAdSid(
  [in]  string SidString
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SidString* \[ dans\]
</dt> <dd>

Chaîne qui contient le SID Active Directory.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Notes

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

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

 

 
