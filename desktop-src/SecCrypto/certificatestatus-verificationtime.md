---
description: Définit ou récupère l’heure à laquelle le certificat a été vérifié.
ms.assetid: 1bd17df3-2fa1-4b99-ab00-659b4ad5fcd9
title: CertificateStatus. VerificationTime, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.VerificationTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 178402861c9830efbea78a31081ae7e8b31800b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520372"
---
# <a name="certificatestatusverificationtime-property"></a>CertificateStatus. VerificationTime, propriété

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**structure X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **VerificationTime** définit ou récupère l’heure à laquelle le certificat a été vérifié.

## <a name="syntax"></a>Syntaxe


```VB
CertificateStatus.VerificationTime As Date
```



## <a name="property-value"></a>Valeur de la propriété

Heure à laquelle le certificat a été vérifié.

## <a name="remarks"></a>Notes

Si cette propriété n’est pas définie, l’heure actuelle est utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
