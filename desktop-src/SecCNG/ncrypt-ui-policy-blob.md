---
description: Utilisé avec la \_ propriété de propriété de stratégie d’interface utilisateur NCRYPT \_ \_ pour contenir les informations d’interface utilisateur pour une clé.
ms.assetid: c567d8ba-3315-4316-8e09-93b2c10a55ec
title: Structure de NCRYPT_UI_POLICY_BLOB (ncrypt \_ Provider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NCRYPT_UI_POLICY_BLOB
api_type:
- HeaderDef
api_location:
- Ncrypt_provider.h
ms.openlocfilehash: 21f9f6c0f6956ffa89da45c9dcd23727c0b3cea2d4f31131713f9ed5a0c3a2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907599"
---
# <a name="ncrypt_ui_policy_blob-structure"></a>\_Structure d' \_ \_ objet blob de stratégie d’interface utilisateur NCRYPT

La structure d' **\_ \_ \_ objet blob de stratégie d’interface utilisateur ncrypt** est utilisée avec la propriété de [**\_ \_ \_ propriété de stratégie**](key-storage-property-identifiers.md) d’interface utilisateur ncrypt pour contenir les informations d’interface utilisateur d’une clé.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct __NCRYPT_UI_POLICY_BLOB {
  DWORD dwVersion;
  DWORD dwFlags;
  DWORD cbCreationTitle;
  DWORD cbFriendlyName;
  DWORD cbDescription;
} NCRYPT_UI_POLICY_BLOB;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwVersion**
</dt> <dd>

Numéro de version de la structure. Ce membre doit contenir 1.

</dd> <dt>

**dwFlags**
</dt> <dd>

Ensemble d’indicateurs qui fournissent des informations supplémentaires sur l’interface utilisateur ou des spécifications.



| Valeur                                                                                                                                                                                                                                                                                                  | Signification                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="NCRYPT_UI_PROTECT_KEY_FLAG"></span><span id="ncrypt_ui_protect_key_flag"></span><dl> <dt>**NCRYPT \_ \_Indicateur de \_ clé \_ Protect UI**</dt> <dt>0x00000001</dt> </dl>                                | Affichez l’interface utilisateur de clé forte si nécessaire.<br/> |
| <span id="NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG"></span><span id="ncrypt_ui_force_high_protection_flag"></span><dl> <dt>**NCRYPT \_ \_Indicateur de \_ \_ protection élevée \_ de force d’interface utilisateur**</dt> <dt>0x00000002</dt> </dl> | Forcez la protection élevée.<br/>                           |



 

</dd> <dt>

**cbCreationTitle**
</dt> <dd>

Longueur, en octets, du titre de création. Le titre de création est une chaîne Unicode terminée par le caractère null qui spécifie le texte utilisé comme titre de la boîte de dialogue clé forte lorsque la clé est terminée. Le titre de création doit être placé immédiatement après la structure d' **\_ \_ \_ objet blob de stratégie d’interface utilisateur NCRYPT** . Si la valeur du membre **cbCreationTitle** est définie sur 0, un titre de création par défaut est utilisé pour le titre de la boîte de dialogue clé forte. Ce membre est utilisé uniquement lors de la finalisation de la clé.

</dd> <dt>

**cbFriendlyName**
</dt> <dd>

Longueur, en octets, du nom convivial de la clé. Le nom convivial est une chaîne Unicode se terminant par un caractère null qui contient le texte affiché dans la boîte de dialogue clé forte comme nom de la clé. Le nom convivial doit être placé immédiatement après le titre de création dans cet objet BLOB. Si la valeur du membre **cbFriendlyName** est définie sur 0, un nom par défaut est utilisé dans la boîte de dialogue clé forte. Ce membre est utilisé à la fois lorsque la clé est terminée et lorsque la clé est utilisée.

</dd> <dt>

**cbDescription**
</dt> <dd>

Longueur, en octets, de la description de la clé. La description de clé est une chaîne Unicode se terminant par un caractère null qui contient le texte affiché dans la boîte de dialogue clé forte comme description de la clé. La valeur de description doit être placée immédiatement après le nom convivial dans cet objet BLOB. Si la valeur du membre **cbDescription** est définie sur 0, une description par défaut est utilisée dans la boîte de dialogue clé forte. Ce membre est utilisé à la fois lorsque la clé est terminée et lorsque la clé est utilisée.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est incluse dans l' \_ en-tête du fournisseur ncrypt. h. Pour utiliser la structure, vous devez télécharger le [Kit de développement du fournisseur de services de chiffrement](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) à partir de Microsoft connecter.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                          |
| En-tête<br/>                   | <dl> <dt>\_Fournisseur ncrypt. h</dt> </dl> |



 

