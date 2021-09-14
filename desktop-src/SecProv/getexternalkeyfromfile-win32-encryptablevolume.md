---
description: Retourne la clé externe à partir d’un fichier.
ms.assetid: b61b71fb-af6f-4fe3-859b-a9f2f42ca6d2
title: Méthode GetExternalKeyFromFile de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFromFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: ba0c2cf4744c12143090488d730a1d49bab9b431
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193751"
---
# <a name="getexternalkeyfromfile-method-of-the-win32_encryptablevolume-class"></a>Méthode GetExternalKeyFromFile de la \_ classe Win32 EncryptableVolume

La méthode **GetExternalKeyFromFile** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) retourne la clé externe à partir d’un fichier créé par [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md), en fonction de l’emplacement de ce fichier.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetExternalKeyFromFile(
  [in]  string PathWithFileName,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PathWithFileName* \[ dans\]
</dt> <dd>

Type : **chaîne**

Chaîne qui spécifie l’emplacement du fichier contenant une clé externe.

</dd> <dt>

*ExternalKey* \[ à\]
</dt> <dd>

Type : **UInt8 \[ \]**

Tableau d’octets qui est la clé externe 256 bits contenue dans le fichier qui peut être utilisé pour déverrouiller un volume.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                   | Description                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | La méthode a réussi.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>           | Le fichier ne contient pas de clé externe.<br/>  |
| <dl> <dt>**Erreur \_ FICHIER \_ \_ introuvable**</dt> <dt>2147942402 (0x80070002)</dt> </dl> | Impossible de trouver le fichier à l’emplacement spécifié.<br/> |



 

## <a name="remarks"></a>Notes

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

 

 
