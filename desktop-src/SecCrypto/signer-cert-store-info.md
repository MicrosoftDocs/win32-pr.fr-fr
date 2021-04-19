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
ms.openlocfilehash: 197bd4855a7d2afec4c0b23662365e5f9197e302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518546"
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

Optionnel. Handle d’un magasin de certificats supplémentaire.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**certificat du signataire \_**](signer-cert.md)
</dt> </dl>

 

 




