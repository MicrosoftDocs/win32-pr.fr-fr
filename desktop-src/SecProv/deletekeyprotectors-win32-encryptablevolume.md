---
description: Supprime tous les protecteurs de clé du volume.
ms.assetid: 46f61899-87ff-4e86-8409-635117cff4de
title: Méthode DeleteKeyProtectors de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 49884566a45bde4977d56baa3e83ae4c42fdd676447a3da1f3df528ec823c414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004607"
---
# <a name="deletekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Méthode DeleteKeyProtectors de la \_ classe Win32 EncryptableVolume

La méthode **DeleteKeyProtectors** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) supprime tous les protecteurs de clé du volume.

Si un volume non chiffré possède des protecteurs de clés, lorsque **DeleteKeyProtectors** est exécuté correctement, le volume revient à un système de fichiers NTFS standard.

Si le volume n’est pas encore complètement déchiffré, utilisez [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) avant d’exécuter **DeleteKeyProtectors** pour vous assurer que les parties chiffrées du volume restent accessibles.

## <a name="syntax"></a>Syntaxe


```mof
uint32 DeleteKeyProtectors();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                          | Description                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                          | La méthode a réussi.<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>         | Le volume est verrouillé.<br/>                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ \_Clé E \_ requise**</dt> <dt>2150694941 (0x8031001D)</dt> </dl>          | Le dernier protecteur de clé pour un volume partiellement ou entièrement chiffré ne peut pas être supprimé si les protecteurs de clé sont activés. Utilisez [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) avant de supprimer ce dernier protecteur de clé pour vous assurer que les parties chiffrées du volume restent accessibles. <br/> |
| <dl> <dt>**FVE \_ \_Limite de volume E \_ \_ déjà**</dt> <dt>2150694943 (0x8031001F)</dt> </dl> | Les protecteurs de clé ne peuvent pas être supprimés, car l’un d’eux est utilisé pour déverrouiller automatiquement le volume. <br/> Utilisez [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) pour désactiver le déverrouillage automatique avant d’exécuter cette méthode.<br/>                                                       |



 

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

 

 
