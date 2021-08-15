---
description: Si le Module de plateforme sécurisée (TPM) (TPM) est disponible, cette méthode sécurise la clé de chiffrement du volume améliorée par un numéro d’identification personnel spécifié par l’utilisateur.
ms.assetid: 8c4c434a-dd60-491a-a983-b3fa78c91c0d
title: Méthode ProtectKeyWithTPMAndPIN de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndPIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0eab283a0eaec97d7f7c9e03cf8d8064e08e0e25bea606b393fb35a38143f7fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891404"
---
# <a name="protectkeywithtpmandpin-method-of-the-win32_encryptablevolume-class"></a>Méthode ProtectKeyWithTPMAndPIN de la \_ classe Win32 EncryptableVolume

La méthode **ProtectKeyWithTPMAndPIN** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) sécurise la clé de chiffrement du volume à l’aide du matériel de sécurité module de plateforme sécurisée (TPM) (TPM) de l’ordinateur, s’il est disponible, amélioré par un code confidentiel (pin) spécifié par l’utilisateur, qui doit être fourni à l’ordinateur au démarrage.

La validation par le module de plateforme sécurisée et l’entrée de la chaîne d’identification personnelle sont nécessaires pour accéder à la clé de chiffrement du volume et déverrouiller le contenu du volume.

Cette méthode s’applique uniquement au volume qui contient le système d’exploitation en cours d’exécution.

Un protecteur de clé de type « TPM et PIN » est créé pour le volume, s’il n’en existe pas déjà un.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ProtectKeyWithTPMAndPIN(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in]           string PIN,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FriendlyName* \[ dans, facultatif\]
</dt> <dd>

Type : **chaîne**

Identificateur de chaîne affecté à l’utilisateur pour ce protecteur de clé. Si ce paramètre n’est pas spécifié, une valeur vide est utilisée.

</dd> <dt>

*PlatformValidationProfile* \[ dans, facultatif\]
</dt> <dd>

Type : **UInt8 \[ \]**

Tableau d’entiers qui spécifie la façon dont le matériel de sécurité du Module de plateforme sécurisée (TPM) (TPM) de l’ordinateur sécurise la clé de chiffrement du volume de disque.

Un profil de validation de plateforme se compose d’un ensemble d’index de registre de configuration de plateforme (PCR) compris entre 0 et 23 inclus. Les valeurs de répétition dans le paramètre sont ignorées. Chaque index PCR est associé à des services qui s’exécutent au démarrage du système d’exploitation. Chaque fois que l’ordinateur démarre, le module de plateforme sécurisée vérifie que les services que vous avez spécifiés dans le profil de validation de plateforme n’ont pas changé. Si l’un de ces services change alors que la protection Chiffrement de lecteur BitLocker (BDE) est toujours activée, le module de plateforme sécurisée ne libère pas la clé de chiffrement pour déverrouiller le volume de disque, et l’ordinateur passe en mode de récupération.

Si ce paramètre est spécifié alors que le paramètre de stratégie de groupe correspondant a été activé, il doit correspondre au paramètre stratégie de groupe.

Si ce paramètre n’est pas spécifié, la valeur par défaut 0, 2, 4, 5, 8, 9, 10 et 11 est utilisée. Le profil de validation de plateforme par défaut protège la clé de chiffrement contre les modifications apportées aux éléments suivants :

-   Racine principale de l’approbation de mesure (CRTM)
-   BIOS
-   Extensions de plateforme (PCR 0)
-   Code option ROM (PCR 2)
-   Code d’enregistrement de démarrage principal (PCR 4)
-   Table de partition d’enregistrement de démarrage principal (DDL) (PCR 5)
-   Secteur de démarrage NTFS (PCR 8)
-   Bloc de démarrage NTFS (PCR 9)
-   Gestionnaire de démarrage (PCR 10)
-   Access Control BitLocker (PCR 11)

Pour la sécurité de votre ordinateur, nous vous recommandons le profil par défaut. Pour bénéficier d’une protection supplémentaire contre les changements de configuration de démarrage précoces, utilisez un profil de PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11. Les ordinateurs basés sur Unified Extensible Firmware Interface (UEFI) n’utilisent pas la PCR 5 par défaut.

