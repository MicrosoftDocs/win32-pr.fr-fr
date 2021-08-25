---
description: Récupère une valeur booléenne qui indique si le certificat est destiné à une autorité de certification (CA).
ms.assetid: 3ca43475-fe97-4eb4-875d-dbc15a0b953c
title: BasicConstraints. IsCertificateAuthority, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCertificateAuthority
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 90d616f4a7a0fe8522118848826bee88523ad45c34cb8a3fff23c722e68f2495
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879759"
---
# <a name="basicconstraintsiscertificateauthority-property"></a>BasicConstraints. IsCertificateAuthority, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP. Utilisez plutôt la [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]

La propriété **IsCertificateAuthority** récupère une valeur booléenne qui indique si le certificat est destiné à une [*autorité de certification*](../secgloss/c-gly.md) (ca).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
BasicConstraints.IsCertificateAuthority As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la **valeur est true**, le certificat doit être utilisé uniquement par une autorité de certification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
