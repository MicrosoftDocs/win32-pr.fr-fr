---
description: Si le Module de plateforme sécurisée (TPM) (TPM) est disponible, cette méthode sécurise la clé de chiffrement du volume.
ms.assetid: 79bee9ca-c86a-482b-a06f-1cfb887e7fae
title: Méthode ProtectKeyWithTPM de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPM
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0369e44d96a4f1dcacf33dbf1b1da6ad6d37eed2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008984"
---
# <a name="protectkeywithtpm-method-of-the-win32_encryptablevolume-class"></a>Méthode ProtectKeyWithTPM de la \_ classe Win32 EncryptableVolume

La méthode **ProtectKeyWithTPM** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) sécurise la clé de chiffrement du volume à l’aide du matériel de sécurité module de plateforme sécurisée (TPM) (TPM) sur l’ordinateur, le cas échéant.

Un protecteur de clé de type « TPM » est créé pour le volume, s’il n’en existe pas déjà un.

Cette méthode s’applique uniquement au volume qui contient le système d’exploitation en cours d’exécution et si un protecteur de clé n’existe pas déjà sur le volume.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ProtectKeyWithTPM(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FriendlyName* \[ dans, facultatif\]
</dt> <dd>

Type : **chaîne**

Chaîne qui spécifie un identificateur de chaîne assigné par l’utilisateur pour ce protecteur de clé. Si ce paramètre n’est pas spécifié, une valeur vide est utilisée.

</dd> <dt>

*PlatformValidationProfile* \[ dans, facultatif\]
</dt> <dd>

Type : **UInt8 \[ \]**

Tableau d’entiers qui spécifie la façon dont le matériel de sécurité du Module de plateforme sécurisée (TPM) (TPM) de l’ordinateur sécurise la clé de chiffrement du volume de disque.

Un profil de validation de plateforme se compose d’un ensemble d’index de registre de configuration de plateforme (PCR) compris entre 0 et 23 inclus. Les valeurs de répétition dans le paramètre sont ignorées. Chaque index PCR est associé à des services qui s’exécutent au démarrage du système d’exploitation. Chaque fois que l’ordinateur démarre, le module de plateforme sécurisée vérifie que les services que vous avez spécifiés dans le profil de validation de plateforme n’ont pas changé. Si l’un de ces services change alors que la protection Chiffrement de lecteur BitLocker (BDE) est toujours activée, le module de plateforme sécurisée ne libère pas la clé de chiffrement pour déverrouiller le volume de disque et l’ordinateur passe en mode de récupération.

Si ce paramètre est spécifié alors que le paramètre de stratégie de groupe correspondant a été activé, il doit correspondre au paramètre stratégie de groupe.

Si ce paramètre n’est pas spécifié, la valeur par défaut 0, 2, 4, 5, 8, 9, 10 et 11 est utilisée. Le profil de validation de plateforme par défaut protège la clé de chiffrement contre les modifications apportées à la racine principale de l’approbation de mesure (CRTM). le BIOS et les extensions de plateforme (PCR 0), le code d’option ROM (PCR 2), le code d’enregistrement de démarrage principal (PCR 4), la table de partition MBR (Master Boot Record) (PCR 5), le secteur de démarrage NTFS (PCR 8), le code de démarrage NTFS (PCR 9),  le gestionnaire de démarrage (PCR 10) et le Chiffrement de lecteur BitLocker Access Control (PCR 11). Pour la sécurité de votre ordinateur, nous vous recommandons le profil par défaut. Les ordinateurs basés sur Unified Extensible Firmware Interface (UEFI) n’utilisent pas la PCR 5 par défaut. Pour bénéficier d’une protection supplémentaire contre les changements de configuration de démarrage précoces, utilisez un profil de PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.

La modification du profil par défaut affecte la sécurité et la facilité de gestion de votre ordinateur. La sensibilité de BitLocker aux modifications de la plateforme (malveillantes ou autorisées) est augmentée ou réduite en fonction de l’inclusion ou de l’exclusion, respectivement, du PCR. Pour que la protection BitLocker soit activée, le profil de validation de plateforme doit inclure PCR 11.



| Valeur                                                                         | Signification                                                                             |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Racine principale de l’approbation des extensions de mesure (CRTM), du BIOS et de la plateforme.<br/> |
| <dl> <dt>1</dt> </dl>  | Configuration et données de la plateforme et de la carte mère<br/>                          |
| <dl> <dt>2</dt> </dl>  | Code option ROM<br/>                                                          |
| <dl> <dt>3</dt> </dl>  | Configuration et données de la ROM optionnelle<br/>                                        |
| <dl> <dt>4</dt> </dl>  | Code d’enregistrement de démarrage principal (MBR)<br/>                                            |
| <dl> <dt>5</dt> </dl>  | Table de partition d’enregistrement de démarrage principal (MBR)<br/>                                 |
| <dl> <dt>6</dt> </dl>  | Événements de transition d’État et de mise en éveil<br/>                                         |
| <dl> <dt>7</dt> </dl>  | Ordinateur Manufacturer-Specific<br/>                                           |
| <dl> <dt>8</dt> </dl>  | Secteur de démarrage NTFS<br/>                                                         |
| <dl> <dt>9</dt> </dl>  | Code de démarrage NTFS<br/>                                                           |
| <dl> <dt>10</dt> </dl> | Gestionnaire de démarrage<br/>                                                             |
| <dl> <dt>11</dt> </dl> | Chiffrement de lecteur BitLocker Access Control<br/>                                |
| <dl> <dt>12</dt> </dl> | Défini pour être utilisé par le système d’exploitation statique<br/>                           |
| <dl> <dt>13</dt> </dl> | Défini pour être utilisé par le système d’exploitation statique<br/>                           |
| <dl> <dt>14</dt> </dl> | Défini pour être utilisé par le système d’exploitation statique<br/>                           |
| <dl> <dt>15</dt> </dl> | Défini pour être utilisé par le système d’exploitation statique<br/>                           |
| <dl> <dt>16</dt> </dl> | Utilisé pour le débogage<br/>                                                       |
| <dl> <dt>17</dt> </dl> | CRTM dynamique<br/>                                                             |
| <dl> <dt>19</dt> </dl> | Plateforme définie<br/>                                                         |
| <dl> <dt>19</dt> </dl> | Utilisé par le système d’exploitation approuvé<br/>                                         |
| <dl> <dt>20</dt> </dl> | Utilisé par le système d’exploitation approuvé<br/>                                         |
| <dl> <dt>21</dt> </dl> | Utilisé par le système d’exploitation approuvé<br/>                                         |
| <dl> <dt>22</dt> </dl> | Utilisé par le système d’exploitation approuvé<br/>                                         |
| <dl> <dt>23</dt> </dl> | Prise en charge des applications<br/>                                                      |



 

</dd> <dt>

*VolumeKeyProtectorID* \[ à\]
</dt> <dd>

Type : **chaîne**

Chaîne qui identifie de façon unique le protecteur créé et qui peut être utilisée pour gérer le protecteur de clé.

Si le lecteur prend en charge le chiffrement matériel et que BitLocker n’a pas pris possession de la bande, la chaîne d’ID est définie sur « BitLocker » et le protecteur de clé est écrit dans les métadonnées par bande.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                         | Description                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                         | La méthode a réussi.<br/>                                                                                                                                              |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>        | Le volume est verrouillé.<br/>                                                                                                                                                   |
| <dl> <dt>**Tbs \_ \_Service E \_ non \_ exécuté**</dt> <dt>2150121480 (0x80284008)</dt> </dl> | Aucun module de plateforme sécurisée compatible n’a été trouvé sur cet ordinateur.<br/>                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME étranger**</dt> <dt>2150694947 (0x80310023)</dt> </dl>       | Le module de plateforme sécurisée ne peut pas sécuriser la clé de chiffrement du volume car le volume ne contient pas le système d’exploitation en cours d’exécution.<br/>                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                 | Le paramètre *PlatformValidationProfile* est fourni, mais ses valeurs ne sont pas comprises dans la plage connue, ou il ne correspond pas au paramètre stratégie de groupe actuellement en vigueur.<br/> |
| <dl> <dt>**FVE \_ Le \_ protecteur E \_ existe**</dt> <dt>2150694961 (0x80310031)</dt> </dl>            | Un protecteur de clé de ce type existe déjà.<br/>                                                                                                                             |



 

## <a name="security-considerations"></a>Considérations relatives à la sécurité

Pour la sécurité de votre ordinateur, nous vous recommandons le profil par défaut. Pour bénéficier d’une protection supplémentaire contre les changements de configuration de démarrage précoces, utilisez un profil de PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.

La modification du profil par défaut affecte la sécurité ou l’utilisation de votre ordinateur.

## <a name="remarks"></a>Remarques

Au plus un protecteur de clé de type « TPM » peut exister pour un volume à tout moment. Si vous souhaitez modifier le nom complet ou le profil de validation de plateforme utilisé par un protecteur de clé « TPM » existant, vous devez d’abord supprimer le protecteur de clé existant, puis appeler **ProtectKeyWithTPM** pour en créer un nouveau.

Pour les index PCR de 0 à 5, les mesures actuelles dans les registres sont utilisées pour protéger la clé de chiffrement. Pour les valeurs PCR de 8 à 11, les mesures utilisées sont celles attendues au cours du prochain cycle de démarrage.

Des protecteurs de clé supplémentaires doivent être spécifiés pour déverrouiller le volume dans les scénarios de récupération où l’accès à la clé de chiffrement du volume ne peut pas être obtenu. par exemple, lorsque le module de plateforme sécurisée ne peut pas être validé avec le profil de validation de plateforme. Utilisez [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) ou [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) pour créer un ou plusieurs protecteurs de clé pour la récupération d’un volume autrement verrouillé.

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

[**\_TPM Win32**](win32-tpm.md)
</dt> </dl>

 

 