La modification du profil par défaut affecte la sécurité et la facilité de gestion de votre ordinateur. La sensibilité de BitLocker aux modifications de la plateforme (malveillantes ou autorisées) est augmentée ou réduite en fonction de l’inclusion ou de l’exclusion, respectivement, du PCR. Pour que la protection BitLocker soit activée, le profil de validation de plateforme doit inclure PCR 11.



| Valeur                                                                         | Signification                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Racine principale de l’approbation de la mesure (CRTM), du BIOS et des extensions de plateforme<br/> |
| <dl> <dt>1</dt> </dl>  | Configuration et données de la plateforme et de la carte mère<br/>                         |
| <dl> <dt>2</dt> </dl>  | Code option ROM<br/>                                                         |
| <dl> <dt>3</dt> </dl>  | Configuration et données de la ROM optionnelle<br/>                                       |
| <dl> <dt>4</dt> </dl>  | Code d’enregistrement de démarrage principal (MBR)<br/>                                           |
| <dl> <dt>5</dt> </dl>  | Table de partition d’enregistrement de démarrage principal (MBR)<br/>                                |
| <dl> <dt>6</dt> </dl>  | Événements de transition d’État et de mise en éveil<br/>                                        |
| <dl> <dt>7</dt> </dl>  | Ordinateur Manufacturer-Specific<br/>                                          |
| <dl> <dt>8</dt> </dl>  | Secteur de démarrage NTFS<br/>                                                        |
| <dl> <dt>9</dt> </dl>  | Bloc de démarrage NTFS<br/>                                                         |
| <dl> <dt>10</dt> </dl> | Gestionnaire de démarrage<br/>                                                            |
| <dl> <dt>11</dt> </dl> | Access Control BitLocker<br/>                                                |
| <dl> <dt>12</dt> </dl> | Défini pour être utilisé par le système d’exploitation statique<br/>                          |
| <dl> <dt>13</dt> </dl> | Défini pour être utilisé par le système d’exploitation statique<br/>                          |
| <dl> <dt>14</dt> </dl> | Défini pour être utilisé par le système d’exploitation statique<br/>                          |
| <dl> <dt>15</dt> </dl> | Défini pour être utilisé par le système d’exploitation statique<br/>                          |
| <dl> <dt>16</dt> </dl> | Utilisé pour le débogage<br/>                                                      |
| <dl> <dt>17</dt> </dl> | CRTM dynamique<br/>                                                            |
| <dl> <dt>19</dt> </dl> | Plateforme définie<br/>                                                        |
| <dl> <dt>19</dt> </dl> | Utilisé par un système d’exploitation approuvé<br/>                                      |
| <dl> <dt>20</dt> </dl> | Utilisé par un système d’exploitation approuvé<br/>                                      |
| <dl> <dt>21</dt> </dl> | Utilisé par un système d’exploitation approuvé<br/>                                      |
| <dl> <dt>22</dt> </dl> | Utilisé par un système d’exploitation approuvé<br/>                                      |
| <dl> <dt>23</dt> </dl> | Prise en charge des applications<br/>                                                     |



 

</dd> <dt>

*Code confidentiel* \[ dans\]
</dt> <dd>

Type : **chaîne**

Chaîne d’identification personnelle spécifiée par l’utilisateur. Cette chaîne doit être composée d’une séquence de 6 à 20 chiffres ou, si la stratégie de groupe « autoriser les codes confidentiels améliorés pour le démarrage » est activée, de 6 à 20 lettres, des symboles, des espaces ou des nombres.

</dd> <dt>

*VolumeKeyProtectorID* \[ à\]
</dt> <dd>

Type : **chaîne**

Identificateur de chaîne unique mis à jour utilisé pour gérer un protecteur de clé de volume chiffré.

