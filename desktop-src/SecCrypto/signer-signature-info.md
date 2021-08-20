---
description: Contient des informations sur une signature numérique.
ms.assetid: 0b86fdf9-533f-4640-8c70-c3c8f4ef2c68
title: Structure SIGNER_SIGNATURE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SIGNATURE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3dc76db36cd752e22bbcd4d2f6672f7359dad882346b764fef0f4d12ef0901f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973393"
---
# <a name="signer_signature_info-structure"></a>Structure des \_ informations de signature du signataire \_

La structure d’informations sur la **\_ \_ signature du signataire** contient des informations sur une signature numérique.

> [!Note]  
> Cette structure n’est définie dans aucun fichier d’en-tête. Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.

 

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _SIGNER_SIGNATURE_INFO {
  DWORD             cbSize;
  ALG_ID            algidHash;
  DWORD             dwAttrChoice;
  union {
    SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
  };
  PCRYPT_ATTRIBUTES psAuthenticated;
  PCRYPT_ATTRIBUTES psUnauthenticated;
} SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

Taille, en octets, de la structure.

</dd> <dt>

**algidHash**
</dt> <dd>

Algorithme de hachage utilisé pour la signature numérique.

</dd> <dt>

**dwAttrChoice**
</dt> <dd>

Spécifie si la signature possède des attributs [*Authenticode*](../secgloss/a-gly.md) . Ce membre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                      | Signification                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_AUTHCODE_ATTR"></span><span id="signer_authcode_attr"></span><dl> <dt>**Signataire \_ FACTEURS \_ attr**</dt> <dt>1</dt> </dl> | La signature possède des attributs [*Authenticode*](../secgloss/a-gly.md) .<br/>           |
| <span id="SIGNER_NO_ATTR"></span><span id="signer_no_attr"></span><dl> <dt>**Signataire \_ AUCUN \_ attr**</dt> <dt>0</dt> </dl>                   | La signature n’a pas d’attributs [*Authenticode*](../secgloss/a-gly.md) .<br/> |



 

</dd> <dt>

**pAttrAuthcode**
</dt> <dd>

Spécifie les attributs d’une signature [*Authenticode*](../secgloss/a-gly.md) . Ce membre est requis si la valeur du membre **dwAttrChoice** est **signer \_ facteurs \_ attr**.

</dd> <dt>

**psAuthenticated**
</dt> <dd>

Attributs authentifiés fournis par l’utilisateur et ajoutés à la signature numérique.

</dd> <dt>

**psUnauthenticated**
</dt> <dd>

Attributs non authentifiés fournis par l’utilisateur ajoutés à la signature numérique.

</dd> </dl>

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
