---
description: Génère une chaîne de vérification de certificat à partir d’un certificat de fin vers le certificat racine approuvé et retourne une valeur booléenne qui indique la validité globale de la chaîne.
ms.assetid: 878f09ba-d79b-4f14-b4f6-ecb54771f56f
title: 'IChain2 :: Build, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.Build
- IChain2.Build
- IChain.Build
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66ad51d94fdbd361a34e25b4b76289139abb87f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537341"
---
# <a name="ichain2build-method"></a>IChain2 :: Build, méthode

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode de **génération** génère une chaîne de vérification de certificat à partir d’un certificat de fin vers le [*certificat racine*](../secgloss/r-gly.md) approuvé et retourne une valeur booléenne qui indique la validité globale de la chaîne.

## <a name="syntax"></a>Syntaxe


```VB
Chain.Build( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Certificat* \[ dans\]
</dt> <dd>

Objet de [**certificat**](certificate.md) qui représente le certificat final sur lequel la chaîne de vérification doit être générée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Valeur booléenne qui indique la validité globale de la chaîne. La validité globale est basée sur la stratégie de vérification de validité en place.

## <a name="remarks"></a>Notes

La chaîne est créée à l’aide de la propriété [**CertificateStatus. CheckFlag**](certificatestatus-checkflag.md) , ainsi que des stratégies d’application et de certificat spécifiées par un objet [**CertificateStatus**](certificatestatus.md) . La collection retournée est triée ; le premier certificat de la collection, **certificats. Item**(1), est le certificat de fin de la chaîne. Le dernier certificat de la collection, Certificates **. Item**(**Certificates. Count**), est le [*certificat racine*](../secgloss/r-gly.md) de la chaîne. **Certificats. Item**(0) représente la chaîne entière.

Chaque fois que la méthode **chain. Build** est appelée, l' [*État*](../secgloss/s-gly.md) de l’objet [**chaîne**](chain.md) est réinitialisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> <dt>

[**Mutation**](chain.md)
</dt> </dl>

 

 
