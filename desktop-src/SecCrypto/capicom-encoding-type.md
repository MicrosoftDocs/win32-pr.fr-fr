---
description: Indique le type d’encodage utilisé.
ms.assetid: 13e78a5e-3a31-44de-b249-28e360e1e087
title: Énumération CAPICOM_ENCODING_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCODING_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: a546831d6e88b3e35706df59adabe0627ad9fccb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121130"
---
# <a name="capicom_encoding_type-enumeration"></a>\_Énumération de type d’encodage CAPICOM \_

Le type d’énumération de **\_ \_ type d’encodage CAPICOM** indique le type d’encodage utilisé.

## <a name="members"></a>Membres



| Membre                      | Description                                                                                                                                                                                 | Valeur      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **\_coder \_ tout**    | Les données sont enregistrées sous la forme d’une chaîne codée en base64 ou d’une séquence binaire pure. Ce type d’encodage est utilisé uniquement pour les données d’entrée dont le type d’encodage est inconnu. Introduit dans CAPICOM 2,0.<br/> | 0xffffffff |
| **\_Encode \_ Base64** | Les données sont enregistrées sous la forme d’une chaîne encodée en base64.<br/>                                                                                                                                        | 0          |
| **codage d’un \_ \_ fichier binaire CAPICOM** | Les données sont enregistrées sous la forme d’une séquence binaire pure.<br/>                                                                                                                                         | 1          |



## <a name="remarks"></a>Notes

Ce type d’énumération est utilisé par les méthodes et propriétés CAPICOM suivantes :

-   [**Certificate. Export,**](certificate-export.md) méthode
-   [**EncodedData. Value**](encodeddata-value.md) (propriété)
-   [**EncryptedData. Encrypt,**](encrypteddata-encrypt.md) méthode
-   [**EnvelopedData. Encrypt,**](envelopeddata-encrypt.md) méthode
-   [**ExtendedProperty. Value**](extendedproperty-value.md) (propriété)
-   [**SignedData. Sign,**](signeddata-sign.md) méthode
-   [**SignedData. cosign,**](signeddata-cosign.md) méthode
-   [**Store. Export,**](store-export.md) méthode
-   Méthode [**Utilities. GetRandom**](utilities-getrandom.md)

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




