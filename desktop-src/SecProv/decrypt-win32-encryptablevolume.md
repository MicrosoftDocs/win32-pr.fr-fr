---
description: Commence le déchiffrement d’un volume entièrement chiffré ou reprend le déchiffrement d’un volume partiellement chiffré.
ms.assetid: 3cdbb1c1-1084-4ddb-ba8d-fc2e3ec75224
title: Méthode Decrypt de la classe Win32_EncryptableVolume (InfoCard. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Decrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 96f7ab1c237879d83be25ddb54425ac31fcb855d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118866"
---
# <a name="decrypt-method-of-the-win32_encryptablevolume-class"></a>Méthode Decrypt de la \_ classe EncryptableVolume Win32

La méthode **Decrypt** de la classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) commence le déchiffrement d’un volume entièrement chiffré, ou reprend le déchiffrement d’un volume partiellement chiffré.

Quand le déchiffrement est suspendu ou en cours, cette méthode se comporte comme [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md). Lorsque le chiffrement est suspendu ou en cours, cette méthode annule le chiffrement et commence le déchiffrement. Une fois le déchiffrement terminé, tous les protecteurs de clé sur ce volume sont supprimés du système et le volume est converti en système de fichiers NTFS standard.

> [!Note]  
> Si le disque est chiffré sur le matériel, la méthode de **déchiffrement** définit l’état de la bande sur « toujours déverrouillé », supprime toutes les métadonnées associées et met à zéro l’ID de sécurité du lecteur.

 

## <a name="syntax"></a>Syntaxe


```mof
uint32 Decrypt();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.

Cette méthode est retournée immédiatement. Si le volume est déjà entièrement déchiffré et qu’aucune autre erreur n’existe, cette méthode retourne 0.



| Code/valeur de retour                                                                                                                                                                       | Description                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | La méthode a réussi.<br/>                                                                                                                                                                                                   |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>      | Le volume est verrouillé.<br/>                                                                                                                                                                                                        |
| <dl> <dt>**FVE \_ \_Désactivation du \_ déverrouillage d’E**</dt> /t <dt>2150694953 (0x80310029)</dt> </dl> | Impossible de déchiffrer ce volume, car les clés utilisées pour déverrouiller automatiquement les volumes de données sont disponibles. <br/> Utilisez [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) pour supprimer ces clés.<br/> |



 

## <a name="security-considerations"></a>Considérations relatives à la sécurité

L’appel de la méthode de **déchiffrement** laisse les données non protégées.

Si l’état de protection du volume est égal à 1 (PROTECTION activée) avant l’utilisation de cette méthode, l’exécution correcte de cette méthode modifie l’état de la protection en 0 (PROTECTION désactivée), car par définition un volume partiellement chiffré n’est pas protégé.

## <a name="remarks"></a>Notes

Si le volume n’est pas déjà entièrement déchiffré, l’exécution de **Decrypte** fait en sorte que [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indique que le déchiffrement est en cours et affiche le pourcentage du volume qui reste chiffré.

Si l’état de protection du volume est « activé » avant l’exécution de cette méthode, l’exécution de cette méthode remplace l’état de protection par « désactivé », car par définition, un volume partiellement chiffré n’est pas protégé.

Si cette méthode est exécutée sur le volume du système d’exploitation en cours d’exécution et que ce volume du système d’exploitation est utilisé pour déverrouiller automatiquement les volumes de données (consultez la méthode [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)), vous devez d’abord appeler la méthode [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md).

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows vista Enterprise, Windows les applications de bureau vista Ultimate \[ uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| En-tête<br/>                   | <dl> <dt>InfoCard. h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
