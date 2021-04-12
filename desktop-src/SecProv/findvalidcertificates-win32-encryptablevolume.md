---
description: Énumère tous les certificats sur le système qui correspondent aux critères indiqués et retourne une liste d’empreintes numériques.
ms.assetid: 69522afe-9870-4ae9-8c69-cf8787913615
title: Méthode FindValidCertificates de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.FindValidCertificates
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 69612d860284f6a47dfa38c2aafc3e73f209c796
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319878"
---
# <a name="findvalidcertificates-method-of-the-win32_encryptablevolume-class"></a>Méthode FindValidCertificates de la \_ classe Win32 EncryptableVolume

La méthode **FindValidCertificates** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) énumère tous les certificats du système qui correspondent aux critères indiqués et retourne une liste d’empreintes numériques. La liste retournée contient uniquement des certificats avec un [*identificateur d’objet*](../secgloss/o-gly.md) (OID) valide. L’OID peut être la valeur par défaut ou il peut être spécifié dans la stratégie de groupe.

## <a name="syntax"></a>Syntaxe


```mof
uint32 FindValidCertificates(
  [out] string CertificateThumbprint[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CertificateThumbprint* \[ à\]
</dt> <dd>

Type : **chaîne \[ \]**

Tableau de chaînes qui contient la liste des certificats valides.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                           | Description                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                           | La méthode a réussi.<br/>                |
| <dl> <dt>**FVE \_ E \_ \_ \_ OID BitLocker 2150695022 non valide**</dt> <dt>(0x8031006E)</dt> </dl> | L’OID BitLocker disponible n’est pas valide.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]<br/>                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                 |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
