---
description: Indique si le volume et sa clé de chiffrement sont sécurisés.
ms.assetid: bcd8fce5-da39-4aa8-93ff-0768deb900ec
title: Méthode GetProtectionStatus de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetProtectionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 66fcbcfc4c5f228fde786a6b9d8913cc69c0d341
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237371"
---
# <a name="getprotectionstatus-method-of-the-win32_encryptablevolume-class"></a>Méthode GetProtectionStatus de la \_ classe Win32 EncryptableVolume

La méthode **GetProtectionStatus** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) indique si le volume et sa clé de chiffrement (le cas échéant) sont sécurisés.

La protection est désactivée si un volume n’est pas chiffré ou partiellement chiffré, ou si la clé de chiffrement du volume est disponible en clair sur le disque dur.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetProtectionStatus(
  [out] uint32 ProtectionStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ProtectionStatus* \[ à\]
</dt> <dd>

Type : **UInt32**

Spécifie si le volume et la clé de chiffrement (le cas échéant) sont sécurisés.




| Valeur | Signification | 
|-------|---------|
| <span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span><dl><dt><strong>Non protégé</strong></dt><dt>0</dt></dl> | PROTECTION DÉSACTIVÉE<br /> Pour un disque dur standard :<br /> Le volume n’est pas chiffré, partiellement chiffré ou la clé de chiffrement du volume est disponible en clair sur le disque dur. La clé de chiffrement est disponible en clair sur le disque dur si les protecteurs de clé ont été désactivés à l’aide de la méthode <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> ou si aucun protecteur de clé n’a été spécifié à l’aide des méthodes suivantes :<ul><li><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></li><li><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></li><li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li><li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li><li><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></li><li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li><li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li><li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li><li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li></ul><br /> Pour un EHDD :<br /> La bande du volume est déverrouillée de façon permanente, n’a pas de gestionnaire de clés ou est gérée par un gestionnaire de clés tiers.<br /> Cela peut également signifier que la bande est gérée par BitLocker mais que la méthode <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> a été appelée et que le lecteur est suspendu.<br /> | 
| <span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span><dl><dt><strong>Protégé</strong></dt><dt>1</dt></dl> | PROTECTION ACTIVÉE<br /> Pour un disque dur standard :<br /> Le volume est entièrement chiffré et la clé de chiffrement du volume n’est pas disponible en clair sur le disque dur.<br /> Pour un EHDD :<br /> BitLocker est le gestionnaire de clés de la bande. Le lecteur peut être verrouillé ou déverrouillé, mais ne peut pas être déverrouillé de façon permanente.<br /> | 
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl><dt><strong>Inconnu</strong></dt><dt>2</dt></dl> | Impossible de déterminer l’état de la protection du volume. Cela peut être dû au fait que le volume est dans un état verrouillé.<br /><strong>Windows vista Ultimate, Windows vista Enterprise et Windows Server 2008 :</strong> Cette valeur n’est pas prise en charge. cette valeur est prise en charge à partir de Windows 7 et Windows Server 2008 R2.<br /> | 




 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Notes

Vous pouvez chiffrer un volume uniquement si vous appelez [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) en premier ou utilisez l’une des méthodes suivantes :

-   [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Par conséquent, si le disque est chiffré et que *ProtectionStatus* retourne la valeur zéro (protection désactivée), les clés sont désactivées.

Utilisez [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md) pour répertorier les protecteurs de clé qui ont été spécifiés pour sécuriser la clé de chiffrement du volume. Si les protecteurs de clé existent mais que la protection est égale à zéro (PROTECTION désactivée), utilisez [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) pour activer la protection du volume.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Spécifications



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

 

 
