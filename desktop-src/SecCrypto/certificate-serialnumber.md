---
description: Récupère une chaîne qui contient le numéro de série du certificat.
ms.assetid: d08be744-4ae8-49f9-8b00-48e76c296f2b
title: Propriété Certificate. SerialNumber
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.SerialNumber
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f69836534dc9a45bcdecd88be83d9051c24852d966c0d0a4949016ff7feea3e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771270"
---
# <a name="certificateserialnumber-property"></a>Propriété Certificate. SerialNumber

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **SerialNumber** récupère une chaîne qui contient le numéro de série du certificat.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Certificate.SerialNumber As String
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne qui contient le numéro de série du certificat.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