Si le lecteur prend en charge le chiffrement matériel et que BitLocker n’a pas pris possession de la bande, la chaîne d’ID est définie sur « BitLocker » et le protecteur de clé est écrit dans les métadonnées par bande.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                                | Description                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                | La méthode a réussi.<br/>                                                                                                                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                        | Le paramètre *PlatformValidationProfile* est fourni, mais ses valeurs ne sont pas comprises dans la plage connue, ou il ne correspond pas au paramètre stratégie de groupe actuellement en vigueur.<br/> |
| <dl> <dt>**FVE \_ E \_ amorçable \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt> </dl>              | Un CD/DVD de démarrage est détecté sur cet ordinateur. Retirez le CD/DVD et redémarrez l’ordinateur.<br/>                                                                                 |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME étranger**</dt> <dt>2150694947 (0x80310023)</dt> </dl>              | Le module de plateforme sécurisée ne peut pas sécuriser la clé de chiffrement du volume car le volume ne contient pas le système d’exploitation en cours d’exécution.<br/>                                            |
| <dl> <dt>**FVE \_ E \_ \_ \_ caractères pin non valides**</dt> <dt>2150695066 (0x8031009A)</dt> </dl>          | Le paramètre *NewPIN* contient des caractères qui ne sont pas valides. Lorsque l’stratégie de groupe « autoriser les codes confidentiels améliorés au démarrage » est désactivée, seuls les nombres sont pris en charge.<br/>          |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>               | Le volume est verrouillé.<br/>                                                                                                                                                    |
| <dl> <dt>**FVE \_ \_Longueur de \_ \_ code confidentiel \_ non valide pour la stratégie E**</dt> <dt>2150695016 (0x80310068)</dt> </dl> | Le paramètre *NewPIN* fourni comporte plus de 20 caractères, moins de 6 caractères, ou une valeur inférieure à la longueur minimale spécifiée par stratégie de groupe.<br/>            |
| <dl> <dt>**FVE \_ Le \_ protecteur E \_ existe**</dt> <dt>2150694961 (0x80310031)</dt> </dl>            | Un protecteur de clé de ce type existe déjà.<br/>                                                                                                                             |
| <dl> <dt>**Tbs \_ \_Service E \_ non \_ exécuté**</dt> <dt>2150121480 (0x80284008)</dt> </dl>        | Aucun module de plateforme sécurisée compatible n’a été trouvé sur cet ordinateur.<br/>                                                                                                                             |



 

## <a name="security-considerations"></a>Considérations relatives à la sécurité

Pour la sécurité de votre ordinateur, nous vous recommandons le profil par défaut. Pour bénéficier d’une protection supplémentaire contre les modifications du code de démarrage anticipé, utilisez un profil de PCR 0, 2, 4, 5, 8, 9, 10 et 11. Pour bénéficier d’une protection supplémentaire contre les changements de configuration de démarrage précoces, utilisez un profil de PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.

La modification du profil par défaut affecte la sécurité ou l’utilisation de votre ordinateur.

## <a name="remarks"></a>Remarques

Au plus un protecteur de clé de type « TPM et PIN » peut exister pour un volume à tout moment. Si vous souhaitez modifier le nom complet ou le profil de validation de plateforme utilisé par un protecteur de clé « TPM et PIN » existant, vous devez d’abord supprimer le protecteur de clé existant, puis appeler **ProtectKeyWithTPMAndPIN** pour en créer un nouveau.

Des protecteurs de clé supplémentaires doivent être spécifiés pour déverrouiller le volume dans les scénarios de récupération où l’accès à la clé de chiffrement du volume ne peut pas être obtenu. par exemple, lorsque le module de plateforme sécurisée ne peut pas être validé avec le profil de validation de plateforme ou que le code confidentiel est perdu.

Utilisez [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) ou [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) pour créer un ou plusieurs protecteurs de clé pour la récupération d’un volume autrement verrouillé.

Bien qu’il soit possible d’avoir à la fois un protecteur de clé du type « TPM » et un autre du type « TPM et PIN », la présence du type de protecteur de clé « TPM » nie les effets des autres protecteurs de clés basés sur le module de plateforme sécurisée.

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

 

 
