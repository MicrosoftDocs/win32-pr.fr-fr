---
description: Récupère le nom du fournisseur de services de chiffrement (CSP).
ms.assetid: b06d2839-0eaa-4f3f-99f7-d77e001fe4ea
title: PrivateKey. ProviderName, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ProviderName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 528117db072b80ab6d9203b8b2fc2786175499ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120854"
---
# <a name="privatekeyprovidername-property"></a>PrivateKey. ProviderName, propriété

\[La propriété **providerName** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**propriété X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **providerName** récupère le nom du fournisseur de [*services de chiffrement*](../secgloss/c-gly.md) (CSP).

## <a name="syntax"></a>Syntaxe


```VB
PrivateKey.ProviderName As String
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne qui contient le nom du fournisseur de services de chiffrement.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
