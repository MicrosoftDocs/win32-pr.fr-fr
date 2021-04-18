---
description: Ajoute un objet certificat à la collection.
ms.assetid: 0973018d-1e83-41b4-a250-7dd5be2fb664
title: 'ICertificates2 :: Add, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Add
- ICertificates2.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d56120c6f584e828c3aadca037d75263d5350f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528912"
---
# <a name="icertificates2add-method"></a>ICertificates2 :: Add, méthode

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **Add** ajoute un objet [**certificat**](certificate.md) à la collection. Cette méthode est introduite dans CAPICOM 2,0.

## <a name="syntax"></a>Syntaxe


```VB
Certificates.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Certificat* \[ dans\]
</dt> <dd>

Objet de [**certificat**](certificate.md) à ajouter à la collection.

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



 

 
