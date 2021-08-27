---
description: Active ou reprend tous les protecteurs de clés désactivés ou suspendus.
ms.assetid: 6f5a17a3-84f2-43a0-a85f-1037cd52439a
title: Méthode EnableKeyProtectors de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d90e37f800a9c224abefb21253f7e74c2bc08401
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474925"
---
# <a name="enablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Méthode EnableKeyProtectors de la \_ classe Win32 EncryptableVolume

La méthode **EnableKeyProtectors** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) active ou reprend tous les protecteurs de clés désactivés ou suspendus. Vous pouvez utiliser cette méthode pour réactiver ou reprendre la protection BitLocker sur un volume chiffré. Cette méthode garantit que la clé de chiffrement du volume n’est pas exposée en clair sur le disque dur.

> [!Note]  
> Si le disque prend en charge le chiffrement matériel, l’état de la bande passe à « déverrouillé » de « toujours déverrouillé ».

 

## <a name="syntax"></a>Syntaxe


```mof
uint32 EnableKeyProtectors();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.

Si les protecteurs de clé sont déjà activés et qu’aucune autre erreur ne se produit, cette méthode retourne zéro.




| Code/valeur de retour | Description | 
|-------------------|-------------|
| <dl><dt><strong>S_OK</strong></dt><dt>0 (0x0)</dt></dl> | La méthode a réussi.<br /> | 
| <dl><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt><dt>2150694919 (0x80310007)</dt></dl> | Aucun protecteur de clé n’existe sur le volume. Utilisez l’une des méthodes suivantes pour spécifier les protecteurs de clé pour le volume :<br /><ul><li><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></li><li><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></li><li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li><li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li><li><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></li><li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li><li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li><li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li><li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li></ul> | 
| <dl><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt><dt>2150694920 (0x80310008)</dt></dl> | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br /> | 




 

## <a name="remarks"></a>Remarques

Si le volume est entièrement chiffré, l’exécution de cette méthode permet de s’assurer que le volume est protégé. Si le volume est partiellement chiffré, l’exécution de cette méthode implique que le volume sera protégé lorsqu’il deviendra entièrement chiffré. Pour plus d’informations, consultez la méthode [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) .

Si des protecteurs de clés basés sur le module de plateforme sécurisée existent pour le volume, l’exécution correcte de cette méthode actualise également ces protecteurs afin que le module de plateforme sécurisée valide les services de démarrage actuels sur la plateforme. En d’autres termes, vous déclarez que l’état actuel de l’ordinateur est l’état correct que le module de plateforme sécurisée doit vérifier par rapport aux redémarrages futurs de l’ordinateur.

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
</dt> <dt>

[**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)
</dt> </dl>

 

 
