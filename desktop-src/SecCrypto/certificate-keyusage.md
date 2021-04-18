---
description: Retourne un objet KeyUsage qui indique l’utilisation valide de la clé du certificat.
ms.assetid: e4590e95-ffa2-4953-bfc1-4d7c70271029
title: 'ICertificate2 :: KeyUsage, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.KeyUsage
- ICertificate2.KeyUsage
- ICertificate.KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85fe008880d9613586d38dba7afaca39bb29f72f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526668"
---
# <a name="icertificate2keyusage-method"></a>ICertificate2 :: KeyUsage, méthode

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **KeyUsage** retourne un objet [**KeyUsage**](keyusage.md) qui indique l’utilisation valide de la clé du certificat.

## <a name="syntax"></a>Syntaxe


```VB
Certificate.KeyUsage()
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

[Objets de chiffrement](cryptography-objects.md)
</dt> <dt>

[**Certificat**](certificate.md)
</dt> </dl>

 

 
