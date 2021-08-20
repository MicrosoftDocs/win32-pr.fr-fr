---
description: Spécifie le magasin de certificats utilisé pour signer un document.
ms.assetid: aabad010-6fa3-4677-bd73-b8c52d68dbc8
title: Structure SIGNER_CERT_STORE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT_STORE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 93524f631f9a9a761880eec5ebba5c97c66dcd8a67f85c6260d4598eba1a9764
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973639"
---
# <a name="signer_cert_store_info-structure"></a>Structure d' \_ \_ informations du magasin du certificat du signataire \_

La structure d' **\_ \_ \_ informations du magasin** de certificats du signataire spécifie le magasin de certificats utilisé pour signer un document.

> [!Note]  
> Cette structure n’est définie dans aucun fichier d’en-tête. Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.

 

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _SIGNER_CERT_STORE_INFO {
  DWORD          cbSize;
  PCCERT_CONTEXT pSigningCert;
  DWORD          dwCertPolicy;
  HCERTSTORE     hCertStore;
} SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

Taille, en octets, de la structure.

</dd> <dt>

**pSigningCert**
</dt> <dd>

Pointeur vers une structure [**de \_ contexte**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) de certificat pour le certificat de signature.

</dd> <dt>

**dwCertPolicy**
</dt> <dd>

Spécifie la manière dont les certificats sont ajoutés à la signature. Pour trouver la chaîne de certificats, les magasins MY, CA, ROOT et SPC, en plus du magasin spécifié par le membre **hCertStore** , sont activés. Ce membre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                   | Signification                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <dt>**Signataire \_ \_ \_ Chaîne de stratégie de certificat**</dt> <dt>2 (0X2)</dt> </dl>                           | Ajoutez uniquement des certificats dans la chaîne de certificats.<br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <dt>**Signataire \_ Chaîne de stratégie de certificat \_ \_ \_ non \_ racine**</dt> <dt>8 (0x8)</dt> </dl> | Ajoutez uniquement des certificats dans la chaîne de certificats, à l’exclusion du certificat racine.<br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <dt>**Signataire \_ \_ \_ Magasin de stratégies de certificat**</dt> <dt>1 (0x1)</dt> </dl>                           | Ajoutez tous les certificats dans le magasin spécifié par le membre **hCertStore** . Cet indicateur peut être **une combinaison or au niveau** du bit avec l’une des autres valeurs possibles pour ce membre.<br/> |



 

</dd> <dt>

**hCertStore**
</dt> <dd>

Facultatif. Handle d’un magasin de certificats supplémentaire.

</dd> </dl>

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**certificat du signataire \_**](signer-cert.md)
</dt> </dl>

 

 




