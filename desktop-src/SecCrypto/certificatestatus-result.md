---
description: La propriété Result récupère une valeur qui indique si le certificat est valide. Il s’agit de la propriété par défaut.
ms.assetid: b1edfbde-9d54-4e9c-ba9b-33e4c354c23f
title: CertificateStatus. Result, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Result
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dd67cd554fce84edc61b1b48e8a539b58a330ec1163b87b17dd8847b31fb15e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993219"
---
# <a name="certificatestatusresult-property"></a>CertificateStatus. Result, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**structure X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **result** récupère une valeur qui indique si le certificat est valide. Il s’agit de la propriété par défaut.

## <a name="syntax"></a>Syntaxe


```VB
CertificateStatus.Result As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la **valeur est true**, le certificat est valide. La validité du certificat est vérifiée à l’aide de la valeur actuelle de la propriété [**CheckFlag**](certificatestatus-checkflag.md) et des différents paramètres de stratégie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
