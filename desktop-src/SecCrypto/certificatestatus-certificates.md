---
description: Définit ou récupère la collection de certificats qui peuvent être utilisés pour créer la chaîne de certificats.
ms.assetid: cdf378f9-0d71-4dd9-93cc-85f09a51c5fc
title: CertificateStatus. Certificates, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b049338bd741281c5b7f012fe4ae7ae443cc2c4b6f9dd7f29591e7616fb8b5dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770386"
---
# <a name="certificatestatuscertificates-property"></a>CertificateStatus. Certificates, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**structure X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **certificats** définit ou récupère la collection de certificats qui peuvent être utilisés pour créer la chaîne de certificats.

## <a name="syntax"></a>Syntaxe


```VB
CertificateStatus.Certificates As Certificates
```



## <a name="property-value"></a>Valeur de la propriété

Objet de [**certificats**](certificates.md) qui représente la collection de certificats qui peut être utilisée pour générer la chaîne de certificats.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,1 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
