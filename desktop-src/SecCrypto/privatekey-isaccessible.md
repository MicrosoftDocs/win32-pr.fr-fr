---
description: Retourne une valeur booléenne qui indique si la clé privée est accessible.
ms.assetid: ee5e89af-745e-4a4d-9943-fecbaee5d3e3
title: Méthode PrivateKey. IsAccessible
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsAccessible
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9997fad702ab1eddbf4c60fa2304df8185ef4c63
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120890"
---
# <a name="privatekeyisaccessible-method"></a>Méthode PrivateKey. IsAccessible

\[La méthode **IsAccessible** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Utilisez plutôt la [**propriété X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **IsAccessible** retourne une valeur booléenne qui indique si la clé privée est accessible.

## <a name="syntax"></a>Syntaxe


```VB
PrivateKey.IsAccessible()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Si la valeur est true, la clé privée est accessible.

## <a name="remarks"></a>Notes

La valeur de retour de cette méthode dépend du [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) utilisé. Cette méthode renvoie une valeur fiable si un fournisseur de services de chiffrement Microsoft est utilisé. Si le fournisseur de services de chiffrement n’est pas un fournisseur de services de chiffrement Microsoft, la valeur de retour ne peut pas être approuvée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
