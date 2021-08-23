---
description: Détermine si les signatures sur les données signées dans l’objet SignedData sont valides.
ms.assetid: 920ac235-0c1a-4b15-9cdd-c7e0c3ea6107
title: SignedData. Verify, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ccda81fc3640d4d09f9644bdf0d84a18a68b743397e1578a5ad434349893e893
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898973"
---
# <a name="signeddataverify-method"></a>SignedData. Verify, méthode

\[La méthode **verify** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La méthode **verify** détermine si les [*signatures*](../secgloss/d-gly.md) sur les données signées dans l’objet [**SignedData**](signeddata.md) sont valides. Pour vérifier une signature, le [*hachage*](../secgloss/h-gly.md) chiffré du contenu est déchiffré à l’aide de la clé publique du signataire à partir du certificat du signataire. Le hachage déchiffré est comparé à un nouveau hachage du contenu des données. Une signature est valide si les hachages correspondent. En outre, cette méthode génère également une chaîne de certificats pour déterminer la validité du certificat qui fournit la [*clé publique*](../secgloss/p-gly.md) utilisée pour déchiffrer le hachage.

## <a name="syntax"></a>Syntaxe


```VB
SignedData.Verify( _
  ByVal SignedMessage, _
  [ ByVal bDetached ], _
  [ ByVal VerifyFlag ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SignedMessage* \[ dans\]
</dt> <dd>

Chaîne qui contient le message signé à vérifier.

</dd> <dt>

*bDetached* \[ dans, facultatif\]
</dt> <dd>

Si la **valeur est true**, les données à signer sont détachées ; autrement dit, le contenu signé n’est pas inclus dans l’objet signé. Pour vérifier la signature sur du contenu détaché, une application doit avoir une copie du contenu d’origine. Le contenu détaché est souvent utilisé pour réduire la taille d’un objet signé à envoyer sur le Web, si le destinataire du message signé contient une copie originale des données signées. La valeur par défaut est **False**.

</dd> <dt>

*VerifyFlag* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’énumération de l' [indicateur de \_ \_ \_ vérification \_ des données signées CAPICOM](capicom-signed-data-verify-flag.md) qui indique la stratégie de vérification. La valeur par défaut est CAPICOM \_ verify \_ signature \_ et \_ Certificate. À l’aide de cette valeur, la validité du certificat et la validité de la signature sont vérifiées. Ce paramètre peut être défini pour vérifier la signature et non le certificat. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                                             | Signification                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_VERIFY_SIGNATURE_ONLY"></span><span id="capicom_verify_signature_only"></span><dl> <dt>**\_signature de vérification CAPICOM \_ \_ uniquement**</dt> </dl>                                   | Seule la signature est vérifiée.<br/>                                                                   |
| <span id="CAPICOM_VERIFY_SIGNATURE_AND_CERTIFICATE"></span><span id="capicom_verify_signature_and_certificate"></span><dl> <dt>**\_vérification \_ de la signature et du \_ \_ certificat de CAPICOM**</dt> </dl> | La signature et la validité du certificat utilisé pour créer la signature sont vérifiées.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne une chaîne qui contient les données signées et encodées.

Si cette méthode échoue, une erreur est levée. L’objet **Err** contient des informations supplémentaires sur l’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
