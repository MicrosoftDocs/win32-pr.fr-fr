---
description: Détermine si le certificat a une clé privée qui lui est associée. La méthode détermine cela en vérifiant si la propriété de l’ID de la clé de certificat \_ \_ Prov \_ info \_ prop \_ est présente.
ms.assetid: 80478956-1ed7-4c25-9ae3-d7176649e6d7
title: 'ICertificate2 :: HasPrivateKey, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.HasPrivateKey
- ICertificate2.HasPrivateKey
- ICertificate.HasPrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 43110e48a1172977ad979d6ec2d94c5b8e3ffc50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523488"
---
# <a name="icertificate2hasprivatekey-method"></a>ICertificate2 :: HasPrivateKey, méthode

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **HasPrivateKey** détermine si le [*certificat*](../secgloss/c-gly.md) a une [*clé privée*](../secgloss/p-gly.md) qui lui est associée. La méthode détermine cela en vérifiant si la propriété de l’ID de la clé de certificat \_ \_ Prov \_ info \_ prop \_ est présente.

## <a name="syntax"></a>Syntaxe


```VB
Certificate.HasPrivateKey()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PrivateKey. Open**](privatekey-open.md)
</dt> <dt>

[Objets de chiffrement](cryptography-objects.md)
</dt> <dt>

[**Certificat**](certificate.md)
</dt> </dl>

 

 
