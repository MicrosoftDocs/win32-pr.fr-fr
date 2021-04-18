---
description: Importe un certificat précédemment encodé à partir d’une chaîne dans l’objet certificat.
ms.assetid: 8515e034-08aa-4575-9b96-34cdee3ccba8
title: 'ICertificate2 :: import, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Import
- ICertificate2.Import
- ICertificate.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ea639f1cd89b673ecf8da77302e3d812894a202b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526028"
---
# <a name="icertificate2import-method"></a>ICertificate2 :: import, méthode

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **Import** importe un certificat précédemment encodé à partir d’une chaîne dans l’objet [**certificat**](certificate.md) . L’appel de cette méthode réinitialise l' [*État*](../secgloss/s-gly.md) de cet objet.

## <a name="syntax"></a>Syntaxe


```VB
Certificate.Import( _
  ByVal EncodedCertificate _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*EncodedCertificate* \[ dans\]
</dt> <dd>

Chaîne qui contient les données de certificat encodées à importer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

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

 

 
