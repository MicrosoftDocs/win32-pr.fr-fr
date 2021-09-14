---
description: Indique si le mot de passe numérique répond aux exigences de format spéciales pour cette valeur d’authentification.
ms.assetid: 3995405f-db4d-4f72-98dc-133a09f9cf65
title: Méthode IsNumericalPasswordValid de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsNumericalPasswordValid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7cec4aa31ae9ff6aee90c0f46ded935b3d553783
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237324"
---
# <a name="isnumericalpasswordvalid-method-of-the-win32_encryptablevolume-class"></a>Méthode IsNumericalPasswordValid de la \_ classe Win32 EncryptableVolume

La méthode **IsNumericalPasswordValid** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) indique si le mot de passe numérique répond aux exigences de format spéciales pour cette valeur d’authentification.

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsNumericalPasswordValid(
  [in]  string  NumericalPassword,
  [out] boolean IsNumericalPasswordValid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NumericalPassword* \[ dans\]
</dt> <dd>

Type : **chaîne**

Chaîne qui spécifie le mot de passe numérique.

Le mot de passe numérique doit contenir 48 chiffres. Ces chiffres peuvent être divisés en 8 groupes de 6 chiffres, le dernier chiffre de chaque groupe indiquant une valeur de somme de contrôle pour le groupe. Chaque groupe de 6 chiffres doit être divisible par 11 et doit être inférieur à 720896. En supposant qu’un groupe de six chiffres s’intitule x1, x2, x3, x4, x5 et x6, le chiffre de la somme de contrôle x6 est calculé comme-x1 + x2 – x3 + x4 – x5 Mod 11.

Les groupes de chiffres peuvent éventuellement être séparés par un espace ou un trait d’Union. Par conséquent, « XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX » ou « xxxxxx XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX » peut également contenir des mots de passe numériques valides.

</dd> <dt>

*IsNumericalPasswordValid* \[ à\]
</dt> <dd>

Type : **booléen**

Valeur booléenne qui est true si le mot de passe numérique remplit les conditions de format spéciales pour cette valeur d’authentification ; sinon, la valeur est false.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | La méthode a réussi.<br/> |



 

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

 

 
