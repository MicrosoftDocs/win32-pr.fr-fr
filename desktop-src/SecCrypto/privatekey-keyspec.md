---
description: Récupère la spécification de clé.
ms.assetid: 93c909cb-b1d1-4c2b-a66c-9d3f6dd9b340
title: PrivateKey. KeySpec, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.KeySpec
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f9d0ba55ca48d5257a038845f84374544b7615b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120858"
---
# <a name="privatekeykeyspec-property"></a>PrivateKey. KeySpec, propriété

\[La propriété **KeySpec** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Utilisez plutôt la [**propriété X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **KeySpec** récupère la spécification de la clé.

## <a name="syntax"></a>Syntaxe


```VB
PrivateKey.KeySpec As CAPICOM_KEY_SPEC
```



## <a name="property-value"></a>Valeur de la propriété

Valeur de l’énumération des [**\_ \_ spécifications de clé CAPICOM**](capicom-key-spec.md) qui indique la spécification de clé. Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                                        | Signification                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <dt>**clé d’échange de la \_ spécification de clé CAPICOM \_ \_**</dt> </dl> | La clé peut être utilisée pour le chiffrement et la signature.<br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <dt>**SIGNATURE de la \_ spécification de clé CAPICOM \_ \_**</dt> </dl>       | La clé peut être utilisée uniquement pour la signature.<br/>           |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
