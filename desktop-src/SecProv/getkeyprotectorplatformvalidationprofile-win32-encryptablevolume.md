---
description: Récupère le profil de validation de plateforme pour un protecteur de clé donné du type approprié.
ms.assetid: 45fa6ba7-169c-4753-8586-0029a7650acc
title: Méthode GetKeyProtectorPlatformValidationProfile de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorPlatformValidationProfile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 9563fc306bd8d50ce4f0c13164640ecee8e99d441b1b923df35cce8615097c8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667789"
---
# <a name="getkeyprotectorplatformvalidationprofile-method-of-the-win32_encryptablevolume-class"></a>Méthode GetKeyProtectorPlatformValidationProfile de la \_ classe Win32 EncryptableVolume

La méthode **GetKeyProtectorPlatformValidationProfile** récupère le profil de validation de plateforme pour un protecteur de clé donné du type approprié.

L’identificateur de protecteur de clé doit faire référence à un protecteur de clé de type « TPM », « TPM et PIN », « TPM et PIN et clé de démarrage », ou « TPM et clé de démarrage ».

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetKeyProtectorPlatformValidationProfile(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PlatformValidationProfile[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VolumeKeyProtectorID* \[ dans\]
</dt> <dd>

Type : **chaîne**

Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.

</dd> <dt>

*PlatformValidationProfile* \[ à\]
</dt> <dd>

Type : **UInt8 \[ \]**

Tableau d’entiers qui spécifie la façon dont le matériel de sécurité Module de plateforme sécurisée (TPM) (TPM) de l’ordinateur sécurise la clé de chiffrement du volume de disque.



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



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                  | Description                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | La méthode a réussi.<br/>                                                                                                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un protecteur de clé de type « TPM », « TPM et pin », « TPM et pin et clé de démarrage », ou « TPM et clé de démarrage ».<br/> |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker.<br/>                                                                                  |



 

## <a name="remarks"></a>Remarques

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

 

 
