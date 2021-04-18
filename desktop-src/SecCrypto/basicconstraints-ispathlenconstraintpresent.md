---
description: Récupère une valeur booléenne qui indique si la contrainte de longueur de chemin d’accès est présente.
ms.assetid: 25840a62-13d1-4b54-9b09-64f77a465e06
title: BasicConstraints. IsPathLenConstraintPresent, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPathLenConstraintPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9809b6747bac548b14b37384719dbe2660188582
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532852"
---
# <a name="basicconstraintsispathlenconstraintpresent-property"></a>BasicConstraints. IsPathLenConstraintPresent, propriété

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP. Utilisez plutôt la [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]

La propriété **IsPathLenConstraintPresent** récupère une valeur booléenne qui indique si la contrainte de longueur de chemin d’accès est présente.

## <a name="syntax"></a>Syntaxe


```VB
BasicConstraints.IsPathLenConstraintPresent As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la **valeur est true**, la contrainte de longueur de chemin d’accès est présente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
