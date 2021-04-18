---
description: Modifie les informations d’identification d’autorisation du propriétaire de l’appareil TPM. Les anciens et nouveaux mots de passe d’autorisation du propriétaire sont requis.
ms.assetid: 5b7f1aec-5181-4330-982c-d80a1d5ae9e8
title: Méthode ChangeOwnerAuth de la classe CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.ChangeOwnerAuth
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2d5a2895e6a0049b2284b55aea1dc9a1849341c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519848"
---
# <a name="changeownerauth-method-of-the-cim_tpm-class"></a>Méthode ChangeOwnerAuth de la \_ classe TPM CIM

Modifie les informations d’identification d’autorisation du propriétaire de l’appareil TPM. Les anciens et nouveaux mots de passe d’autorisation du propriétaire sont requis.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ChangeOwnerAuth(
  [in] string OldOwnerAuth,
  [in] string NewOwnerAuth
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*OldOwnerAuth* \[ dans\]
</dt> <dd>

Représente les anciennes informations d’identification d’autorisation du propriétaire requises pour prendre possession du périphérique TPM. La sous-classe **CIM \_ SharedCredential** peut être requise avec la valeur non null du **\_ SharedCredential CIM**.**Propriété secrète** pour le paramètre.

</dd> <dt>

*NewOwnerAuth* \[ dans\]
</dt> <dd>

Représente les informations d’identification d’autorisation du nouveau propriétaire requises pour prendre possession du périphérique TPM. La sous-classe **CIM \_ SharedCredential** peut être requise avec la valeur non null du **\_ SharedCredential CIM**.**Propriété secrète** pour le paramètre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite ; Sinon, retourne une erreur.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> <dt>

**Erreur inconnue/non spécifiée** (2)
</dt> <dt>

**DMTF réservé** (3.. 4095)
</dt> <dt>

**Méthode réservée** (4096.. 32767)
</dt> <dt>

**Fournisseur spécifié** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TPM CIM**](cim-tpm.md)
</dt> </dl>

 

 




