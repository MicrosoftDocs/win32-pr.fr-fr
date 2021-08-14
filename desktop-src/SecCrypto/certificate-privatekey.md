---
description: Définit ou récupère la clé privée associée au certificat.
ms.assetid: 976d81b4-5cbe-4824-9087-9a908b0e60e5
title: Propriété Certificate. PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 18e6acc2aa4b765e9219eff479280df814f1089dc27366c5d175dcdeda4fd890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771554"
---
# <a name="certificateprivatekey-property"></a>Propriété Certificate. PrivateKey

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **PrivateKey** définit ou récupère la clé privée associée au certificat. Cette propriété a été introduite dans CAPICOM 2,0.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Certificate.PrivateKey As PrivateKey
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**PrivateKey**](privatekey.md) qui représente la clé privée associée au certificat.

## <a name="remarks"></a>Remarques

La définition de la propriété **PrivateKey** sur Nothing supprime l’association entre la clé privée et le certificat, mais elle ne supprime pas la clé privée. Pour supprimer la clé privée, appelez la méthode [**PrivateKey. Delete**](privatekey-delete.md) , puis affectez à cette propriété la valeur Nothing.

Cette propriété déclenche l’E CAPICOM \_ E \_ non \_ autorisée quand elle est définie à partir d’une application Web.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Certificate**](certificate.md)
</dt> </dl>

 

 
