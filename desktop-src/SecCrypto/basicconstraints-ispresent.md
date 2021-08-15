---
description: Récupère une valeur booléenne qui indique si l’extension de contraintes de base est présente. Il s’agit de la propriété par défaut.
ms.assetid: 775b37fc-5015-4096-9e94-608f13a5ed14
title: BasicConstraints. IsPresent, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 646d7988b24d9ad03e55bb7ee4401875c42f7b779a81e1b80a611aaae18a93a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773021"
---
# <a name="basicconstraintsispresent-property"></a>BasicConstraints. IsPresent, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP. Utilisez plutôt la [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]

La propriété **IsPresent** récupère une valeur booléenne qui indique si l’extension de contraintes de base est présente. Il s’agit de la propriété par défaut.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
BasicConstraints.IsPresent As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la **valeur est true**, l’extension de contraintes de base est présente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BasicConstraints**](basicconstraints.md)
</dt> </dl>

 

 
