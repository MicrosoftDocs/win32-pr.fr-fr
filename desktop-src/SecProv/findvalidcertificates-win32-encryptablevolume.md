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
ms.openlocfilehash: da642ff24fa01d27c74a30af7de6c7f91e33a712a28c47644a7044f43c40d586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892437"
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
| Client minimal pris en charge<br/> | Windows 7 Entreprise, Windows 7 Édition Intégrale des \[ applications de bureau uniquement\]<br/>                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                 |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
