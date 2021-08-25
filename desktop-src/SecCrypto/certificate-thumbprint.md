---
description: Récupère une chaîne hexadécimale qui contient le hachage SHA-1 du certificat.
ms.assetid: 6fd6f3ba-f7a9-43a3-a8da-8fd826649a92
title: Propriété Certificate. empreinte
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Thumbprint
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 64748f3eb8b9623ea7c07a7428f29b30276c34ab38631fdbf210b25b5be92a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878159"
---
# <a name="certificatethumbprint-property"></a>Propriété Certificate. empreinte

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété d' **empreinte numérique** récupère une chaîne hexadécimale qui contient le hachage [*SHA-1*](../secgloss/s-gly.md) du certificat.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Certificate.Thumbprint As String
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne hexadécimale qui contient le hachage SHA-1 du certificat.

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

 

 
