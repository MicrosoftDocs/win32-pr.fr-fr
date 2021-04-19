---
description: Retourne une valeur booléenne qui indique si la clé privée appartient à un jeu de clés d’ordinateur.
ms.assetid: ea13ba68-30ae-4aa4-b490-29fd4542c621
title: Méthode PrivateKey. IsMachineKeyset
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsMachineKeyset
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a42e3f932b8294d9671b7901437151d9fbbe5a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537713"
---
# <a name="privatekeyismachinekeyset-method"></a>Méthode PrivateKey. IsMachineKeyset

\[La méthode **IsMachineKeyset** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Utilisez plutôt la [**propriété X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **IsMachineKeyset** retourne une valeur booléenne qui indique si la clé privée appartient à un jeu de clés d’ordinateur.

## <a name="syntax"></a>Syntaxe


```VB
PrivateKey.IsMachineKeyset()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si la valeur est true, la clé privée appartient à un jeu de clés d’ordinateur.

## <a name="remarks"></a>Notes

La valeur de retour de cette méthode dépend du [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) utilisé. Cette méthode renvoie une valeur fiable si un fournisseur de services de chiffrement Microsoft est utilisé. Si le fournisseur de services de chiffrement n’est pas un fournisseur de services de chiffrement Microsoft, la valeur de retour ne peut pas être approuvée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
