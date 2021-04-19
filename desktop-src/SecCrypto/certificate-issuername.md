---
description: Récupère une chaîne qui contient le nom de l’émetteur du certificat.
ms.assetid: 6cf528e3-061a-44dc-b320-0e4b48a6c6ab
title: Propriété Certificate. IssuerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IssuerName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6b34b3bf198759d08fd3d0e3e4261407389a69a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533061"
---
# <a name="certificateissuername-property"></a>Propriété Certificate. IssuerName

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **IssuerName** récupère une chaîne qui contient le nom de l’émetteur du certificat.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Certificate.IssuerName As String
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne qui contient le nom de l’émetteur du certificat.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
